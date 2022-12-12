<template>
    <v-app id="login">
        <v-parallax dark src="https://images.pexels.com/photos/853427/pexels-photo-853427.jpeg?cs=srgb&dl=pexels-delbeautybox-853427.jpg&fm=jpg" height="800">
            <v-container>
                <v-row align="center" justify="center">
                    <v-col cols="12" sm="12">
                        <v-card class="elevation-6 mt-16" color="black">
                            <v-window v-model="step">
                                <v-window-item :value="1">
                                    <v-row>
                                        <v-col cols="12" md="6">
                                            <v-card-text class="mt-12">
                                                <h4 class="text-center">Login in to Your Account</h4>
                                                <h6 class="text-center  grey--text "> Log in to your account to access your salon<br>and editing your onboarding flows</h6>
                                                <v-row align="center" justify="center">
                                                    <v-col cols="12" sm="8">
                                                        <v-text-field label="Email" persistent-hint variant="outlined" color="#FBDF7E" autocomplete="false" class="mt-16"></v-text-field>
                                                        <v-text-field label="Password" persistent-hint variant="outlined" color="#FBDF7E" autocomplete="false" type="password"></v-text-field>
                                                        <v-row>
                                                            <v-col cols="12" sm="6">
                                                                <router-link to="/" custom v-slot="{ navigate }">
                                                                    <v-btn @click="navigate" role="link" block tile dark class="text-yellow" variant="outlined">
                                                                        BACK
                                                                    </v-btn>
                                                                </router-link>                                                            
                                                            </v-col>
                                                            <v-col cols="12" sm="6">
                                                                <v-btn color="#FBDF7E" dark block tile class="text-yellow" variant="outlined">Log in</v-btn>
                                                            </v-col>
                                                        </v-row>
                                                    </v-col>
                                                </v-row>
                                            </v-card-text>
                                        </v-col>
                                        <v-col cols="12" md="6" class="orange rounded-bl-xl">
                                            <div style="  text-align: center; padding: 180px 0;">
                                                <v-card-text class="white--text">
                                                    <h1 class="text-center ">Don't Have an Account Yet?</h1>
                                                    <br>
                                                    <h5 class="text-center">Let's get you all set up so you can start creating your your first<br> onboarding experience</h5>
                                                </v-card-text>
                                                <div class="text-center">
                                                    <v-btn @click="step++" tile dark class="text-yellow mt-8" variant="outlined">SIGN UP</v-btn>
                                                    <v-text-field loading disabled></v-text-field>
                                                </div>
                                            </div>
                                        </v-col>
                                    </v-row>
                                </v-window-item>
                                <v-window-item :value="2">
                                    <v-row>
                                        <v-col cols="12" md="6" class="orange rounded-br-xl">
                                            <div style="  text-align: center; padding: 180px 0;">
                                                <v-card-text class="white--text">
                                                    <h1 class="text-center ">Alredy Signed up?</h1>
                                                    <br>
                                                    <h5 class="text-center">Log in to your account so you can continue building and<br> editing your onboarding flows</h5>
                                                </v-card-text>
                                                <div class="text-center">
                                                    <v-btn @click="step--" tile dark class="text-yellow mt-8" variant="outlined">Log in</v-btn>
                                                    <v-text-field loading disabled></v-text-field>
                                                </div>
                                            </div>
                                        </v-col>
        
                                        <v-col cols="12" md="6">
                                            <v-card-text class="mt-12">
                                                <h4 class="text-center">Sign Up for an Account</h4>
                                                <br>
                                                <v-row align="center" justify="center">
                                                <h6 class="text-center  grey--text ">Let's get you all set up so you can start creatin your <br> first onboarding experiance</h6>
                                                <br>
                                                    <v-col cols="12" sm="8">                                                
                                                        <v-text-field label="Name" persistent-hint variant="outlined" color="#FBDF7E"/>
                                                        <v-text-field label="Email" persistent-hint variant="outlined" color="#FBDF7E"></v-text-field>
                                                        <v-text-field label="Password" persistent-hint variant="outlined" color="#FBDF7E" type="password"></v-text-field>
                                                        <v-file-input label="Upload Image" accept="image/*" persistent-hint variant="outlined" show-size color="#FBDF7E"></v-file-input>
                                                        <v-btn color="#FBDF7E" dark block tile class="text-yellow mt-8" variant="outlined">Sign up</v-btn>
                                                    </v-col>
                                                </v-row>
                                            </v-card-text>
                                        </v-col>
                                    </v-row>
                                </v-window-item>
                            </v-window>
                        </v-card>
                    </v-col>
                </v-row>
            </v-container>        
        </v-parallax>
    </v-app>
</template>

<script>


export default {
    name: "LoginView",
    data: () => ({
        step: 1
    }),
    props: {
        source: String
    }

}
</script>
<style scoped>
.v-application .rounded-bl-xl {
    border-bottom-left-radius: 300px !important;
}

.v-application .rounded-br-xl {
    border-bottom-right-radius: 300px !important;
}
</style>