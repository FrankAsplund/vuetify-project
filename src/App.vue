<template>
  <v-app>
    
    <v-app-bar :elevation="6" class="mb-16">
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

    <v-alert class="mt-16" title="Observera!" closable text="..." type="error" variant="tonal">Ingen av knapparna fungerar och är bara till för estetiska syften.</v-alert>
    
    
    <v-col class="mt-16">
      
      <div class="d-flex align-center flex-row mx-4 rounded-xl">      
        
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
      
      <v-divider class="mt-4" inset></v-divider>
    </v-col>
      

    
    <v-expansion-panels class="ma-8 w-50">
      <v-expansion-panel
      title="Expansion Panel"
      text="This is an expansion panel, lorem ipsum lorem ipsum"
      >
      
    </v-expansion-panel>
  </v-expansion-panels>
  

  <v-row auto>

    <v-col class="mb-16">
      <v-form class="mx-8 w-50"
      ref="form"
      v-model="valid"
lazy-validation
>
<v-text-field
v-model="name"
:counter="10"
:rules="nameRules"
label="Name"
required
></v-text-field>

<v-text-field
v-model="email"
:rules="emailRules"
label="E-mail"
required
></v-text-field>

<v-select
v-model="select"
:items="items"
:rules="[v => !!v || 'Item is required']"
label="Item"
required
></v-select>

<v-checkbox
v-model="checkbox"
:rules="[v => !!v || 'You must agree to continue!']"
label="Do you agree?"
required
></v-checkbox>

<v-btn
color="success"
class="mr-4"
@click="validate"
>
Validate
</v-btn>

<v-btn
color="error"
class="mr-4"
@click="reset"
>
Reset Form
</v-btn>

<v-btn
color="warning"
@click="resetValidation"
>
Reset Validation
</v-btn>
</v-form>


</v-col>

<v-hover>
  <template v-slot:default="{ isHovering, props }">
    <v-card
      v-bind="props"
      :color="isHovering ? 'primary' : undefined"
      title="Hover over me"
      text="..."
    ></v-card>
  </template>
</v-hover>

</v-row>


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

/* .container {
  margin: 7rem 0 5rem 0;
} */

/* .container-card {
  margin: 1rem;
} */


</style>
