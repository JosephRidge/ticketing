<!-- template -->
<template>
  <div class="topNavigationBar">
    <!-- logo -->
    <div class="logoStyle">bree ..</div>
    <!-- routes -->
    <div id="routes">
      <div id="route"><a href="">home</a></div>
      <div id="route"><a href="">events</a></div>
      <div id="route"><a href="">about</a></div>
    </div>
    <!-- props rendering -->
    <div>{{ msg }}</div>
    <button @click="alterColor">change text style</button>

    <!--
   1. where ar gpipng to use class csss selector 
    to style the duiv tag
  2. We are going to  make it dynmaic in nature(chnageable at run time)
  3. Create a function to trigger the dynamic 
  nature
  -->
    <div :id="nameOfIndividual">John Doe</div>

    <!-- Binding images  -->
    <!-- <img :src="imageOfLand"/> -->


    <!--  conditional rendering 
    v-if...v-else...v-else-if... -->
<div v-if="imageOfCar">
  <img :src="imageOfCar"/>
</div>
<div v-else> No Image found</div>

<div v-show="imageOfCar">
  <img :src="imageOfCar"/></div>






<button @click="increaseAge">add age</button>
<button @click="descreaseAge">reduce Age</button>
<div>{{age}}</div>
    <!--  conditional rendering
- conditionally displayoing elements 
based on particular condiiotns  eg conept if...else...else ief -->
  </div>
</template>
<!--  script -->
<script>
export default{
  // porps is tacked with
  // passing data from pparent component to child component
  props:[
    'msg'
  ],
  // data option
  data(){
    return {
      nameOfIndividual:"nameofPerson",
      text:"bree",
      age:0,
      logo:'logoStyle',
      imageOfCar:"",
      imageOfLand:"src/components/navigation/assets/images/land1.jpg"
    }
  },
   methods:{
    /**
     * increment age
     *  - increment by one
     * - check if age has reached 10
     * - if so change image
     */
    increaseAge(){
      this.age++; // incrementd by one
     // toggles between toy car and actual car
     this.toggleImage();
    },

    /**
     * toggle car image
     *
     */
    /**
       * descrea age
       * - reduce age by 1
       */
       descreaseAge(){
        this.age--;
     // toggles between toy car and actual car
     this.toggleImage();
      },

      /**
       * toggle between toy car image and actual car imiage is user is 10yrs and above 21 yrs
       */

       toggleImage(){
         /*
         - check if age is 10 => toy car
         - check if age > 21 => actual car
         * */

         if(this.age=== 10){
        //toy car image
          this.imageOfCar ="https://images.pexels.com/photos/385997/pexels-photo-385997.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1";
         }
        //  else{
        //   this.imageOfCar="https://images.pexels.com/photos/13407918/pexels-photo-13407918.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1";
        //  }

         if(this.age >=21){
          //actual car image
          this.imageOfCar="https://images.pexels.com/photos/762911/pexels-photo-762911.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1";
         }
        //  else{
        //   this.imageOfCar="https://images.pexels.com/photos/165236/pexels-photo-165236.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1";
        //  }

       },



    alterColor(){
      // console.log("alter color clicked ...")
      // this.nameOfIndividual = 'nameClicked'
      // dynamically changing the image above
      this.imageOfLand ="https://images.pexels.com/photos/15953899/pexels-photo-15953899/free-photo-of-in-flight.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1";
    }
   }
}
</script>
<!-- style -->
<style>
button {
  background-color: #696969;
  color: black;
}
#nameClicked {
  color: yellow;
  font-style: bold;
  background-color: black;
  margin-left: 10px;
  font-size: 48px;
}
#nameofPerson {
  color: #0cca9c;
  font-style: bold;
  font-size: 40px;
}
img {
  width: 200px;
  height: 200px;
}
/*  set page margins */
template {
  font-family: "Poppins", sans-serif;
  width: 100vw;
  padding: 0%;
}
body {
  overflow: hidden;
}
.test {
  font-size: 100px;
  color: black;
  font-family: "Courier New", Courier, monospace;
}
/* logo styling  */
.logoStyle {
  margin-top: 48px;
  margin-bottom: 48px;
  font-size: 40px;
  color: #0cca9c;
}

/* styles to handle top navigation */
a {
  margin-left: 10px;
  margin-right: 10px;
  font-size: 24px;
  text-decoration: none;
  cursor: pointer;
  color: #696969;
}
.topNavigationBar {
  display: flex;
  justify-content: space-between;
  margin-left: 200px;
  margin-right: 200px;
}

#routes {
  /* display: flex; */
  margin-top: 55px;
}
#route {
  margin-top: auto;
  margin-bottom: auto;
  color: #696969;
  margin-right: 70px;
  height: fit-content;
  width: fit-content;
  text-decoration: none;
  transition: 0.7s;
  border-bottom: 3px solid #ffffff;
}
#route:hover {
  border-bottom: 3px solid #0cca9c;
}
</style>
