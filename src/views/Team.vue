<template>
  <div class="team">
    <h1 class="subheading grey--text">Team</h1>

    <v-container class="my-5">
      <v-layout row wrap>
        <v-flex xs12 sm6 md4 lg3 v-for="person in team" :key="person.name">
          <v-card flat class="text-xs-center ma-3">
            <v-responsive class="pt-4">
              <v-avatar size="100" class="grey lighten-2">
                <img :src="person.avatar" />
              </v-avatar>
            </v-responsive>
            <v-card-text>
              <div class="subheading">{{ person.name }}</div>
              <div class="grey--text">{{ person.role }}</div>
            </v-card-text>
            <v-card-action>
              <v-btn flat color="grey">
                <v-icon small left>message</v-icon>
                <span>Message</span>
              </v-btn>
            </v-card-action>
          </v-card>
        </v-flex>
      </v-layout>
    </v-container>
  </div>
</template>

<script>
export default {
  data() {
    return {
      team: [
        {
          name: "Ioda",
          role: "Web developer",
          avatar: "https://i.pravatar.cc/150?img=1"
        },
        {
          name: "Luke",
          role: "Graphic designer",
          avatar: "https://i.pravatar.cc/150?img=2"
        },
        {
          name: "Batman",
          role: "Web developer",
          avatar: "https://i.pravatar.cc/150?img=3"
        },
        {
          name: "Leonardo",
          role: "Social media maverick",
          avatar: "https://i.pravatar.cc/150?img=4"
        },
        {
          name: "Jak",
          role: "Sales guru",
          avatar: "https://i.pravatar.cc/150?img=5"
        }
      ]
    };
  }
};
</script>
