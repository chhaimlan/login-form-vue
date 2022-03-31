<template>
<v-app>
    <v-app-bar app dark color="blue">
      <v-toolbar-title>Login</v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn text rounded>Home</v-btn>
      <v-btn text rounded>Login</v-btn>
      <v-btn text rounded>About</v-btn>
      <v-btn text rounded>Contact</v-btn>      
    </v-app-bar>
    <v-content>
      <v-card width="500" class="mx-auto mt-9">
        <v-card-title>Long Area</v-card-title>
      <v-card-text>
         <v-text-field label="username"  prepend-icon="mdi-account-circle"/>
         <v-text-field label="password" 
         :type="showPassword ? 'text' : 'password'" 
         prepend-icon="mdi-lock" :append-icon="showPassword ? 'mdi-eye' :  'mdi-eye-off'"
         @click:append="showPassword = !showPassword"
         />
      </v-card-text>
      <v-divider></v-divider>
      <v-card-actions>
         <v-btn color="success">Register</v-btn>
         <v-btn color="info">Login</v-btn>
      </v-card-actions>
      </v-card>
    </v-content>
  <template>
  <v-footer
    class="bg-indigo-lighten-1 text-white text-center d-flex flex-column" color="blue"
  >
    <div>
      <!-- <v-btn color="red"
        v-for="icon in icons"
        :key="icon"
        class="mx-4 text-white"
        :icon="icon"
        variant="text"
      ></v-btn> -->
      <v-avatar class="mx-4 text-white" color="success" size="x-small">      
        <v-icon start>mdi-facebook</v-icon>
      </v-avatar>
      <v-avatar class="mx-4 text-white" color="success" size="x-small">      
        <v-icon blue start>mdi-twitter</v-icon>
      </v-avatar>
      <v-avatar class="mx-4 text-white" color="success" size="x-small">      
        <v-icon blue start>mdi-linkedin</v-icon>
      </v-avatar>
      <v-avatar class="mx-4 text-white" color="success" size="x-small">      
        <v-icon blue start>mdi-instagram</v-icon>
      </v-avatar>
    </div>

    <div class="text-white pt-0">
      
    </div>

    <v-divider></v-divider>  
    <div class="text-white">
      {{ new Date().getFullYear() }} — <strong>Vue by Me</strong>
    </div>
   </v-footer>
  </template>
 </v-app>
</template>

<script>
export default {
      data: () => ({
      showPassword:false,
      icons: [
        'mdi-facebook',
        'mdi-twitter',
        'mdi-linkedin',
        'mdi-instagram',
      ],
    }),

  
       
  
}
</script>