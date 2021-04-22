<template>
  <nav class="w-full bg-gray-700 absolute top-0 left-0 min-h-full">
      <li>Home</li>
      <li>About</li>
      <li>Contact</li>

      <div @click='handleToggle' class='w-16 h-12 border-2 border-blue-500'>
          Toggle close
        </div>
  </nav>
</template>

<script>
export default {
    methods:{
        handleToggle(){
            this.$emit('closeNav')
        }
    }
}
</script>

<style>

</style>