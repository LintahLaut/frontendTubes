<template>   
    <v-navigation-drawer color="white" v-model="drawer" :rail="rail" permanent @click="rail = false">
        <v-list>
            <v-list-item
                prepend-avatar="https://media-exp1.licdn.com/dms/image/D4D03AQGapk0zWeda6Q/profile-displayphoto-shrink_800_800/0/1646372744955?e=2147483647&v=beta&t=u-FhXTsoRdmRhDH5kKNGHL77Tp_kiuhgbIzh_mrznK0"
                title="Dandy Lord" subtitle="dandy_lord@gmailcom"></v-list-item>
        </v-list>

        <v-divider></v-divider>

        <v-list density="compact" nav>
            <router-link to="/crud1" custom v-slot="{ navigate }">
                <v-list-item prepend-icon="mdi-folder" title="Crud 1" value="crud1" @click="navigate" role="link">
                </v-list-item>
            </router-link>

            <router-link to="/crud2" custom v-slot="{ navigate }">
                <v-list-item prepend-icon="mdi-home-city" title="Crud 2" value="crud2" @click="navigate" role="link">
                </v-list-item>
            </router-link>
            
            <router-link to="/" custom v-slot="{ navigate }">
                <v-list-item prepend-icon="mdi-home-city" title="Back Welcome" value="welcome" @click="navigate" role="link">
                </v-list-item>
            </router-link>
        </v-list>
    </v-navigation-drawer>
</template>

<script>
export default {
    data() {
        return {
            drawer: true,
            items: [
                { title: 'crud1', icon: 'mdi-home-city' },
                { title: 'crud2', icon: 'mdi-account' },
                { title: 'welcome', icon: 'mdi-account-group-outline' },
            ],
            mini: true,
        }
    },
}
</script>