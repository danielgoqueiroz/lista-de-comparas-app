<template>
  <ion-page>
    <ion-header>
      <ion-toolbar>
        <ion-title>Listas</ion-title>
      </ion-toolbar>
    </ion-header>
    <ion-content :fullscreen="true">
      <ion-header collapse="condense">
        <ion-toolbar>
          <ion-title size="large">Tab 1</ion-title>
        </ion-toolbar>
      </ion-header>
      <ion-list>
        <ion-item v-for="lista in listas" :key="lista.nome"> 
          <ion-label>{{lista.nome}}</ion-label>
        </ion-item>
      </ion-list>
    </ion-content>
  </ion-page>
</template>

<script lang="ts">
import {
  IonPage,
  IonHeader,
  IonToolbar,
  IonTitle,
  IonContent,
  IonList,
  IonItem,
} from "@ionic/vue";

export default {
  data() {
    return {
      listas: [ {nome: "Mercado Mãe"}, {nome: "Mercado"}]
    }
  },
  name: "Listas",
  components: {
    IonList,
    IonHeader,
    IonToolbar,
    IonTitle,
    IonContent,
    IonPage,
    IonItem,
  },
};
</script>
