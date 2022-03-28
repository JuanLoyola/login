<template>
  <v-container>
    <v-row align="center" justify="center">
      <v-col cols="12" sm="10">
        <v-card class="elevation-6 mt-10">
          <v-window v-model="step">

            <!-- Login account section -->
            <v-window-item :value="1">
              <v-row class="white black--text">
                <v-col cols="12" sm="6" class="white darken-2">
                  <v-card-text class="mt-12">
                    <h3 class="text-center">Login in to your Account</h3>
                    <h5 class="text-center grey--text">Log in to your account so you can continue building
                      <br> and editing your onboarding flows
                    </h5>
                    <v-row align="center" justify="center">
                      <v-col cols="12" sm="6">
                        <v-text-field label="Email" outlined dense color="orange darken-1" autocomplete="false" class="mt-16"></v-text-field>
                        <v-text-field label="Password" outlined dense color="orange darken-1" autocomplete="false" type="password"></v-text-field>
                        <v-row>
                          <v-col cols="12" sm="7">
                            <v-checkbox label="Remember Me" class="mt-n1" color="orange darken-1"></v-checkbox>
                          </v-col>
                          <v-col cols="12" sm="5">
                            <span class="caption orange--text">Forget password</span>
                          </v-col>
                        </v-row>
                        <v-btn color="orange darken-1" dark block tile>Login in</v-btn>
                        <h5 class="text-center mt-4 mb-3">Or Log in using</h5>
                        <div class="d-flex justify-space-around align-center mx-10 mb-16">
                          <v-btn depressed outlined color="grey">
                            <v-icon color="red">fab fa-google</v-icon>
                          </v-btn>
                          <v-btn depressed outlined color="grey">
                            <v-icon color="blue">fab fa-facebook</v-icon>
                          </v-btn>
                          <v-btn depressed outlined color="grey">
                            <v-icon color="light-blue lighten-3">fab fa-twitter</v-icon>
                          </v-btn>
                        </div>
                      </v-col>
                    </v-row>
                  </v-card-text>
                </v-col>
                <v-col cols="12" sm="6" class="orange darken-1 rounded-bl-xl">
                  <div style="text-align:center; padding: 180px 0;">
                    <v-card-text class="white--text">
                      <h3 class="text-center">Don't Have and Account Yet?</h3>
                      <h6 class="text-center">Let's get you all set up so you can start creating your first <br>onboarding experience</h6>
                    </v-card-text>
                    <div class="text-center">
                      <v-btn tile outlined dark @click="step++"> 
                        SIGN UP
                      </v-btn>
                    </div>
                  </div>
                </v-col>
              </v-row>
            </v-window-item>

            <!-- Create account section -->
            <v-window-item :value="2">
              <v-row class="white black--text">
                <v-col cols="12" sm="6" class="orange darken-1 rounded-br-xl">
                  <div style="text-align: center; padding: 180px 0;">
                    <v-card-text class="white--text">
                      <h3 class="text-center">Already Signed up?</h3>
                      <h6 class="text-center" >Sign Log in to your account so you can continue building and <br>editing your onboarding flows</h6>
                    </v-card-text>
                    <div class="text-center">
                      <v-btn tile outlined dark @click="step--">Log in</v-btn>
                    </div>
                  </div>
                </v-col>
                <v-col cols="12" sm="6">
                  <v-card-text class="mt-12">
                    <h3 class="text-center">Sign up for an Account</h3>
                    <h5 class="text-center grey--text"> Let's get you all set up so you can start creating your <br> firts onboarding experience</h5>
                    <v-row align="center" justify="center">
                      <v-col cols="12" sm="8">
                        <v-row>
                          <v-col cols="12" sm="6">
                            <v-text-field label="First Name" outlined dense color="orange darken-1" autocomplete="false" class="mt-4"></v-text-field>
                          </v-col>
                          <v-col cols="12" sm="6">
                            <v-text-field label="Last Name" outlined dense color="orange darken-1" autocomplete="false" class="mt-4"></v-text-field>
                          </v-col>
                        </v-row>
                        <v-text-field label="Email" outlined dense color="orange darken-1" autocomplete="false"></v-text-field>
                        <v-text-field label="Password" outlined dense color="orange darken-1" autocomplete="false" type="password"></v-text-field>
                        <v-row>
                          <v-col cols="12" sm="7">
                            <v-checkbox label="I accept" class="mt-n1" color="orange darken-1"></v-checkbox>
                          </v-col>
                          <v-col cols="12" sm="5">
                            <span class="caption orange--text ml-n4">Terms & Conditions</span>
                          </v-col>
                        </v-row>
                        <v-btn color="orange darken-1" dark block tile>Sign up</v-btn>
                        <h5 class="text-center gray--text mt-4 mb-3">Or sign up using</h5>
                        <div class="d-flex justify-space-around align-center mx-10 mb-16">
                          <v-btn depressed outlined color="grey">
                            <v-icon color="red">fab fa-google</v-icon>
                          </v-btn>
                          <v-btn depressed outlined color="grey">
                            <v-icon color="blue">fab fa-facebook</v-icon>
                          </v-btn>
                          <v-btn depressed outlined color="grey">
                            <v-icon color="light-blue lighten-3">fab fa-twitter</v-icon>
                          </v-btn>
                        </div>
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
</template>

<script>
// @ is an alias to /src

export default {
  name: 'Home',
  data: () => ({
    step: 1
  }),
  props: {
    source: String
  },
  components: {
    
  }
}
</script>

<style scoped>
  .v-application .rounded-bl-xl {
    border-bottom-left-radius:300px !important;
  }
  .v-application .rounded-br-xl {
    border-bottom-right-radius: 300px !important;
  }
</style>
