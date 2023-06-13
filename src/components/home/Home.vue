<!-- template -->
<template>
    <!--  top navigatoin -->
    <div>
        <Navigation :msg="'Welcome to my ticketing App'"/>
    </div>
    <!-- center section -->
    <!--  footer -->
</template>
    
<!-- script -->
<script>
// impormt the cpomponents

import Navigation from '../navigation/Navigation.vue'

//  build the option object  
/**
 * 
 * export default{
 * }
 */
export default {
    components:{
        Navigation
    }
}
</script>

<!-- style -->
<style>
/*  styling the centerSEction
 */
#centerSection {

  margin-left: 200px;
  margin-right: 200px;
  display: flex;
}

#imageSection {
  width: 50%;
}

#descriptionSection {
  width: 50%;
  height: 100%;
  margin-top: auto;
  margin-bottom: auto;
}

/* homepage image styling */
#homePageImage {
  width: 80%;
  height: 600px;
  object-fit: cover;
  border-radius: 30px;
}

/*  title for description section */
#title {
  font-size: 48px;
  font-weight: bold;
  text-align: start;
}
#description {
  font-size: 20px;
  text-align: start;
  color: #A1A1A3;
  line-height: 200%;
}

/*  button styling   */
#buyTicketButton {
  background-color: black;
  color: white;
  font-weight: bold;
  font-size: 20px;
  width: fit-content;
  padding-right: 40px;
  padding-left: 40px;
  padding-top: 14px;
  padding-bottom: 14px;
  border-radius: 40px;
}
/* using pseudo selector */
#buyTicketButton:hover {
    background-color: #0CCA9C;
    color: black;
    cursor: pointer;
}

/* footer  */
footer{
    background-color: #0CCA9C;
    margin-top: 65px;
    width: 100%;
    height: 100rem;
    border-top: 15px solid black;
}

article{
    background-color: crimson;
}</style>