<template>
  <div @click="clickHandle">
    
    
    <i-grid i-class="no-border">
    <i-grid-item i-class="no-border">
        <i-grid-icon>
            <image src="/static/grid/1.png" />
        </i-grid-icon>
        <i-grid-label>观景</i-grid-label>
    </i-grid-item>
    <i-grid-item i-class="no-border">
        <i-grid-icon>
            <image src="/static/grid/2.png" />
        </i-grid-icon>
        <i-grid-label>分享</i-grid-label>
    </i-grid-item>
    <i-grid-item i-class="no-border">
        <i-grid-icon>
            <image src="/static/grid/3.png" />
        </i-grid-icon>
        <i-grid-label>客服</i-grid-label>
    </i-grid-item>
</i-grid>
    <i-grid i-class="no-border">
    <i-grid-item i-class="no-border">
        <i-grid-icon>
            <image src="/static/grid/4.png" />
        </i-grid-icon>
        <i-grid-label>查找</i-grid-label>
    </i-grid-item>
    <i-grid-item i-class="no-border">
        <i-grid-icon>
            <image src="/static/grid/5.png" />
        </i-grid-icon>
        <i-grid-label>资讯</i-grid-label>
    </i-grid-item>
    <i-grid-item i-class="no-border">
        <i-grid-icon>
            <image src="/static/grid/6.png" />
        </i-grid-icon>
        <i-grid-label>消息</i-grid-label>
    </i-grid-item>
</i-grid>
<i-notice-bar icon="systemprompt" loop>
    在这里，与我们一起分享你的经历，你所见过的风景
    </i-notice-bar>
    <i-panel title="用户分享">
      <view class="top-padding">
      <i-card title="我曾经遇到过的风景" extra="编辑推荐" thumb="http://img1.imgtn.bdimg.com/it/u=2735633715,2749454924&fm=26&gp=0.jpg">
        <view slot="content">好多不错的风景</view>
        <view slot="footer">长白山</view>
      
      
      
      </i-card>
      <view class="top-padding"></view>
      <i-card title="用户分享" i-class="top-padding" extra="编辑推荐" thumb="http://img.sccnn.com/bimg/337/23662.jpg">
        <view slot="content">内容不错</view>
        <view slot="footer">尾部内容</view>
      </i-card>
      <view class="top-padding"></view>
    </view>
    </i-panel>
  </div>
</template>

<script>
import card from '@/components/card'

export default {
  data () {
    return {
      motto: 'Hello miniprograme',
      userInfo: {
        nickName: 'mpvue',
        avatarUrl: 'http://mpvue.com/assets/logo.png'
      }
    }
  },

  components: {
    card
  },

  methods: {
    bindViewTap () {
      const url = '../logs/main'
      if (mpvuePlatform === 'wx') {
        mpvue.switchTab({ url })
      } else {
        mpvue.navigateTo({ url })
      }
    },
    clickHandle (ev) {
      console.log('clickHandle:', ev)
      // throw {message: 'custom test'}
    }
  },

  created () {
    // let app = getApp()
  }
}
</script>

<style scoped>
div >>> .no-border {
  border-width: 0pt;
}
.top-padding {
  padding-top: 50rpx;
}
.userinfo {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.userinfo-avatar {
  width: 128rpx;
  height: 128rpx;
  margin: 20rpx;
  border-radius: 50%;
}

.userinfo-nickname {
  color: #aaa;
}

.usermotto {
  margin-top: 150px;
}

.form-control {
  display: block;
  padding: 0 12px;
  margin-bottom: 5px;
  border: 1px solid #ccc;
}
.all{
  width:7.5rem;
  height:1rem;
  background-color:blue;
}
.all:after{
  display:block;
  content:'';
  clear:both;
}
.left{
  float:left;
  width:3rem;
  height:1rem;
  background-color:red;
}

.right{
  float:left;
  width:4.5rem;
  height:1rem;
  background-color:green;
}
</style>
