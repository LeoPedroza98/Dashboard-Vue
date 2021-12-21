<template>
    <v-navigation-drawer v-model="drawer" app>
        <v-img height="140" class="pa-4" src="https://images.pexels.com/photos/531880/pexels-photo-531880.jpeg?auto=compress&cs=tinysrgb&dpr=1&w=500">
            <div class="text-center">
                <v-avatar class="mb-4" color="grey darken-1" size="64">
                    <v-img aspect-ratio="30" src="https://www.publicdomainpictures.net/pictures/270000/velka/avatar-people-person-business-.jpg"></v-img>
                </v-avatar>
                <h2 class="white--text">Leonardo Pedroza</h2>
            </div>
        </v-img>
        <v-divider></v-divider>
        <v-list>
            <v-list-item v-for="[icon, text] in links" :key="icon" link>
                <v-list-item-icon>
                    <v-icon>{{icon}}</v-icon>
                </v-list-item-icon>
                <v-list-item-content>
                    <v-list-item-title>{{ text }}</v-list-item-title>
                </v-list-item-content>
            </v-list-item>
        </v-list>
    </v-navigation-drawer>
</template>
<script>
export default{
  name: "Sidebar",
  props: ["drawer"],
  data() {
    return {
      links: [
        ["mdi-microsoft-windows", "Dashboard"],
        ["mdi-account", "Perfil"],
        ["mdi-clipboard-list-outline", "Produtos"],
        ["mdi-card-account-details-outline", "Ordens"],
        ["mdi-cog", "Configurações de Sistemaa"],
      ],
    };
  }
}
</script>