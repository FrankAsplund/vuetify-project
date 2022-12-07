<template>
  <v-app>

    <v-app-bar :elevation="8">
      <v-app-bar-nav-icon />
      <v-app-bar-title>
        Vuetify Tutorial
      </v-app-bar-title>
  <template v-slot:append>
    <v-btn icon="mdi-heart"></v-btn>

    <v-btn icon="mdi-magnify"></v-btn>

    <v-btn icon="mdi-dots-vertical"></v-btn>
  </template>
</v-app-bar>


<div class="container">

      <div class="d-flex align-center flex-row mx-4 ">      
        
        <v-card
        class="mx-4"
        width="400"
        title="This is a title"
        subtitle="This is a subtitle"
        text="This is content"
        ></v-card>

        <v-card
        class="mx-4"
        width="400"
        title="This is a title"
        subtitle="This is a subtitle"
        text="This is content"
        ></v-card>

        <v-card
        class="mx-4"
        width="400"
        title="This is a title"
        subtitle="This is a subtitle"
        text="This is content"
        ></v-card>
  </div>

  <v-form v-model="valid">
    <v-container>
      <v-row>
        <v-col
          cols="12"
          md="4"
        >
          <v-text-field
            v-model="firstname"
            :rules="nameRules"
            :counter="10"
            label="First name"
            required
          ></v-text-field>
        </v-col>

        <v-col
          cols="12"
          md="4"
        >
          <v-text-field
            v-model="lastname"
            :rules="nameRules"
            :counter="10"
            label="Last name"
            required
          ></v-text-field>
        </v-col>

        <v-col
          cols="12"
          md="4"
        >
          <v-text-field
            v-model="email"
            :rules="emailRules"
            label="E-mail"
            required
          ></v-text-field>
        </v-col>
      </v-row>
    </v-container>
  </v-form>
</div>

<v-bottom-navigation mode="shift">
  <v-btn value="recent">
    <v-icon>mdi-history</v-icon>
    
    Recent
  </v-btn>
  
  <v-btn value="favorites">
    <v-icon>mdi-heart</v-icon>
    
    Favorites
  </v-btn>

  <v-btn value="nearby">
    <v-icon>mdi-map-marker</v-icon>

    Nearby
  </v-btn>
</v-bottom-navigation>
  </v-app>
</template>

<script setup>

</script>

<style scoped>

.container {
  margin: 7rem 0 5rem 0;
}

/* .container-card {
  margin: 1rem;
} */


</style>
