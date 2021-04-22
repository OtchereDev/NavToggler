<template>
<div class=" relative min-h-screen overflow-x-hidden body">

  <NavBar @closeNav='handleToggle'/>
  <div ref="body" class="absolute top-0 left-0 z-10 min-h-screen w-full">
    <div class='bg-gray-300 min-h-screen '>

      <nav>
        <div @click='handleToggle' class='w-16 h-12 border-2 border-blue-500'>
          Toggle open
        </div>
      </nav>
      <div>
        Main
      </div>
    </div>
  </div>
</div>
  
</template>

<script>
import NavBar from '@/components/NavBar.vue'

export default {
  name: 'App',
  components: {
    NavBar
  },
  methods:{
    handleToggle(){
      const body=this.$refs.body
      if(body.classList.contains('top-0')){
        body.classList.remove('top-0')
        body.classList.remove('left-0')
        body.classList.remove('min-h-screen')
        body.style.top= '30%'
        body.style.left= '90%'
        body.style.minHeight= '90vh'
        
      }else{
        body.style.top= '0%'
        body.style.left= '0%'
        body.style.minHeight= '100vh'
        body.classList.add('top-0')
        body.classList.add('left-0')
        body.classList.add('min-h-screen')
      }
    }
  }
}
</script>

<style>
.body{
  overflow-x: hidden;
}
</style>
