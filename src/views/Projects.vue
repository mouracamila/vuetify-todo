<template>
  <div class="projects">
    <h1 class="subheading grey--text">Projects</h1>
        
    <v-container class="my-5">

      <v-expansion-panel>
        <v-expansion-panel-content v-for="project in projects" :key="project.title">
          <div slot="header">{{ project.title }}</div>
          <v-card>
            <v-card-text class="px-4 grey--text">
              <div class="font-weight-bold">due by {{ project.due}}</div>
              <div>{{ project.content }}</div>
            </v-card-text>
          </v-card>
        </v-expansion-panel-content>
      </v-expansion-panel>

    </v-container>
  
  </div>
    

</template>

<script>

export default {
  data() {
    return {
      projects: [
        { title: 'Design a new website', person:'Ninja', due: '1st Jan 2019', status: 'ongoing', content: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed to eiusmod tempor incididunt ut labore et dolore magna aliqua.'},
        { title: 'Code up the homepage', person:'chun Li', due: '10th Jan 2019', status:'complete', content:'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed to eiusmod tempor incididunt ut labore et dolore magna aliqua.'},
        { title: 'Design a the homepage', person:'Ryu', due: '20th Dec 2019', status: 'complete', content:'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed to eiusmod tempor incididunt ut labore et dolore magna aliqua.'},
        { title: 'Create a community forum', person:'Rafa', due: '14th Jul 2019', status: 'overdue', content:'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed to eiusmod tempor incididunt ut labore et dolore magna aliqua.'}
      ]
    }
  },
  computed: {
    myProjects(){
      return this.projects.filter(project => {
        return project.person === 'Ninja'
      })
    }
  }
}
</script>
