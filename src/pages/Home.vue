<template>
    <div>
       <navbar />
       <section class="home">
   
   <div class="image">
       <img src="images/profile.png" alt="">
   </div>
   
   <div class="content">
       <h3>"FOOT FRUIT FOOD"</h3>
       <span>"Fastest Delivery & Easy Pickup"</span>
       <p>ร้านอาหารของเราเป็นร้านที่ มีอาหารหลากหลายรูปเเบบ หลากหลายสัญชาติในร้านเดียว เเละ มีราคาที่ย่อมเยาว์ ด้วยระบบสั่งอาหารออนไลน์ก็จะทําทุกท่านได้เลือกอาหารที่อยากทานด้วยปลายนิ้ว เเละรอรับที่บ้านของท่าน S I M P L E</p>
       
   
   </div>
   <div class="content">
       <p> <span>Fast Delivery : </span> Promise to deliver within 30 mins </p>
       <p> <span>Easy Pickup : </span> Easy order & easy life </p>
       <p> <span>Good food :  </span> Food that makes you say wow.  </p>
       <p> <span>Fresh food :   </span>Enjoy your food fresh crispy and hot. 	</p>
       <p> <span>Promotion :  </span>There are a lot of foods promotion. </p>
   </div>
   
   </section>
    </div>
   </template>
   
   <script>
   import Navbar from '../components/Navbar.vue';
   import axios from 'axios'
   
   
   export default {
       components: { Navbar },
       methods: {
           async fetchExperience() {
               try {
                   let res = await axios.get("https://633fc566e44b83bc73c0f545.mockapi.io/profile/v1/experiences")
                   this.experience = res.data
               } catch (error) {
           
               }
           }
            
       },
       data() { 
           return { 
               experience: []
           }
       },
       beforeMount() {
           this.fetchExperience()
       }
   
               
       } 
   
   </script>
   
   <style>
   
   </style>