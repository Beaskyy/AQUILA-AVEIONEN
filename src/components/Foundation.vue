<template>
  <div>
    <b-container class="bv-example-row">
    <div class="name">
      {{name}}
    </div>



    <b-row>
    <b-col sm="8" offset="2">
      <b-jumbotron class="jumb">
    <b-img class="aveion" src="assets/Aveion.png"></b-img>
      </b-jumbotron>
    </b-col>
  </b-row>
  </b-container>

  <b-img class="aquila" src="assets/Aquila.png"></b-img>
  <ul class="beasky">
    <li>HOME</li>
    <li>ABOUT</li>
    <li style="padding-left:300px;">GALLERY</li>
    <li>CONTACT</li>
  </ul>
  <div class="sci">
  <p><a :href="`https://instagram.com ${social_media.instagram}`"><i class="fa fa-instagram"></i></a></p>
  <p><a :href="`https://twitter.com ${social_media.twitter}`"><i class="fa fa-twitter"></i></a></p>
  <p><a :href="`https://snapchat.com ${social_media.snapchat}`"><i class="fa fa-snapchat"></i></a></p>
  <p><a :href="`https://mail ${social_media.mail}`"><i class="fa fa-envelope"></i></a></p>
  </div>
</div>
</template>


<script>
export default {
  props: {
    name: String,
    social_media: Object
  }
}
</script>
<style scoped>
.jumb {
  margin-top: 40px;
  background: #C82864;
  border-radius: 0px;
  box-shadow: 5px 15px 50px rgba(0,0,0,0.5);
}
.aveion {
  width: 100%;
}
.aquila {
  max-width: 10%;
  height: auto;
  border-radius: 50%;
}
ul{
    position: relative;
    display: flex;
}
ul li
{
  list-style: none;
  justify-content: center;
  letter-spacing: 10px;
  font-size: 20px;
  padding-right: 50px;
}
ul li a
{
    display: inline-block;
    color: #ffffff;
    font-weight: 100;
    margin-left: 40px;
    text-decoration: none;

}
/* ul li {
  color: #ffffff;


} */
.beasky {
  padding-left: 70px;
  margin-top: -50px;
  width: 100%;
  justify-content: center;
  padding-bottom: 40px;
}
p {
  margin-bottom: 50px;
}
i {
  font-size:40px;
  color: #ffffff;
}
.sci
{
  position: absolute;
  top: 120%;
  right: 1px

}
.name {
  padding-top: 40px;
  font-size: 30px;
  letter-spacing: 20px;
  padding-left: 90px;

}

</style>