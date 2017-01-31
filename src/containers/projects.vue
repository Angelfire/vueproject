<template>
  <div id="projects">
    <div class="columns">
      <div class="column is-half">
        <div class="notificacion">
          List of fake projects
        </div>
        <div>
          <table class="table">
            <thead>
              <tr>
                <th>Project name</th>
                <th>Assign to</th>
                <th>Prority</th>
              </tr>
            </thead>
            <tbody>
              <tr v-for="item in projects">
                <td>{{item.name}}</td>
                <td>{{item.assignedTo}}</td>
                <td>{{item.priority}}</td>
              </tr>
            </tbody>
          </table>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  import axios from 'axios'

  export default {
    name: 'projects',
/*    data: function() {
      return {
        projects: []
      }
    },*/
    data: () => ({
      projects: []
    }),
    methods: {
      loadProjects: function() {
        axios
          .get('http://www.mocky.io/v2/585e03ce100000b82c501e8e')
          .then((response) => {
            this.projects = response.data
          }, (err) => {
            console.log(err)
          })
      }
    },
    mounted: function() {
      this.loadProjects()
    }
  }
</script>
