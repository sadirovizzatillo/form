<template>
  <div>
    <FormBuilder :form="form"/>
  </div>
</template>

<script>
  import FormBuilder from './components/FormBuilder.vue'

  export default {
    name: 'App',
    components: {
      FormBuilder
    },
    data(){
      return{
        form:	[
        {
          "name": "image",
          "field_type": "file",
          "title": "Image",
          "label": "Image to display",
        },
        {
          "name": "full_name",
          "field_type": "text",
          "label": "Full Name",
          "placeholder": "Enter your full name",
          "required": true
        },
        {
          "name":"passport_number",
          "field_type": "password",
          "label": "Passport Number",
          "placeholder": "Enter your passport number",
          "required": true
        },
        {
          "name": "email",
          "field_type": "email",
          "label": "Email",
          "placeholder": "Enter your email",
          "required": true
        },
        {
          "name": "phone",
          "field_type": "tel",
          "label": "Phone",
          "placeholder": "Enter your phone number",
          "required": true
        },
        ]
      }
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
    margin-top: 30px;
  }
</style>
