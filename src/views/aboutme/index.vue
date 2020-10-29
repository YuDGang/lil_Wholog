<!-- 关于我 -->
<template>
  <div class="aboutmeBox">
    <div class="tcommonBox">
      <div class="aboutme-title">
            关于我
      </div>
      <section class="aboutme-content">
        <p class="">
          <img src="./../../assets/img/maoto.png" alt="" class="aboutmeImg">
        </p>
        <p class="aboutme-description">
          欢迎来到lil_Wholog，学前端，做剪辑，聊数码，谈美化
        </p>
        <p class="aboutme-description">
          99年出生，年轻有为😍前端小萌新，
        </p>
        <p class="aboutme-description">
          <!-- 爱美食，爱动手做美食，想长胖的尽管来。 -->
        </p>
        <p class="aboutme-description">
          博客fork自aimme学姐，2020年10月20日更新到Vue
        </p>
      </section>
    </div>
    <Message />
  </div>
</template>

<script>
import Message from './../../components/message/index'
export default {
  data () { //选项 / 数据
    return {

    }
  },
  methods: { //事件处理器

  },
  components: { //定义组件
    Message
  },
  created () { //生命周期函数

  }
}
</script>

<style scoped lang="less">
.aboutmeBox{
  .aboutme-title{
    font-size: 25px;
    font-weight: 700;
    text-align: center;
    padding: 30px 0;
  }
  .aboutmeImg {
    max-width: 100%;
    /*height:300px;*/
  }
  .aboutme-description{
    font-size: 15px;
    line-height: 25px;
    padding: 10px 30px;
  }
}


</style>
