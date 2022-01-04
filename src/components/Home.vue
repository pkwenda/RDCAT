<template>
  <v-app id="inspire">
    
 <div class="ma-12 pa-12">
   
    <v-card>
      
      <!-- left nav -->
      <!-- https://vuetifyjs.com/zh-Hans/api/v-navigation-drawer/#props -->
      <v-navigation-drawer
        permanent
        mini-variant
        app
        clipped
        left
      >
        <v-list>
          <v-list-item class="px-2">
            <v-list-item-avatar>
              <v-img src="https://randomuser.me/api/portraits/women/85.jpg"></v-img>
            </v-list-item-avatar>
          </v-list-item>
         
        </v-list>

        <v-divider></v-divider>

        <v-list
          nav
          dense
        >
          <v-list-item link  >
            <v-list-item-title><v-icon>mdi-folder</v-icon></v-list-item-title>
          </v-list-item>
          <v-list-item link>
            <v-list-item-title><v-icon>mdi-account-multiple</v-icon></v-list-item-title>
          </v-list-item>
          <v-list-item link>
            <v-list-item-title> <v-icon>mdi-star</v-icon></v-list-item-title>
          </v-list-item>
        </v-list>

        
      </v-navigation-drawer>


       <!-- left nav -->
      <!-- https://vuetifyjs.com/zh-Hans/api/v-navigation-drawer/#props -->
      <v-navigation-drawer
        permanent
        width="150"
        app
        clipped
        left
        style="margin-left: 56px;"
      >
        <v-list>
      <v-list-item-group v-model="model">
        <v-list-item
          v-for="(i) in 16"
          :key="i"
        >
           
          <v-list-item-content>
            <v-list-item-title > DB  {{i}}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list-item-group>
    </v-list>

        
      </v-navigation-drawer>
  
    </v-card>

    
    
  </div>

    <!-- right nav -->
    <!-- permanent mean not folding -->
    <v-navigation-drawer
      permanent 
      app
      clipped
      right
    >
      <v-list>
        <v-list-item
          v-for="n in 5"
          :key="n"
          link
        >
          <v-list-item-content>
            <v-list-item-title>Item {{ n }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-main>
      <!--  -->
      
    </v-main>

    <v-footer
      app
      color="transparent"
      height="72"
      inset
    >
      <v-text-field
        background-color="grey lighten-1"
        dense
        flat
        hide-details
        rounded
        solo
      ></v-text-field>
    </v-footer>
  </v-app>
</template>
 

<script>
export default {
    name: 'Home',
    data: () => ({ drawer: null }),
  } 
</script>
