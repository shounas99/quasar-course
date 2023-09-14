<template>
  <q-page class="q-ma-md">
    <span class="text-h3">Forms</span>
    <q-separator />

    <div class="row justify-center">
      <q-form
        @submit="onSubmit"
        @reset="onReset"
        class="q-gutter-sm col-xs-12 col-sm-12 col-md-6 q-pt-xl"
      >
        <q-input
          filled
          v-model="userForm.email"
          type="email"
          label="Escribe tu correo electronico *"
          lazy-rules
          no-error-icon
          :rules="[
            (val) => (val && val.length > 0) || 'Este campo es obligatorio',
            isValidEmail,
          ]"
        />

        <q-input
          filled
          type="password"
          v-model="userForm.password1"
          label="Escribe tu contraseña *"
          lazy-rules
          no-error-icon
          :rules="[
            (val) => (val && val.length > 0) || 'Este campo es obligatorio',
          ]"
        />
        <q-input
          filled
          type="password"
          v-model="userForm.password2"
          label="Repite tu contraseña *"
          lazy-rules
          no-error-icon
          :rules="[
            (val) => (val && val.length > 0) || 'Este campo es obligatorio',
            isSamePassword,
          ]"
        />

        <q-checkbox
          v-model="userForm.conditions"
          :style="
            userForm.errorInConditions && !userForm.conditions && 'color: red'
          "
          label="Acepto las condiciones y términos de uso."
        />

        <div class="row justify-end">
          <q-btn
            label="Reset"
            type="reset"
            color="primary"
            flat
            class="q-ml-sm"
          />
          <q-btn unelevated label="Submit" type="submit" color="primary" />
        </div>
      </q-form>
    </div>
  </q-page>
</template>

<script>
import { defineComponent, ref } from "vue";
// inside of a Vue file
import { useQuasar } from "quasar";

export default defineComponent({
  name: "FormsPage",

  setup() {
    const $q = useQuasar();

    const userForm = ref({
      email: "",
      password1: "",
      password2: "",
      conditions: false,
      errorInConditions: false,
    });

    return {
      userForm,

      onSubmit() {
        if (!userForm.value.conditions) {
          $q.notify({
            message: "Debe de aceptar las condiciones",
            icon: "las la-exclamation-circle",
          });
          console.log("Debe de aceptar las condiciones");
          userForm.value.errorInConditions = true;
          return;
        }
        console.log("USER FORM", userForm.value);
      },
      onReset() {
        userForm.value = {
          email: "",
          password1: "",
          password2: "",
          conditions: false,
          errorInConditions: false,
        };
      },

      isValidEmail(val) {
        const emailPattern =
          /^(?=[a-zA-Z0-9@._%+-]{6,254}$)[a-zA-Z0-9._%+-]{1,64}@(?:[a-zA-Z0-9-]{1,63}\.){1,8}[a-zA-Z]{2,63}$/;
        return emailPattern.test(val) || "El correo no parece ser válido";
      },
      isSamePassword(val) {
        return (
          val === userForm.value.password1 || "Las contraseñas no son iguales"
        ); //Si son iguales las contraseñas mando un true, sino mando mensaje
      },
    };
  },
});
</script>
