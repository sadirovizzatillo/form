<template>
      <div class="shadow overflow-hidden sm:rounded-md">
        <div class="px-4 py-5 bg-white sm:p-6">
          <div class="col-span-6 sm:col-span-3 lg:col-span-2">
            <label :for="name" class="flex text-sm font-medium text-gray-700">{{ label }}</label>
            <input
            :type="type"
            :name="name"
            id="postal-code"
            :placeholder="placeholder"
            v-model="fields"
             required class="appearance-none rounded-none relative block w-full px-3 py-2 border border-gray-300 placeholder-gray-500 text-gray-900 rounded-b-md focus:outline-none focus:ring-indigo-500 focus:border-indigo-500 focus:z-10 sm:text-sm"
            >
          </div>
        </div>
      </div>
</template>

<script>
  export default {
    name: 'FormBuilder',
    data(){
      return{
        fields:[]
      }
    },
    props:{
      item:{
        type:Object,
        required:true
      }
    },
    computed:{
      name(){
        return this.item.name
      },
      placeholder(){
        return this.item.placeholder
      },
      type(){
        return this.item.field_type
      },
      label(){
        return this.item.label
      }
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  h3 {
    margin: 40px 0 0;
  }
  ul {
    list-style-type: none;
    padding: 0;
  }
  li {
    display: inline-block;
    margin: 0 10px;
  }
  a {
    color: #42b983;
  }
</style>
