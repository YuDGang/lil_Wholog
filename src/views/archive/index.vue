<template>
  <div class="tcommonBox archive-box">
    <div class="archive-title">归档</div>
    <div class="archive-class-title">分类</div>
    <ul class="archive-class-all">
      <li v-for="item in classList" :key="item.id"><a href="/category">{{item.name}}</a><span>（{{item.count}}）</span></li>
    </ul>
    <div class="article-time" v-for="item in articleList" :key="item.year">
      <div class="archive-class-title">{{item.year}}</div>
      <el-timeline>
        <el-timeline-item v-for="a in item.list" :key="a.id" :hide-timestamp="true">
          <span class="archive-class-item-time">{{a.time}}</span> <a class="archive-class-item-title" :href="'/dispDemo/' + a.name" >{{a.title}}</a>
        </el-timeline-item>
      </el-timeline>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Archive',
  data () {
    return {
      classList: [
        {
          id: 1,
          name: '分享镜',
          count: 8
        },
        {
          id: 2,
          name: '创作集',
          count: 8
        },
        {
          id: 3,
          name: '事件簿',
          count: 89
        },
        {
          id: 4,
          name: '闲言碎语',
          count: 8
        }
      ],
      articleList: [
        {
          year: '2020',
          list: [
            {
              id: 1,
              time: '11-20',
              title:'Macbook',
              name:'macbook'
            },
            {
              id: 2,
              time: '11-15',
              title: '面试题：CSS时钟',
              name: 'clocks',
            },
            {
              id: 3,
              time: '11-01',
              title: '文字搬运工',
              name: 'wordRemove'
            },
            {
              id: 4,
              time: '10-21',
              title: '[精] 看点空投 - 管理平台',
              name:'AirNews-admin'
            },
            {
              id: 5,
              time: '10-15',
              title: '[精] NoStyleMusic 无风格音乐播放器',
              name:'musicAPP'
            },
            {
              id: 6,
              time: '10-06',
              title: '豆瓣网',
              name:'douban'
            },
            {
              id: 7,
              time: '09-02',
              title: '网易严选',
              name: 'netease'
            },
            {
              id: 8,
              time: '08-29',
              title: '购物车',
              name:'dragShoppingcar'
            },
            {
              id: 9,
              time: '08-25',
              title: '豆瓣网',
              name:'douban'
            },
          ]
        },
        {
          year: '2019',
          list: [
            {
              id: 1,
              time: '12-29',
              title: '[精] Finder摄影租赁器材',
              name: 'FinderAPP'
            },
            {
              id: 2,
              time: '12-25',
              title: '实验室项目 - ‘曹操到’家政后台',
              name:'myHouse'
            }
          ]
        }
      ]
    }
  },
  components: {},
  methods: {},
  created () { }
}
</script>

<style scoped lang="less">
.archive-box {
  padding-left: 50px;
  padding-right: 50px;
  .archive-title {
    // color: #444;
    font-size: 25px;
    font-weight: 700;
    text-align: center;
    padding: 30px 0;
  }
  .archive-class-title {
    text-align: left;
    font-size: 22px;
    font-weight: 700;
    margin-bottom: 30px;
  }
  .archive-class-all {
    padding: 0 10px;
    margin-bottom: 40px;
    li {
      display: inline-block;
      padding-right: 20px;
      a {
        color: #ab3300;
        &:hover {
          color: #ff4d00;
        }
      }
      span {
        color: #bbb;
      }
    }
  }
  .article-time {
    margin-bottom: 20px;
  }
}
</style>

<style lang="less">
.archive-box {
  .el-timeline-item__tail {
    border-left: 4px solid rgba(151, 223, 253, 0.1);
    left: 3px;
  }
  .el-timeline-item__wrapper {
    color: #97dffd;
  }
  .el-timeline-item__node {
    background: #97dffd;
    width: 6px;
    height: 6px;
    left: 2px;
  }
  .archive-class-item-time {
    color: #00a7e0;
    font-size: 12px;
    margin-right: 10px;
  }
  .archive-class-item-title {
    font-size: 14px;
    font-weight: 400;
    line-height: inherit;
    color: #444444;
    &:hover {
      color: #222;
    }
  }
}
</style>