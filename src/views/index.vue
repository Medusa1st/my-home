<template>
  <div class="cp-home">
    <div class="title">{{title}}</div>
    <div class="links">
      <div id="link-to-resume" class="link-to">
        <a v-bind:href="resumeLink">{{resumeTitle}}</a>
      </div>
      <div id="link-to-blog" class="link-to">
        <a v-bind:href="blogLink">{{blogTitle}}</a>
      </div>
      <div id="link-to-works" class="link-to">
        <a v-bind:href="worksLink">{{worksTitle}}</a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'cp-home',
  data () {
    return {
      title: '美杜鲨的个人网站',
      resumeTitle: '我的简历',
      resumeLink: 'http://medusa1st.me/resume/',
      blogTitle: '我的博客',
      blogLink: 'http://www.cnblogs.com/medusa1st/',
      worksTitle: '我的作品',
      worksLink: 'http://medusa1st.me/works/'
    }
  },
  mounted(){
    document.querySelector('body').style.backgroundImage = 'url(http://medusa1st.me/images/bg-sunny-' + parseInt(Math.random()*3 +1) + '.jpg)';
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.cp-home{
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  -o-user-select: none;
  user-select: none;
  max-width: 500px;
  max-height: 100px;
  margin: 0 auto;
  position: absolute;top:0;left:0;bottom:0;right:0;margin:auto;
}
.title{
  font-size: 20px;
  color: #fff;
  margin-bottom: 15px;
}
.links{
  display: flex;
  justify-content: center;
}
.link-to{
  width: 150px;
  background-color: rgba(0,0,0,0.2);
  border-radius: 8px;
  padding: 10px 0;
  margin: 0 15px;
}
.link-to:hover{
  background-color: rgba(0,0,0,0.5);
  transition: background-color 0.25s ease;
  
}
a{
  font-size: 16px;
  color: #fff;
  text-decoration: none;
}
a:hover{
  text-decoration: underline;
}
</style>
