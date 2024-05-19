<template>
  <div id="app">
    <div class="header">
      <div class="header-main">
        <div class="logoBox"><a class="logo" href="https://www.jiakaobaodian.com/"></a></div>
        <div class="searchBox">
          <input type="text" placeholder="请输入关键词" class="searchInput">
          <input type="submit" value="搜 索" class="searchButton">
        </div>
      </div>
    </div>
    <div class="navigation">
      <ul>
        <li><a href="https://www.jiakaobaodian.com/" class="active">首页</a></li>
        <li class="menu" @mouseenter="showDropDown($event)" @mouseleave="hideDropDown($event)" data-type="mnks"><a href="https://www.jiakaobaodian.com/mnks/">模拟考试 </a> <div class="menu-select" v-show="dropDown === 'mnks'">
          <a href="https://www.jiakaobaodian.com/mnks/kemu1/car.html">科目一</a>
          <a href="https://www.jiakaobaodian.com/mnks/kemu2/car.html">科目二</a>
          <a href="https://www.jiakaobaodian.com/mnks/kemu3/car.html">科目三</a>
          <a href="https://www.jiakaobaodian.com/mnks/kemu4/car.html">科目四</a>
        </div></li>       
        <li class="menu" @mouseenter="showDropDown($event)" @mouseleave="hideDropDown($event)" data-type="school"><a href="https://www.jiakaobaodian.com/school/">找驾校 </a> <div class="menu-select" v-show="dropDown === 'school'">
          <a href="https://www.jiakaobaodian.com/school">找驾校</a>
          <a href="https://www.jiakaobaodian.com/coach">找教练</a>
          <a href="https://www.jiakaobaodian.com/peilian">找陪练</a>
        </div></li>   
        <li><a href="https://www.jiakaobaodian.com/bbs/">驾考圈</a></li>
        <li><a href="https://www.jiakaobaodian.com/sign/">交通标志</a></li>
        <li><a href="https://www.jiakaobaodian.com/download/">软件下载</a></li>
        <li><a href="https://www.jiakaobaodian.com">驾考宝典企业版</a></li>
        <li><a href="https://www.futurephantom.cn/">智慧驾校</a></li>
        <li class="menu" @mouseenter="showDropDown($event)" @mouseleave="hideDropDown($event)" data-type="car"><a href="https://www.maiche.com/rank/?from=jiakao_web">买新车 </a> <div class="menu-select" v-show="dropDown === 'car'">
          <a href="https://www.maiche.com/rank/?from=jiakao_web">买车网</a>
          <a href="http://www.pingxing.cn/">平行之家</a>
        </div></li>
        <li><a href="http://www.xiaozhu2.com/?from=jiakao_web">二手车</a></li>
      </ul>
    </div>
    <div class="banner">
     <div class="swiper-container">
    <div class="swiper-wrapper">
        <div class="swiper-slide"><a href="https://saas-shop.jiakaobaodian.com/runtu/cooperate.html" style="background: url(https://www.jiakaobaodian.com/core-assets/static/images/common/home_banner_download.png)center center no-repeat;"></a></div>
        <div class="swiper-slide"><a href="https://saas-shop.jiakaobaodian.com/runtu/cooperate.html" style="background: url(https://www.jiakaobaodian.com/core-assets/static/images/common/home_banner_jiaolian.jpg)center center no-repeat;"></a></div>
        <div class="swiper-slide"><a href="https://saas-shop.jiakaobaodian.com/runtu/cooperate.html" style="background:url(https://www.jiakaobaodian.com/core-assets/static/images/common/home_banner_download.png)center center no-repeat; "></a></div>
        <div class="swiper-slide"><a href="https://saas-shop.jiakaobaodian.com/runtu/cooperate.html" style="background: url(https://www.jiakaobaodian.com/core-assets/static/images/common/home_banner_new1.jpeg)center center no-repeat;"></a></div>
    </div>
    <div class="swiper-pagination"></div>
     </div>
     <div class="detail-container">
      <div class="banner-detail">
        <p class="detail-title">学车流程</p>
        <ul class="detail-list">
          <li class="icon1">
            <p class="p1"><a href="https://www.jiakaobaodian.com/mnks/kemu1/car.html">科目一</a></p>
            <p class="p2">2024新题库</p>
          </li>
          <li class="icon2">
            <p class="p1"><a href="https://www.jiakaobaodian.com/mnks/kemu2/car.html">科目二</a></p>
            <p class="p2">精选视频，详解考点</p>
          </li>
          <li class="icon3">
            <p class="p1"><a href="https://www.jiakaobaodian.com/mnks/kemu3/car.html">科目三</a></p>
            <p class="p2">全方位讲解，攻克难点</p>
          </li>
          <li class="icon4">
            <p class="p1"><a href="https://www.jiakaobaodian.com/mnks/kemu4/car.html">科目四</a></p>
            <p class="p2">2024新题库</p>
          </li>
        </ul>
      </div>
     </div>
    </div>
    <div class="test">
      <div class="test-title">
        <hr>
        <div class="lilunkaoshi">2024小车理论考试</div>
      </div>
      <div class="test-content">
        <ul class="test-left">
          <li class="item-title">
            <a href="https://www.jiakaobaodian.com/mnks/kemu1/car.html" class="jiaogui">
              科目一交规
            </a>
          </li>
          <li class="item icon1">
            <a href="https://www.jiakaobaodian.com/mnks/exercise/0-car-kemu1.html">顺序练习</a>
            <p>按照顺序练习做题</p>
          </li>
          <li class="item icon2">
            <a href="https://www.jiakaobaodian.com/mnks/exercise/3-car-kemu1.html">随机练习</a>
            <p>按随机顺序做题</p>
          </li>
          <li class="item icon3">
            <a href="https://www.jiakaobaodian.com/mnks/strengthen/car-kemu1.html">专项练习</a>
            <p>分门别类重点突破</p>
          </li>
          <li class="item icon4">
            <a href="https://www.jiakaobaodian.com/mnks/exercise/8-car-kemu1.html">难题攻克</a>
            <p>准确把握考试难点</p>
          </li>
          <li class="item-button">
            <a href="https://www.jiakaobaodian.com/mnks/exam/car-kemu1.html">模拟考试</a>
          </li>
        </ul>
        <ul class="test-right">
          <li class="item-title">
            <a href="https://www.jiakaobaodian.com/mnks/kemu4/car.html" class="jiaogui">
              科目四安全文明驾驶
            </a>
          </li>
          <li class="item icon1">
            <a href="https://www.jiakaobaodian.com/mnks/exercise/0-car-kemu1.html">顺序练习</a>
            <p>按照顺序练习做题</p>
          </li>
          <li class="item icon2">
            <a href="https://www.jiakaobaodian.com/mnks/exercise/3-car-kemu1.html">随机练习</a>
            <p>按随机顺序做题</p>
          </li>
          <li class="item icon3">
            <a href="https://www.jiakaobaodian.com/mnks/strengthen/car-kemu1.html">专项练习</a>
            <p>分门别类重点突破</p>
          </li>
          <li class="item icon4">
            <a href="https://www.jiakaobaodian.com/mnks/exercise/8-car-kemu1.html">难题攻克</a>
            <p>准确把握考试难点</p>
          </li>
          <li class="item-button">
            <a href="https://www.jiakaobaodian.com/mnks/exam/car-kemu1.html">模拟考试</a>
          </li>
        </ul>
      </div>
    </div>
    <div class="ad">
      <a href="https://saas-shop.jiakaobaodian.com/runtu/cooperate.html">
        <img src="https://www.jiakaobaodian.com/core-assets/static/images/common/banner-jxb.png" alt="">
      </a>
    </div>
    <div class="recommend">
      <div class="recommend-title">
        <hr>
        <div class="jiaxiaotuijian">驾校推荐</div>
      </div>
      <div class="recommend-content">
        <ul class="school-list">
          <li>
            <div class="item-top">
              <div class="item1">
                <div class="box1">
                  <span>龙泉驾校</span>
                  <div class="stars">
                    <div class="score1"></div>
                  </div>
                </div>
                <div class="box2">
                  <span>口碑好</span>
                  <span>规模大</span>
                  <span>拿本快</span>
                  <span>包接送</span>
                </div>
              </div>
              <div class="item2">
                <p class="price">￥3480</p>
              </div>
              <div class="item3">
                <button>学车报名</button>
              </div>
            </div>
            <div class="item-bottom">
              <div class="avatar">
                <img src="https://avatar-user.mc-cdn.cn/user-avatar/2024/03/20/09/3725aef96d3e452b8708fb7d519d593d.jpg!100x100" alt="">
              </div>
              <p class="comments">教练态度好，学校环境好，约课方便，有班车接送</p>
            </div>
          </li>
          <li>
            <div class="item-top">
              <div class="item1">
                <div class="box1">
                  <span>公交驾校</span>
                  <div class="stars">
                    <div class="score1"></div>
                  </div>
                </div>
                <div class="box2">
                  <span>口碑好</span>
                  <span>规模大</span>
                  <span>拿本快</span>
                  <span>包接送</span>
                </div>
              </div>
              <div class="item2">
                <p class="price">￥4900</p>
              </div>
              <div class="item3">
                <button>学车报名</button>
              </div>
            </div>
            <div class="item-bottom">
              <div class="avatar">
                <img src="https://avatar-user.mucang.cn/user-avatar/default/XeCvtUX-AE0.jpg!100x100" alt="">
              </div>
              <p class="comments">今天很顺利考完科一，一把过</p>
            </div>
          </li>
          <li>
            <div class="item-top">
              <div class="item1">
                <div class="box1">
                  <span>金菱驾校</span>
                  <div class="stars">
                    <div class="score2"></div>
                  </div>
                </div>
                <div class="box2">
                  <span>口碑好</span>
                  <span>规模大</span>
                  <span>拿本快</span>
                  <span>包接送</span>
                </div>
              </div>
              <div class="item2">
                <p class="price">￥3980</p>
              </div>
              <div class="item3">
                <button>学车报名</button>
              </div>
            </div>
            <div class="item-bottom">
              <div class="avatar">
                <img src="https://avatar-user.mucang.cn/user-avatar/default/DWLYxmRNYe8.jpg!100x100" alt="">
              </div>
              <p class="comments">一人一车，教练挺专业的，各个点位准确，通过率高</p>
            </div>
          </li>
          <li>
            <div class="item-top">
              <div class="item1">
                <div class="box1">
                  <span>嘉安驾校</span>
                  <div class="stars">
                    <div class="score2"></div>
                  </div>
                </div>
                <div class="box2">
                  <span>口碑好</span>
                  <span>规模大</span>
                  <span>拿本快</span>
                  <span>包接送</span>
                </div>
              </div>
              <div class="item2">
                <p class="price">￥4000</p>
              </div>
              <div class="item3">
                <button>学车报名</button>
              </div>
            </div>
            <div class="item-bottom">
              <div class="avatar">
                <img src="https://avatar-user.mucang.cn/user-avatar/default/adK3Vu70DEQ.jpg!100x100" alt="">
              </div>
              <p class="comments">。。。。。。。。
</p>
            </div>
          </li>
        </ul>
        <div class="more">
          <a href="https://www.jiakaobaodian.com/school/">查看更多</a>
        </div>
      </div>
    </div>
    <div class="process">
      <div class="process-title">
        <hr>
        <div class="title-text">学车流程</div>
        <div class="title-text2">驾考宝典整合学车全流程，驾考宝典为用户提供全方位学车服务</div>
      </div>
      <div class="process-content">
        <ul class="process-list">
          <li class="process-item icon1">
            <a href="https://www.jiakaobaodian.com/school/">
              <span>找驾校</span>
              <p>口碑好的驾校</p>
            </a>
          </li>
          <li class="process-item icon2">
            <a href="https://www.jiakaobaodian.com/mnks/kemu1/car.html">
              <span>科目一</span>
              <p>驾驶员理论考试</p>
            </a>
          </li>
          <li class="process-item icon3">
            <a href="https://www.jiakaobaodian.com/mnks/kemu2/car.html">
              <span>科目二</span>
              <p>场地驾驶技能考试科目</p>
            </a>
          </li>
          <li class="process-item icon4">
            <a href="https://www.jiakaobaodian.com/mnks/kemu3/car.html">
              <span>科目三</span>
              <p>机动车驾驶人道路考试</p>
            </a>
          </li>
          <li class="process-item icon5">
            <a href="https://www.jiakaobaodian.com/mnks/kemu4/car.html">
              <span>科目四</span>
              <p>安全文明驾驶常识考试</p>
            </a>
          </li>
          <li class="process-item icon6">
            <a href="#">
              <span>拿本</span>
              <p>开心拿本，安全驾驶</p>
            </a>
          </li>
        </ul>
      </div>
    </div>
    <div class="honor">
      <div class="honor-title">
        <hr>
        <div class="title-text">宝典荣誉</div>
        <div class="title-text2">强大的驾考功能，优秀的用户体验，我们的愿景是学车无忧，轻松拿本</div>
      </div>
      <div class="honor-content">
        <img src="https://www.jiakaobaodian.com/core-assets/static/images/common/home-dynamic.png" alt="">
      </div>
    </div>
    <div class="app">
      <div class="app-content">
        <div class="app1" @mouseenter="expandApp($event)" @mouseleave="shrinkApp($event)" data-type="app1">
          <span>教练宝典APP</span>
          <div v-show="showAppContent === 'app1'"></div>
        </div>
        <div class="app2" @mouseenter="expandApp($event)" @mouseleave="shrinkApp($event)" data-type="app2" >
          <span>驾考宝典APP</span>
          <div v-show="showAppContent === 'app2'"></div>
        </div>
        <div class="app3"  @mouseenter="expandApp($event)" @mouseleave="shrinkApp($event)" data-type="app3" >
          <span>买车宝典APP</span>
          <div v-show="showAppContent === 'app3'"></div>
        </div>
      </div>
    </div>
    <div class="QRcode">
      <div class="code-content">
        <ul class="code-list">
          <li class="code-item">
            <span>驾考宝典APP下载</span>
            <p>考驾照 用宝典</p>
          </li>
          <li class="code-item2">
            <span>驾考宝典微信小程序</span>
            <p>无需下载，驾考做题更方便！</p>
          </li>
        </ul>
      </div>
    </div>
    <div class="sideBar">
      <ul class="side-list">
        <li class="weixin" @mouseenter="showDropDown($event)" @mouseleave="hideDropDown($event)" data-type="weixin" >
          <div class="weixin-box" v-show="dropDown === 'weixin'" ></div>
        </li>
        <li class="weibo"  @mouseenter="showDropDown($event)" @mouseleave="hideDropDown($event)" data-type="weibo">
          <div class="weibo-box" v-show="dropDown === 'weibo'"></div>
        </li>
        <li class="yijian" @mouseenter="showDropDown($event)" @mouseleave="hideDropDown($event)" data-type="yijian">
          <span>意见反馈</span>
          <div class="yijian-box" v-show="dropDown === 'yijian'">
            <ul>
              <li>
                <span class="title">用户反馈</span>
                <div class="content"> 400-056-1617（电话）</div>
              </li>
              <li>
                <span class="title">教练反馈</span>
                <div class="content">jiaolian_service@mucang.cn(邮箱)</div>
              </li>
              <li>
                <span class="title">驾校反馈</span>
                <div class="content">jiaxiao_service@mucang.cn(邮箱)</div>
              </li>
              <li>
                <span class="title">学员反馈</span>
                <a href="#" class="content">点击提交学员反馈</a>
              </li>
            </ul>
          </div>
        </li>
        <li class="backTop" @click="back">
          <span>返回顶部</span>
        </li>
      </ul>
    </div>
    <div class="footer"> 
    </div>
  </div>

  
</template>

<script>
import Swiper from 'swiper';
import 'swiper/css/swiper.min.css'


export default {
  name: "App",
  data() {
    return {
      dropDown: null,
      Interval: null,
      showAppContent: null
    }
  },
  methods: {
    showDropDown(event) {
      const target = event.currentTarget.getAttribute('data-type');
      this.dropDown = target;
    },
    hideDropDown() {
      this.dropDown = null;
    },
    back() {
      let scroll =
        document.body.scrollTop || document.documentElement.scrollTop;

      if (scroll > 100) {
        this.Interval = setInterval(() => {
          document.body.scrollTop =
            document.documentElement.scrollTop =
            scroll -=
              50;
          if (scroll <= 0) {
            clearInterval(this.Interval);
          }
        }, 5);
      }
    },
    expandApp(event) {
      const target = event.currentTarget.getAttribute('data-type');
      this.showAppContent = target;
    },
    shrinkApp() {
    this.showAppContent = null;
  },
  },
  mounted() {
    new Swiper ('.swiper-container', {
    loop: true,  //环路，让Swiper看起来是循环的
    pagination: {
      el: '.swiper-pagination',
      },
    speed: 500,
    freeMode: false,//根据惯性滑动可能不止一格且不会贴合
    observer : true,//修改swiper自己或子元素时，自动初始化swiper 
    autoplay : true,//自动切换 
    autoplay : {
      delay : 2000,//自动切换的时间间隔，单位ms 
      disableOnInteraction : false //用户操作swiper之后，是否禁止autoplay
    },
  })
  },
  destroyed() {
    
  },
}
</script>


<style>
*{
  padding: 0;
  margin: 0;
}

*, .block-item, :after, :before {
  box-sizing: border-box;
}

li,ol,ul{
  list-style: none;
  padding: 0;
  margin: 0;
}

p{
  display: block;
    margin-inline-start: 0px;
    margin-inline-end: 0px;
    unicode-bidi: isolate;
}

li{
  display: list-item;
    text-align: -webkit-match-parent;
    unicode-bidi: isolate;
}

a{
  font-size: inherit;
    color: inherit;
    text-decoration: none;
    cursor: pointer;
}

a,button{
  cursor: pointer;
}

body{
  margin: 0;
    font-size: 14px;
    color: #333;
    line-height: 1.01;
    -webkit-touch-callout: none;
    -webkit-tap-highlight-color: transparent;
    font-family: "Microsoft YaHei", "Hiragino Sans GB", "Hiragino Sans GB W3", "Helvetica Neue", Helvetica, Arial, sans-serif;
}

.header{
  width: 100%;
  height: 70px;
}

.header-main {
  width: 1200px;
  height: 42px;
  overflow: hidden;
  margin: 28px auto;
}

.logoBox{
  float: left;
  width: 210px;
  height: 100%;
  overflow: hidden;
}

.logo{
  display: block;
  width: 207px;
  height: 100%;
  overflow: hidden;
  background: url(/src/assets/img/logo.png) left center no-repeat;
}

.searchBox{
  float: right;
  position: relative;
  width: 300px;
}

.searchInput{
  height: 42px;
  width: 100%;
  line-height: 40px;
  font-size: 14px;
  padding: 0 40px 0 10px;
  border: 1px solid #e9e9e9;
  outline:none
}

.searchInput:focus{
  border: 1px solid #37b5f8;
}

.searchButton:focus{
  border: 1px solid #37b5f8;

}

.searchButton{
  height: 42px;
  width: 100%;
  line-height: 40px;
  border:1px solid #e9e9e9;
  font-size:14px;
  padding: 0 40px 0 10px;
}

.searchButton{
  position: absolute;
  top:0;
  right: 0;
  width: 53px;
}

.navigation{
  width: 100%;
  height: 50px;
  background-color: #37B5F8;
  color:#fff
}

.navigation ul {
  width: 1200px;
  height: 50px;
  line-height: 50px;
  margin: auto;
  font-size: 16px;
  text-align: left;
}
.navigation ul li {
  display: inline-block;
  width: 108px;
  text-align: center;
  padding: 0;
  vertical-align: top;
}

.active{
  background-color: #258FC7;
}

.navigation ul li a {
  display: block;
  width: 100%;
  height: 100%;
  text-decoration: none;
  font-size: inherit;
  color:inherit;
  cursor: pointer;
}

.menu{
  position: relative;
  overflow:visible;
}

.menu ::after{
  display: inline-block;
  width: 10px;
  height: 10px;
  margin-left: 6px;
  margin-top: 5px;
  vertical-align: middle;
  border: 5px solid transparent;
  border-top: 5px solid #fff;
  content: ' ';
}
.menu-select{
  position: absolute;
  top: 50px;
  width: 100%;
  background-color: #fff;
  z-index:2;
  line-height: 40px;
  font-size: 14px;
  padding: 0 8px;
  color:#666;
  box-shadow: 0 0 20px rgba(0, 0, 0, .1);;
}

.navigation ul li a:hover{
  background-color:rgba(244, 241, 241, 0.2);
}

.menu-select a{
  width: 100%;
  height: 100%;
  display: block;
  padding: 0px;
  text-align: center;
  border-bottom: 1px solid #f6f6f6;
}

.menu-select a:last-child{
  border-bottom: none;
}

.menu-select::after{
  display: none !important; 
}

.menu-select a::after{
  display: none;
}

.menu-select a:hover{
  color:#37b5f8
}

.swiper-container{
  width: 100%;
  height: 380px;
}

.swiper-slide a {
  display: inline-block;
  width: 100%;
  height: 380px;
}

.detail-container {
  position: relative;
  width: 1200px;
  height: 0;
  margin: 0 auto;
  overflow: visible;
}

.detail-container .banner-detail{
  width: 280px;
  position: absolute;
  top: -358px;
  left: 0;
  z-index: 1;
  padding: 0 20px;
  background-color: rgba(255,255,255,.9);
}



.banner-detail .detail-title {
  line-height: 50px;
  font-size: 20px;
  border-bottom: 1px dotted #ddd;
  text-align: center;
}

.detail-list .icon1{
background: url(https://www.jiakaobaodian.com/core-assets/jiakao/application/home/files/5061edda4ba913bd8f1ca5bdaee8d1d7.png) left center no-repeat;
}

.detail-list li {
  padding: 18px 20px 18px 50px
}

.p1{
  font-size:16px;
  color:#37B5F8 !important;
}

.detail-list li .p2{
  margin-top: 5px;
  color:#666;
}


.detail-list .icon2{
  background: url(https://www.jiakaobaodian.com/core-assets/jiakao/application/home/files/9bfc61e92388bf9d0521dbbc5497172b.png) left center no-repeat;
}

.detail-list .icon3{
  background: url(https://www.jiakaobaodian.com/core-assets/jiakao/application/home/files/5061edda4ba913bd8f1ca5bdaee8d1d7.png) left center no-repeat;
}

.detail-list .icon4{
  background: url(https://www.jiakaobaodian.com/core-assets/jiakao/application/home/files/ef73328f70c08beb91f54eae709a05b1.png) left center no-repeat;
}


.test{
  width: 1200px;
  margin: 60px auto;
}

.test-title{
  padding-top: 20px;
  margin-bottom: 40px;
  text-align: center;
}

.test-title hr {
  height: 1px;
  border: none;
  border-top: 1px dotted #e9e9e9;
}

.lilunkaoshi{
  display: inline-block;
  font-size: 30px;
  margin-top: -20px;
  padding: 0 45px;
  line-height: 41px;
  background-color: #fff;
}

.test-left{
  width: 580px;
  float: left;
  border: 1px solid #e9e9e9;
}

.item-title{
  width: 100%;
  float: right;
  height: 110px;
  line-height: 110px;
  padding-top: 0;
  border: none;
  margin: 0;
  text-align: center;
}


.item-title .jiaogui {
  padding: 0 0 0 38px;
}

.jiaogui{
  display: inline-block;
  background: url(https://www.jiakaobaodian.com/core-assets/jiakao/application/home/files/cd9c3b69a1d8d0bc72b839ebdaeb5fd4.png) left center no-repeat;
  font-size: 20px;
  padding: 10px,0,10px,38px;
}

.test-content{
  height: 373px;
}

.test-content a:hover{
  color: #37B5F8;
}

li.item{
  float: left;
  width: 250px;
  height: 70px;
  line-height: 20px;
  margin: 15px  15px;
  padding: 15px 0 15px 85px;
  background-color: #FAFAFA;
}

.icon1{
  background: url(https://www.jiakaobaodian.com/core-assets/jiakao/application/home/files/7920c46acf795cfe91990d3bb8c8635c.png) left 50px center no-repeat;
}

.icon2{
  background: url(https://www.jiakaobaodian.com/core-assets/jiakao/application/home/files/29f60eac40621dffb37c38f8d584f215.png) left 50px center no-repeat;
}

.icon3{
  background: url(https://www.jiakaobaodian.com/core-assets/jiakao/application/home/files/cd9c3b69a1d8d0bc72b839ebdaeb5fd4.png) left 50px center no-repeat;
}

.icon4{
  background: url(https://www.jiakaobaodian.com/core-assets/jiakao/application/home/files/f117d8ae0fca3bffd25ff4511664e607.png) left 50px center no-repeat;
}

.item p {
  font-size: 16px;
  color:#999
}


.item-button{
  width: 100%;
  float: right;
  height: auto;
  line-height: 70px;
  padding-top: 0;
  border: none;
  margin: 0;
  text-align: center;
}


.item-button a{
  width: 300px;
  margin: 15px auto 30px;
  border: none;
  display: block;
  height: 46px;
  line-height: 44px;
  background: #37B5F8;
  color: #fff;
  border-radius: 4px;
  font-size: 16px;
}

.item-button a:hover{
  color:#fff
}


.test-right {
  width: 580px;
  float: right;
  border: 1px solid #e9e9e9;
}


#app .ad {
  margin-top: 30px;
}

.ad {
  width: 1200px;
  height: 120px;
  margin:60px auto;
}

.ad a{
  display: inline-block;
  height: 120px;
}


.recommend{
  width: 1200px;
  margin: 60px auto;
}

.recommend-title{
  margin-bottom: 40px;
  text-align: center;
  padding-top: 20px;
}

.jiaxiaotuijian{
  display: inline-block;
  margin-top: -20px;
  line-height: 41px;
  padding: 0 45px;
  background-color: #fff;
  font-size: 30px;
}

.recommend-title hr {
  height: 1px;
  border: none;
  border-top: 1px dotted #e9e9e9;
}

.recommend-content {
  margin: 0 auto;
}

.school-list{
  height: 570px;
  margin: -30px 0 0 -30px;
  color: #666;
  font-size: 14px;
}

.school-list li {
  position: relative;
  float: left;
  width: 585px;
  margin: 30px 0 0 30px;
  padding: 40px 30px;
  border: 1px solid #e9e9e9;
}

.item-top{
  width: 523px;
  height: 63px;
}

.item1{
  float: left;
  width: 305px;
  line-height: 30px;
}

.box1 span {
  max-width: 180px;
  display: inline-block;
  vertical-align: middle;
  font-size: 22px;
  overflow: hidden;
  white-space: nowrap;
  text-overflow: ellipsis;
}

.stars{
  width: 90px;
  height: 20px;
  display: inline-block;
  vertical-align: middle;
  margin: -3px 0 0 10px;
  background: url(https://www.jiakaobaodian.com/core-assets/jiakao/application/home/files/109f4167a600727d6976ae03c64a5560.png) left center no-repeat;
}

.stars .score1{
  width: 84%;
  height: 100%;
  background: url(https://www.jiakaobaodian.com/core-assets/jiakao/application/home/files/26170a2c1308047cbc25d47cc860cd1e.png) left center no-repeat;
}
.stars .score2{
  width: 92%;
  height: 100%;
  background: url(https://www.jiakaobaodian.com/core-assets/jiakao/application/home/files/26170a2c1308047cbc25d47cc860cd1e.png) left center no-repeat;
}

.box2 {
  margin-top: 10px;
  line-height: 20px;
}

.box2 span {
  display: inline-block;
  background: url(https://www.jiakaobaodian.com/core-assets/jiakao/application/home/files/24bc3d8a827f32b86d0ed191681125f9.png) left center no-repeat;
  padding-left: 20px;
  margin-left: 5px;
}

.item2{
  float: left;
  width: 130px;
  line-height: 63px;
  border-left: 1px solid #e9e9e9;
  font-size: 30px;
  text-align: center;
}
.price {
  color:#ee4653
}

.item3{
  float: right;
}

.item3 button{
  width: 80px;
  line-height: 28px;
  margin-top: 17px;
  text-align: center;
  font-size: 14px;
  border-radius: 4px;
  border: 1px solid #e9e9e9;
  background: 0 0;
  outline: 0;
}

.item-bottom{
  height: 80px;
  margin-top: 30px;
  padding: 20px;
  background: #FAFAFA;
  color: #999;
}

.item-bottom .avatar{
  float: left;
  width: 40px;
  height: 40px;
  border-radius: 50%;
}

.avatar img {
  display: block;
  width: 40px;
  height: 40px;
}

.comments{
  height: 40px;
  line-height: 20px;
  margin-left: 60px;
  display: -webkit-box;
  overflow: hidden;
  text-overflow: ellipsis;
}


.more {
  margin-top: 40px;
}

.more a {
  display: block;
  width: 280px;
  height: 50px;
  margin: 20px auto 0;
  line-height: 48px;
  border: 1px solid #e9e9e9;
  border-radius: 4px;
  color: #999;
  text-align: center;
  font-size: 16px;
}

.process{
  width: 1200px;
  margin: 60px auto;
}

.process-title{
  margin-bottom: 40px;
  text-align: center;
  padding-top: 20px;
}

.process-title hr {
  height: 1px;
  border: none;
  border-top: 1px dotted #e9e9e9;
}

.process-title .title-text{
  display: inline-block;
  margin-top: -20px;
  line-height: 41px;
  padding: 0 45px;
  background-color: #fff;
  font-size: 30px;
}

.title-text2{
  font-size: 16px;
  margin: 30px 0;
  color: #666;
}

.process-content{
  text-align: center;
  height: 224px;
}

.process-list{
  margin: 0 -40px;
}

.process-list .icon1{
background: url(https://www.jiakaobaodian.com/core-assets/jiakao/application/home/files/0fc72e66088099891c2317a3e1da2b34.png) center top no-repeat;
}

.process-item{
  float: left;
  width: 16.6%;
  line-height: 1.4;
}

.process-item a {
  display: block;
  padding: 150px 40px 0;
}

.process-item span{
  display: block;
  font-size: 24px;
}

.process-item p {
  color: #999;
  margin: 10px -20px;
}

.process-list .icon2{
background: url(https://www.jiakaobaodian.com/core-assets/jiakao/application/home/files/ea7968d83db78dd84782f5fb7cdb0ba4.png) center top no-repeat;
}

.process-list .icon3{
background: url(https://www.jiakaobaodian.com/core-assets/jiakao/application/home/files/1a6197c837b9e484084f9fe1b15c08fe.png) center top no-repeat;
}

.process-list .icon4{
background: url(https://www.jiakaobaodian.com/core-assets/jiakao/application/home/files/8df30d2c3be0257c8acd81369e739479.png) center top no-repeat;
}

.process-list .icon5{
background: url(https://www.jiakaobaodian.com/core-assets/jiakao/application/home/files/e63aa9a32b7a40551616e7f01654ec3e.png) center top no-repeat;
}

.process-list .icon6{
background: url(https://www.jiakaobaodian.com/core-assets/jiakao/application/home/files/eb7d98a204cd7957135b8c131b0011a1.png) center top no-repeat;
}

.process-item a:hover{
  color:#37B5F8
}


.honor{
  width: 1200px;
  margin: 60px auto;
}

.honor-title{
  margin-bottom: 40px;
  text-align: center;
  padding-top: 20px;
}

.honor-title hr {
  height: 1px;
  border: none;
  border-top: 1px dotted #e9e9e9;
}

.honor-title .title-text{
  display: inline-block;
  margin-top: -20px;
  line-height: 41px;
  padding: 0 45px;
  background-color: #fff;
  font-size: 30px;
}


.honor-title .title-text2{
  font-size: 16px;
  margin: 30px 0;
  color: #666;
}

.honor-content{
  height: 211px;
  text-align: center;
}

.honor-content img {
  display: block;
}


.app{
  background-color: #f5f5f5;
}

.app-content{
  position: relative;
  width: 1200px;
  height: 560px;
  margin: 70px auto 0;
  overflow: hidden;
}

.app-content div {
  position: absolute;
  bottom: -40px;
  text-align: center;
}

.app1{
  position: absolute;
  bottom: -40px;
  left: 30px;
  text-align: center;
  width: 300px;
  height: 500px;
  background: url(https://www.jiakaobaodian.com/core-assets/jiakao/application/home/files/f4b3be31a83c5d02bf5cb2e0fb11636b.png) center bottom no-repeat;
  transition: bottom 0.3s;
}

.app1:hover {
  bottom: -20px;
}

.app span {
  font-size: 20px;
}

.app1 div {
  /* display: none; */
  width: 100%;
  height: 100%;
  margin-top: 37px;
  background: url(https://www.jiakaobaodian.com/core-assets/jiakao/application/home/files/2d1920df784226626de9efd062e808a2.png) center no-repeat;
  transition: height 0.3s;
}

.app1 div:hover{
  height: 520px;
}

.app2{
  position: absolute;
  bottom: -40px;
  text-align: center;
  left: 400px;
  width: 430px;
  height: 540px;
  background: url(https://www.jiakaobaodian.com/core-assets/jiakao/application/home/files/48726c2bb302051522dfc028c0532488.png) center bottom no-repeat;
  transition: bottom 0.3s;
}

.app2:hover {
  bottom: -20px;
}

.app2 div {
  /* display: none; */
  width: 100%;
  height: 100%;
  margin-top: 52px;
  background: url(https://www.jiakaobaodian.com/core-assets/jiakao/application/home/files/47b4a64f54ae7eaace0daaf9dc3446c5.png) center no-repeat;
  background-color: rgba(255, 255, 255, .5);
  background-size: 150px 150px;
  transition: height 0.3s;
}

.app2 div:hover{
  height: 520px;
}

.app3 {
  left: 905px;
  width: 265px;
  height: 428px;
  background: url(https://www.jiakaobaodian.com/core-assets/jiakao/application/home/files/40ab1d6a3ed0757b51ad19cbec3b29c4.png)center bottom no-repeat;
  transition: bottom 0.3s;
}

.app3:hover {
  bottom: -20px;
}

.app3 div {
  /* display: none; */
  width: 100%;
  height: 100%;
  margin-top: 37px;
  background: url(https://www.jiakaobaodian.com/core-assets/jiakao/application/home/files/188c7ffa5035c0976ff6e06a1ca89666.png) center no-repeat;
  transition: height 0.3s;
}

.app3 div:hover{
  height: 520px;
}

.QRcode{
  width: 1200px;
  height: 178px;
  margin: 60px auto;
}

.code-list .code-item {
  float: left;
  width: 600px;
  line-height: 1.7;
  margin: 20px 0;
  padding: 40px 80px;
  background: url(https://www.jiakaobaodian.com/core-assets/jiakao/application/home/files/dd59a20c70d3f6ed409efc01c65ad14d.png) right 80px center no-repeat;
  background-size: 140px;
  border-right: 1px solid #e9e9e9;
}

.code-item span {
  font-size: 20px;
}

.code-item p {
  color:#999
}

.code-item2{
  float: right;
  background: url(https://www.jiakaobaodian.com/core-assets/jiakao/application/home/files/9e699ddb2a6e87f8fbe90aa6b1d01564.jpg) right 80px center no-repeat;
  background-size: 130px;
  border: none;
  width: 600px;
  line-height: 1.7;
  margin: 20px 0;
  padding: 40px 80px;
}

.code-item2 span{
  font-size: 20px;
}

.code-item2 p{
  color:#999
}

.sideBar{
  position: fixed;
  right: 0;
  bottom: 102px;
  z-index: 2;
  width: 117px;
  min-height: 258px;
  background: url(https://www.jiakaobaodian.com/core-assets/jiakao/application/home/files/ddf1aabca9786f509b6d60d167fb0111.png) center top no-repeat;
}

.side-list {
  position: relative;
  margin-top: 158px;
  border: 1px solid #e6e6e6;
  border-top: none;
  color: #999;
  font-size: 12px;
}


.sideBar ul li {
  height: 33px;
  line-height: 33px;
  cursor: pointer;
}

.weixin .weixin-box{
  display: block;
  position: absolute;
  width: 179px;
  height: 195px;
  top: 25px;
  left: -180px;
  background: url(https://www.jiakaobaodian.com/core-assets/jiakao/application/home/files/c4f622fc933083fa8d224db497037fb1.png) center no-repeat;
}

.weibo .weibo-box{
  display: block;
  position: absolute;
  width: 179px;
  height: 195px;
  top: 62px;
  left: -180px;
  background: url(https://www.jiakaobaodian.com/core-assets/jiakao/application/home/files/8323b7c6a07700c0ea220e49fe814870.png) center no-repeat;
}

.yijian {
  padding-left: 45px;
  background: url(https://www.jiakaobaodian.com/core-assets/jiakao/application/home/files/eec2e6d69f66cc4dd0dc9cb962cc7eea.png) left 15px center no-repeat #fff;
  background-size: 20px;
  border-bottom: 1px solid #e6e6e6;
}

.yijian-box{
  display: block;
  position: absolute;
  top: -65px;
  left: -165px;
  width: 170px;
  height: 280px;
  cursor: default;
  text-indent: 0;
}

.sideBar .yijian-box ul {
  margin-right: 10px;
  padding: 5px 15px;
  border: 1px solid #eee;
  background-color: #fff;
}

.yijian-box ul li {
  text-align: left;
  padding: 8px 0;
  height: 70px;
}

.yijian-box ul li .title{
  display: block;
  line-height: 1.4;
  font-size: 15px;
  color: #000;
}

.yijian-box ul li .content{
  height: 33px;
  font-size: 12px;
  color: #999;
  line-height: 1.4;
  word-wrap: break-word;
}

.yijian-box ul li a.content{
  display: block;
  color: #00f;
  font-size: 12px;
  line-height: 1.4;
  word-wrap: break-word;
}

.footer{
  height: 400px;
  background: #222;
  margin-top: 60px;
}
.backTop{
  padding-left: 45px;
  background: url(https://www.jiakaobaodian.com/core-assets/jiakao/application/home/files/5b170b68eb9edd74ba8cc3d82a945302.png) left 15px center no-repeat #fff;
  color: #333;
}
</style>
