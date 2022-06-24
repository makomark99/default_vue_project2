<template>
  <div class="container-fluid nav-bg-color ">
    <div class="container">
      <nav class="navbar navbar-expand-lg navbar-light">
        <button
          class="navbar-toggler"
          type="button"
          data-toggle="collapse"
          data-target="#navbarSupportedContent"
          aria-controls="navbarSupportedContent"
          aria-expanded="false"
          aria-label="Toggle navigation"
        >
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarSupportedContent">
          <ul class="navbar-nav mr-auto">
            <li class="nav-item"
                v-for="(menuItem,index) in menuItems" :key="index">
              <router-link class="nav-link" :to="menuItem.to">{{menuItem.title}}</router-link>
            </li>
          </ul>
        </div>
      </nav>
    </div>
  </div>
</template>

<script>
export default {
  name: "app-nav",
  data(){
      return{
          menuItems:[
              {title:'Nyitó oldal',to:'/'},
              {title:'Bejelentkezés',to:'/bejelentkezes'},
              {title:'Profil',to:'/profil'},
              {title:'Kijeletkezés',to:'/kijelentkezes'},
          ],
      }
  }
};
</script>

<style>
</style>