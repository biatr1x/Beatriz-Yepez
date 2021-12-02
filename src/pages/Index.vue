<template>
  <q-page class="flex flex-center">
    <!--<img
      alt="Quasar logo"
      src="~assets/quasar-logo-vertical.svg"
      style="width: 200px; height: 200px"
    >-->
    <div class="q-pa-lg row items-start q-gutter-lg">
        <q-card class="my-card bg-secondary">
            <q-card-section>
                <div class="text-h6">Ingrese los datos </div>
            </q-card-section>
            <q-card-section>
            <!--formulario-->
                <q-input v-model="nomb1" label="Primer Nombre" stack-label :dense="dense" />
                <q-input v-model="nomb2" label="Segundo Nombre" stack-label :dense="dense" />
                <q-input v-model="apell1" label="Primer Apellido" stack-label :dense="dense" />
                <q-input v-model="apell2" label="Segundo Apellido" stack-label :dense="dense" />
                <q-select v-model="tipoident" :options="options" label="Tipo de identificacion" />
                <q-input v-model="ident" label="Identificacion" stack-label :dense="dense" />
                <q-input v-model="gmail" label="Correo Electronico" stack-label :dense="dense" />
                <q-input v-model="telf" label="Telefono" stack-label :dense="dense" />
                <q-separator dark />
                <q-date v-model= "date" />
            </q-card-section>
            <q-separator dark />
            <q-card-actions>
                <q-btn flat> Guardar </q-btn>
            </q-card-actions>
        </q-card>
    </div>
  </q-page>
</template>

<script>
import { ref } from 'vue'
export default {
  setup () {
    return {
      nomb1: ref(' '),
      nomb2: ref(' '),
      apell1: ref(' '),
      apell2: ref(' '),
      tipoident: ref(' '),
      ident: ref(' '),
      gmail: ref(' '),
      telf: ref(' '),
      dense: ref(null),
      date: ref(' 2021/12/02'),
      options: [
        'ID Nacional', 'ID Extranjera', 'Pasaporte'
      ]
    }
  }
}
</script>
