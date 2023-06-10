<script>
import {defineComponent} from 'vue'

export default defineComponent({
   name: "HomeView",
   data() {
      return {
         demos: [
            {
               "name": "finance-parser",
               "description": "Serverless parser to extract information from financial reports using AWS Step Functions, AWS S3, AWS Api Gateway, AWS Textract, AWS DynamoDB and Eventbridge ",
               "url": "https://demo.denniscm.com/finance-parser"
            }
         ]
      }
   }
})
</script>

<template>
   <div class="container py-5">
      <p>DEMOS</p>
      <table class="table">
         <thead>
         <tr>
            <th scope="col">Name</th>
            <th scope="col">Description</th>
            <th scope="col">url</th>
         </tr>
         </thead>
         <tbody>
         <tr v-for="demo in demos">
            <td>{{ demo['name'] }}</td>
            <td>{{ demo['description'] }}</td>
            <td><a :href="demo['url']" target="_blank">Link</a></td>
         </tr>
         </tbody>
      </table>
   </div>
</template>