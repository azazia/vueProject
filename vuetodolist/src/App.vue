<template>
    <div id="app">
        <div class="container">
            <div class="row header p-5">
                <div class="col-lg-12">
                    <h2>What I do today</h2>
                </div>
            </div>
            <div class="row content">
                <div class="col-lg-12">
                    <div class="pekerjaan-rumah">
                        <div class="row">
                            <div v-for="tugasSaya in tugas" v-bind:key="tugasSaya.id" class="mb-3 tugas col-lg-12 text-left">
                                <ItemTugas v-bind:tugasSaya="tugasSaya"/>
                            </div>
                        </div>                        
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>

import 'bootstrap/dist/css/bootstrap.css'
import ItemTugas from './components/ItemTugas.vue'

export default {
  name: 'App',
  data: function(){
      return{
        tugas: [
            {
                id: 1,
                namaTugas: "Menyapu Rumah",
                isDone: false
            },
            {
                id: 2,
                namaTugas: "Memasak ayam",
                isDone: false
            },
            {
                id: 3,
                namaTugas: "Belajar pemogramman",
                isDone: false
            }
        ]
      }
  },
  components: {
    ItemTugas
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.header {
    background: blue;
    color: white;
    margin-bottom: 20px;
}
.header h2{
    margin: 0px;
}
.tugas {
    font-size: 20px;
}

.item{
    color: green;
}
</style>
