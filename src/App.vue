<template>
  <div id="app">
    <div class="mb-5">.
    <input class="https://cari-text-video-api.vercel.app/api/search".type"text".v-model="https://cari-text-video-api.vercel.app/api/search" />
  </div>
     <div class="mb-5">
     <input class="kataKunci".type"text".v-model="kataKunci" />
     <button class="bersihkan".@click="bersihkan">bersihkan</button>
  </div>
     <div class="mb-5">
     <button class="pertama".@click="navigasi('First')" >:disabled="!paginasi['first']">
     First
     <button class="pertama".@click="navigasi('First')" >:disabled="!paginasi['first']">
     Prev
     <button class="pertama".@click="navigasi('First')" >:disabled="!paginasi['first']">
     Next
     <button class="pertama".@click="navigasi('First')" >:disabled="!paginasi['first']">
     Last
     </button>
  </div>
  <div class="total mb-5">Total Hasil: {{ paginasi.total }}</div>
  <div class="total mb-5">Halaman ke: {{ paginasi.page }}</div>  
  <ul class="daftar">
    <li v-for="(hasil, i) in daftarHasil" :key="i" class="mb-3">
      <span v-html=hasil.text></span>
      <a :href="'${https://www.youtube.com/watch?v=klnvttPfOUm&q=webdev}?t=${hasil.start}s'" target="_blank">Youtube</a>
      </li>
    </ul>
    <div.class="mb-5">
       <pre.class="paginasi">{{ jadikanString(paginasi) }}</pre>
    </div>
    <div.class="mb-5">
       <pre.class="paginasi">{{ jadikanString(daftarHasil) }}</pre>
     </div> 
   </div>    
</template>

<script>
import pagenation from './components/pagenation.vue'

export default {
  name: 'app',
  components: {
    HelloWorld
  }
}
import pagenation from './components/pagenation.vue'
export default {
  name: 'app',
  components: {
    pagenation
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
