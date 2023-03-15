

<template>

  <div id="wrapper">
    <NavBar />
    <div id="container">
      <div id="sidebar">
        <div v-for="page in pages" @click="currentPage = page" class="sidebarBtn">{{page}}</div>
       </div>
       <div id="content">
        <Home v-if="currentPage == 'home'"/>
        <Conge v-if="currentPage == 'congé'"/>
        <Employees v-if="currentPage == 'employees'"/>
       </div>
    </div>
  </div>

</template>


<script>
import Home from '../views/Home.vue'
import Conge from '../views/Conge.vue'
import Employees from '../views/Employees.vue'
import NavBar from '../views/NavBar.vue'
export default{
  components: {Home, Conge, Employees, NavBar},
  data(){
    return{
      currentPage: 'home',
      pages: ['home', 'employees', 'congé']
    }
  }
}
</script>