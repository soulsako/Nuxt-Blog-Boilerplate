<template>
  <div class="home-page">
    <section class='intro'>
      <h1>Get the latest tech news!</h1>
    </section>
    <section class="featured-posts">
      <PostPreview :img="img1" title='Title 1' previewText='Lorem ipsum dolor sit amet.' id='1' />
      <PostPreview :img="img2" title='Title 2' previewText='Lorem ipsudhhd hdhd sit amet.' id='2'/>
    </section>
  </div>
  
</template>

<script>
import PostPreview from '@/components/posts/postPreview'
export default {
  components: {
    PostPreview
  }, 
  data(){
    return {
      img1: 'url("http://www.kiplinger.com/slideshow/investing/T058-S001-10-tech-stocks-to-watch-like-a-hawk-this-spring/images/intro.jpg");',
      img2: 'url("https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQjO66Ilsde8IbxWbxMRQermBW8iq1_vwJQDQkWKsY1yVb5WL0H");', 
    }
  }
}
</script>

<style scoped>

.intro {
  height: 300px;
  position: relative;
  padding: 30px;
  box-sizing: border-box;
  background-position: center;
  background-image: linear-gradient(to right bottom, rgba(204, 204, 204, 0.75), rgba(238, 238, 238, 0.75
  
  )), url('~assets/images/main-page-background.jpg');
  background-size: cover;
}

.intro h1 {
  position: absolute;
  top: 10%;
  left: 5%;
  width: 90%;
  font-size: 1.5rem;
  color: black;
  background-color: rgb(211, 211, 211);
  padding: 10px;
  border-radius: 10px;
  box-shadow: 3px 3px 3px black;
  box-sizing: border-box;
  border: 1px solid black;
}

@media (min-width: 768px) {
  .intro h1 {
    font-size: 2rem;
  }
}

.featured-posts {
  display: flex;
  padding: 20px;
  box-sizing: border-box;
  flex-wrap: wrap;
  align-items: center;
  justify-content: center;
}

</style>
