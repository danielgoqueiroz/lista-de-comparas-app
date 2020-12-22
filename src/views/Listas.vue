<template>
  <ion-page>
    <ion-header>
      <ion-toolbar>
        <ion-title>Listas {{count}}</ion-title>
        
      </ion-toolbar>
    </ion-header>
    <ion-content :fullscreen="true">
      <ion-header collapse="condense">
        <ion-toolbar>
          <ion-title size="large">Listas</ion-title>
        </ion-toolbar>
      </ion-header>
      <ion-list>
        <ion-item v-for="lista in listas" :key="lista.nome" button @click="acao(lista.nome)"> 
          <ion-label>{{lista.nome}}</ion-label>
        </ion-item>
      </ion-list>
      <ion-button @click="acao('teste')">Adicionar Lista</ion-button>
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
  IonButton,
  IonLabel
} from "@ionic/vue";

export default {
  data() {
    return {
      count: 0,
      listas: [ {nome: "Mercado Mãe"}, {nome: "Mercado"}]
    }
  },
   methods: {
    acao (nome: string) {
      console.log(`Lista ${nome}`)
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
    IonButton,
    IonLabel
  },
};
</script>
