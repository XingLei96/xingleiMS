<template>
  <div class="box">
    <div class="header animated" :class="navFlag ? 'fadeInDown' : 'slideOutUp'">
      <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
        <img class="logo" src="../assets/logo.png" alt="" />
        <button
          class="navbar-toggler"
          type="button"
          data-toggle="collapse"
          data-target="#navbarSupportedContent"
        >
          <span class="navbar-toggler-icon"></span>
        </button>
        <div
          class="collapse navbar-collapse justify-content-end"
          id="navbarSupportedContent"
        >
          <ul class="navbar-nav" id="headerNav">
            <li class="nav-item" id="navMainPage">
              <span class="nav-link">{{ $t("header.aboutUs") }}</span>
            </li>
            <li class="nav-item" id="navTechPage">
              <span class="nav-link">{{ $t("header.ourProducts") }}</span>
            </li>
            <li class="nav-item" id="navFoodPage">
              <span class="nav-link">{{ $t("header.news") }}</span>
            </li>
            <li class="nav-item" id="navPhotoPage">
              <span class="nav-link">{{ $t("header.CorporateSocial") }}</span>
            </li>
            <li class="nav-item" id="navEssayPage">
              <span class="nav-link">{{ $t("header.joinUs") }}</span>
            </li>
          </ul>
        </div>
      </nav>
    </div>
    <div class="banners">
      <div class="block">
        <el-carousel
          trigger="click"
          :width="clientWidth + 'px'"
          :height="clientHeight + 'px'"
          :autoplay="true"
        >
          <el-carousel-item v-for="item in banner" :key="item.index">
            <img :src="item" alt="" />
          </el-carousel-item>
        </el-carousel>
        <div class="tit">
          <p>{{ $t("slogan.mission") }}</p>
          <h1>{{ $t("slogan.mission1") }}</h1>
          <h1>{{ $t("slogan.mission2") }}</h1>
        </div>
      </div>
    </div>
    <div class="txtbanner">
      <div class="row">
        <div class="col align-self-center">
          <div class="swiper-container">
            <div class="parallax-bg" data-swiper-parallax="-23%"></div>
            <div class="swiper-wrapper">
              <div class="swiper-slide">
                <div class="title" data-swiper-parallax="-100">
                  {{ $t("bannerTxt.title1") }}
                </div>
                <div class="subtitle" data-swiper-parallax="-200"></div>
                <div class="text" data-swiper-parallax="-300">
                  <p>
                    {{ $t("bannerTxt.content1") }}
                  </p>
                </div>
              </div>
              <div class="swiper-slide">
                <div class="title" data-swiper-parallax="-100">
                  {{ $t("bannerTxt.title2") }}
                </div>
                <div class="subtitle" data-swiper-parallax="-200"></div>
                <div class="text" data-swiper-parallax="-300">
                  <p>
                    {{ $t("bannerTxt.content2") }}
                  </p>
                </div>
              </div>
              <div class="swiper-slide">
                <div class="title" data-swiper-parallax="-100">
                  {{ $t("bannerTxt.title3") }}
                </div>
                <div class="subtitle" data-swiper-parallax="-200"></div>
                <div class="text" data-swiper-parallax="-300">
                  <p>
                    {{ $t("bannerTxt.content3") }}
                  </p>
                </div>
              </div>
            </div>
            <div class="swiper-pagination swiper-pagination-white"></div>
          </div>
        </div>
      </div>
    </div>
    <div class="boxLR">
      <div class="row">
        <div class="col op">
          <div class="left">
            <h2>{{ $t("boxLR.title1") }}</h2>
            <h5>
              {{ $t("boxLR.content1") }}
            </h5>
            <button type="button" class="btn btn-outline-light">
              {{ $t("boxLR.btn") }}
            </button>
            <p class="next">{{ $t("boxLR.more1") }} >></p>
          </div>
        </div>
        <div class="col">
          <div class="right1">
            <div class="card text-center ol">
              <div class="card-body">
                <h2 class="card-title">{{ $t("boxLR.title1") }}</h2>
                <h5 class="card-text">
                  {{ $t("boxLR.content1") }}
                </h5>
                <button type="button" class="btn btn-outline-light">
                  {{ $t("boxLR.btn") }}
                </button>
                <p class="next">{{ $t("boxLR.more1") }}</p>
              </div>
            </div>
          </div>
        </div>
      </div>

      <div class="row">
        <div class="col">
          <div class="right2">
            <div class="card text-center ol">
              <div class="card-body">
                <h2 class="card-title">{{ $t("boxLR.title2") }}</h2>
                <h5 class="card-text">
                  {{ $t("boxLR.content2") }}
                </h5>
                <button type="button" class="btn btn-outline-light">
                  {{ $t("boxLR.btn") }}
                </button>
              </div>
            </div>
          </div>
        </div>
        <div class="col op">
          <div class="left">
            <h2>{{ $t("boxLR.title2") }}</h2>
            <h5>{{ $t("boxLR.content2") }}</h5>
            <button type="button" class="btn btn-outline-light">
              {{ $t("boxLR.btn") }}
            </button>
          </div>
        </div>
      </div>

      <div class="row">
        <div class="col op">
          <div class="left">
            <h2>{{ $t("boxLR.title3") }}</h2>
            <h5>
              {{ $t("boxLR.content3") }}
            </h5>
            <button type="button" class="btn btn-outline-light">
              {{ $t("boxLR.btn") }}
            </button>
          </div>
        </div>
        <div class="col">
          <div class="right3">
            <div class="card text-center ol">
              <div class="card-body">
                <h2 class="card-title">{{ $t("boxLR.title3") }}</h2>
                <h5 class="card-text">
                  {{ $t("boxLR.content3") }}
                </h5>
                <button type="button" class="btn btn-outline-light">
                  {{ $t("boxLR.btn") }}
                </button>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="cards">
      <div class="row d-flex justify-content-around">
        <div class="col">
          <div class="card text-center">
            <img
              class="card-img-top"
              src="../assets/imgs/4.jpg"
              alt="Card image cap"
            />
            <div class="card-body">
              <h5 class="card-title">{{ $t("cards.title1") }}</h5>
              <p class="card-text">
                {{ $t("cards.content1") }}
              </p>
              <button type="button" class="btn">{{ $t("cards.btn") }}</button>
            </div>
          </div>
        </div>

        <div class="col">
          <div class="card text-center">
            <img
              class="card-img-top"
              src="../assets/imgs/5.jpg"
              alt="Card image cap"
            />
            <div class="card-body">
              <h5 class="card-title">{{ $t("cards.title2") }}</h5>
              <p class="card-text">
                {{ $t("cards.content2") }}
              </p>
              <button type="button" class="btn">{{ $t("cards.btn") }}</button>
            </div>
          </div>
        </div>
        <div class="col">
          <div class="card text-center">
            <img
              class="card-img-top"
              src="../assets/imgs/6.jpg"
              alt="Card image cap"
            />
            <div class="card-body">
              <h5 class="card-title">{{ $t("cards.title3") }}</h5>
              <p class="card-text">
                {{ $t("cards.content3") }}
              </p>
              <button type="button" class="btn">{{ $t("cards.btn") }}</button>
            </div>
          </div>
        </div>

        <div class="col">
          <div class="card text-center">
            <img
              class="card-img-top"
              src="https://www.neusoft.com/cn/upload/img/business-pic4.jpg"
              alt="Card image cap"
            />
            <div class="card-body">
              <h5 class="card-title">{{ $t("cards.title4") }}</h5>
              <p class="card-text">
                {{ $t("cards.content4") }}
              </p>
              <button type="button" class="btn">{{ $t("cards.btn") }}</button>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="boxLRB">
      <div class="row">
        <div class="col">
          <div class="right4">
            <div class="card text-center ol">
              <div class="card-body">
                <h2 class="card-title">
                  {{ $t("boxLR.title4") }}
                </h2>
                <h5 class="card-text">
                  {{ $t("boxLR.content4") }}
                </h5>
                <button type="button" class="btn btn-outline-light">
                  {{ $t("boxLR.btn2") }}
                </button>
                <p class="next">{{ $t("boxLR.more2") }}</p>
              </div>
            </div>
          </div>
        </div>
        <div class="col op">
          <div class="left">
            <h2>{{ $t("boxLR.title4") }}</h2>
            <h5>
              {{ $t("boxLR.content4") }}
            </h5>
            <button type="button" class="btn btn-outline-light">
              {{ $t("boxLR.btn2") }}
            </button>
            <p class="next">{{ $t("boxLR.more2") }}</p>
          </div>
        </div>
      </div>
    </div>
    <div class="three">
      <div class="container">
        <div class="row">
          <div class="col-sm">
            <div class="col">
              <div class="card text-center">
                <div class="borders">
                  <img
                    class="card-img-top"
                    src="https://www.neusoft.com/cn/upload/img/icon/target-icon-1.svg"
                    alt="Card image cap"
                  />
                </div>
                <div class="card-body">
                  <h5 class="card-title">{{ $t("three.title1") }}</h5>
                  <p class="card-text">
                    {{ $t("three.content1") }}
                  </p>
                </div>
              </div>
            </div>
          </div>
          <div class="col-sm">
            <div class="col">
              <div class="card text-center">
                <div class="borders">
                  <img
                    class="card-img-top"
                    src="https://www.neusoft.com/cn/upload/img/icon/target-icon-5.svg"
                    alt="Card image cap"
                  />
                </div>
                <div class="card-body">
                  <h5 class="card-title">{{ $t("three.title2") }}</h5>
                  <p class="card-text">
                    {{ $t("three.content2") }}
                  </p>
                </div>
              </div>
            </div>
          </div>
          <div class="col-sm">
            <div class="col">
              <div class="card text-center">
                <div class="borders">
                  <img
                    class="card-img-top"
                    src="https://www.neusoft.com/cn/upload/img/icon/target-icon-4.svg"
                    alt="Card image cap"
                  />
                </div>
                <div class="card-body">
                  <h5 class="card-title">{{ $t("three.title3") }}</h5>
                  <p class="card-text">
                    {{ $t("three.content3") }}
                  </p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="footer">
      <div class="row">
        <div class="col-xs-12 col-md-4">
          <div class="col">
            <div class="card text-center">
              <ul class="list-group list-group-flush">
                <li class="list-group-item">
                  <img src="../assets/logo.png" alt="" />
                </li>
                <li class="list-group-item">
                  <el-select
                    size="small"
                    v-model="value"
                    @change="switchLanguage"
                    placeholder="请选择"
                  >
                    <el-option
                      v-for="item in options"
                      :key="item.value"
                      :label="item.label"
                      :value="item.value"
                    >
                    </el-option>
                  </el-select>
                </li>
              </ul>
            </div>
          </div>
        </div>

        <div class="col-xs-12 col-md-2">
          <div class="col">
            <div class="card">
              <ul class="list-group list-group-flush">
                <li class="list-group-item">{{ $t("footer.aboutUs") }}</li>
                <li class="list-group-item">{{ $t("footer.aboutUs1") }}</li>
                <li class="list-group-item">{{ $t("footer.aboutUs2") }}</li>
                <li class="list-group-item">{{ $t("footer.aboutUs3") }}</li>
                <li class="list-group-item">{{ $t("footer.aboutUs4") }}</li>
                <li class="list-group-item">{{ $t("footer.aboutUs5") }}</li>
              </ul>
            </div>
          </div>
        </div>

        <div class="col-xs-12 col-md-2">
          <div class="col">
            <div class="card">
              <ul class="list-group list-group-flush">
                <li class="list-group-item">{{ $t("footer.news") }}</li>
                <li class="list-group-item">{{ $t("footer.news1") }}</li>
              </ul>
            </div>
          </div>
        </div>
        <div class="col-xs-12 col-md-2">
          <div class="col">
            <div class="card">
              <ul class="list-group list-group-flush">
                <li class="list-group-item">
                  {{ $t("footer.CorporateSocial") }}
                </li>
                <li class="list-group-item">
                  {{ $t("footer.CorporateSocial1") }}
                </li>
                <li class="list-group-item">
                  {{ $t("footer.CorporateSocial2") }}
                </li>
                <li class="list-group-item">
                  {{ $t("footer.CorporateSocial3") }}
                </li>
                <li class="list-group-item">
                  {{ $t("footer.CorporateSocial4") }}
                </li>
              </ul>
            </div>
          </div>
        </div>
        <div class="col-xs-12 col-md-2">
          <div class="col">
            <div class="card">
              <ul class="list-group list-group-flush">
                <li class="list-group-item">{{ $t("footer.joinUs") }}</li>
                <li class="list-group-item">{{ $t("footer.joinUs1") }}</li>
              </ul>
            </div>
          </div>
        </div>

        <div class="container">
          <div class="row text-center">
            <div class="col align-self-center">
              <div class="end">
                <span>{{ $t("end.company") }}</span>
                <span>
                  <img
                    src="https://sf1-scmcdn2-tos.pstatp.com/ies/bytedance_official/_next/static/images/icp-9ca98112ae9d12370794027a9b22b221.png"
                    alt=""
                  />
                  {{ $t("end.number") }}</span
                >
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <el-backtop></el-backtop>
  </div>
</template>
<script>
import Swiper from "swiper";
// 引入插件
import { swiper, swiperSlide } from "vue-awesome-swiper";
import "swiper/swiper-bundle.css";
import Xinglei from '../components/xinglei.vue';
export default {
  components: {
    swiper,
    Xinglei,
  },
  data() {
    return {
      msg: [1,2,3,45,67,89],
      psVal: '',
      swiperOption: {
        // loop: true,
        autoplay: {
          delay: 3000,
          stopOnLastSlide: false,
          disableOnInteraction: false,
        },
        // 显示分页
        pagination: {
          el: ".swiper-pagination",
          clickable: true, //允许分页点击跳转
        },
        // 设置点击箭头
        navigation: {
          nextEl: ".swiper-button-next",
          prevEl: ".swiper-button-prev",
        },
      },
      banner: [
        "https://sf1-scmcdn2-tos.pstatp.com/ies/bytedance_official/_next/static/images/2-d144f7683bd942509b6456ee4ad66835.jpg",
        "https://sf1-scmcdn2-tos.pstatp.com/ies/bytedance_official/_next/static/images/1-f24e4ff81b4839abcf20f8b9751e4720.jpg",
        "https://sf1-scmcdn2-tos.pstatp.com/ies/bytedance_official/_next/static/images/2-d144f7683bd942509b6456ee4ad66835.jpg",
        "https://sf1-scmcdn2-tos.pstatp.com/ies/bytedance_official/_next/static/images/3-c995479da352d8306fb33c6d11902fb8.png",
      ],
      options: [
        {
          value: "1",
          label: "English",
        },
        {
          value: "2",
          label: "中文简",
        },
      ],
      value: "2",
      navFlag: true,
      i: 0,
      // bannerW: "",
      // bannerH: "",
      clientWidth: document.body.clientWidth,
      clientHeight: document.body.clientHeight,
    };
  },

  computed: {
    swiper() {
      return this.$refs.mySwiper.swiper;
    },
  },
  mounted() {
    if (localStorage.getItem("localeVal")) {
      this.value = localStorage.getItem("localeVal");
      if (this.value == 1) {
        localStorage.setItem("localeVal", this.value);
        this.$i18n.locale = "en";
      } else if (this.value == 2) {
        localStorage.setItem("localeVal", this.value);
        this.$i18n.locale = "zh";
      }
    }

    //     //设置localStroage值
    // localStorage.setItem（'username','zhangsan'）;
    // //获取localStroage值
    // localStorage.getItem（'username'）;

    // console.log("this is current swiper instance object", this.swiper);
    // 轮播文字
    new Swiper(".swiper-container", {
      loop: true,
      // 如果需要分页器
      pagination: ".swiper-pagination",
      // 如果需要前进后退按钮
      navigation: {
        nextEl: ".swiper-button-next",
        prevEl: ".swiper-button-prev",
      },
      // 如果需要滚动条
      scrollbar: ".swiper-scrollbar",
    });

    // 监听（绑定）滚轮 滚动事件
    window.addEventListener("scroll", this.handleScroll, true);

    // 在DOM渲染数据时，设置下区域高度为浏览器可视区域高度．
    this.clientHeight = document.body.clientHeight;
    this.clientWidth = document.body.clientWidth;
    // 监听window的resize事件．在浏览器窗口变化时再设置下区域高度．
    const _this = this;
    window.onresize = function temp() {
      _this.clientHeight = document.body.clientHeight;
      _this.clientWidth = document.body.clientWidth;
    };
    // console.log(this.clientWidth);
    // console.log(this.clientHeight);
  },

  watch: {
    clientWidth: {
      handler(newVal, oldVal) {
        // console.log(newVal);
        // console.log(oldVal);
        this.clientWidth = newVal;
        console.log(this.clientWidth);
        if (this.clientHeight + 200 > this.clientWidth) {
          this.clientHeight = this.clientWidth - 220;
        }
      },
      immediate: true,
      deep: true,
    },
    clientHeight: {
      handler(newVal, oldVal) {
        // console.log(newVal);
        // console.log(oldVal);
        this.clientHeight = newVal;
        // console.log(this.clientHeight);
        // console.log(this.clientWidth);
        if (this.clientHeight + 200 > this.clientWidth) {
          this.clientHeight = this.clientWidth - 220;
        }
        console.log(this.clientHeight);
      },
      immediate: true,
      deep: true,
    },
  },

  methods: {
     receive(val) {
       console.log(val)
       this.psVal = val
    },
    handleScroll() {
      // 页面滚动距顶部距离
      var scrollTop =
        window.pageYOffset ||
        document.documentElement.scrollTop ||
        document.body.scrollTop;
      var scroll = scrollTop - this.i;
      this.i = scrollTop;
      // console.log(scrollTop);
      // console.log(scroll);
      console.log(this.navFlag);
      if (scrollTop > 500) {
        this.navFlag = true;
        if (scroll < 0) {
          this.navFlag = true;
        } else {
          this.navFlag = false;
        }
      }
    },
    // 切换语言
    switchLanguage(val) {
      console.log(val);
      // localeVal = localStorage.setItem('localeVal',val)
      if (val == 1) {
        localStorage.setItem("localeVal", val);
        this.$i18n.locale = "en";
      } else if (val == 2) {
        localStorage.setItem("localeVal", val);
        this.$i18n.locale = "zh";
      }
    },
  },
};
</script>

<style lang="scss" scoped>
.el-select-dropdown .el-select-dropdown__item {
  height: 20px !important;
  line-height: 20px !important;
}
</style>

<style lang="scss" scoped>
/*==================================================
=            Bootstrap 3 Media Queries             =
==================================================*/

/*==========  Mobile First Method  ==========*/

/* Custom, iPhone Retina */
@media only screen and (min-width: 320px) {
}

/* Extra Small Devices, Phones */
@media only screen and (min-width: 480px) {
}

/* Small Devices, Tablets */
@media only screen and (min-width: 768px) {
}

/* Medium Devices, Desktops */
@media only screen and (min-width: 992px) {
}

/* Large Devices, Wide Screens */
@media only screen and (min-width: 1200px) {
}

/*==========  Non-Mobile First Method  ==========*/

/* Large Devices, Wide Screens */
@media only screen and (max-width: 1200px) {
}

/* Medium Devices, Desktops */
@media only screen and (max-width: 992px) {
  .banners {
    padding-top: 100px;
    .tit {
      left: 0 !important;
      padding: 7rem 6% 2% 3% !important;
      border-bottom-right-radius: 50px !important;
      p {
        font-size: 0.8rem !important;
      }
      h1 {
        font-size: 1.3rem !important;
      }
    }
  }
  .right1 {
    padding: 0 !important;
  }
  .op {
    display: none;
    padding: 0;
  }
  .ol {
    display: block !important;
  }

  .cards {
    .row {
      .col {
        padding: 0 6%;
        .card {
          margin: 0 0 6% 0;
        }
        .card:first-child {
          margin-top: 6%;
        }
      }
    }
  }

  .txtbanner {
    padding: 2% 10% !important;
  }
}

/* Small Devices, Tablets */
@media only screen and (max-width: 768px) {
  .txtbanner {
    padding: 2% 6% !important;
    .swiper-container {
      .title {
        font-size: 18px !important;
      }
      .text {
        p {
          font-size: 14px !important;
        }
      }
    }
  }
  .logo {
    width: 120px !important;
    padding: 0 !important;
  }
  .banners {
    padding-top: 56px;
    .tit {
      padding: 4rem 6% 2% 3% !important;
    }
  }
  .boxLR {
    .row {
      height: 466px !important;
      .card {
        transform: scale(0.8);
      }
    }
  }
    .boxLRB {
    .row {
      height: 466px !important;
      .card {
        transform: scale(0.8);
      }
    }
  }
}

/* Extra Small Devices, Phones */
@media only screen and (max-width: 480px) {
  .txtbanner {
    padding: 2% 4% !important;
  }
}

/* Custom, iPhone Retina */
@media only screen and (max-width: 320px) {
}
</style>

<style lang='scss' scoped>
html {
  font-size: 13.33333333vw;
}

.box {
  max-width: 1920px;
  margin: 0 auto;
}

body {
  .bg-dark {
    background: #3c8cff !important;
    .nav-link {
      color: #fff;
      cursor: pointer;
    }
    .nav-link:hover {
      color: #78e6dc;
    }
  }
  .header {
    width: 100%;
    max-width: 1920px;
    background: #3c8cff;
    position: fixed;
    z-index: 100;
  }
  .row {
    margin: 0;
  }
  .logo {
    width: 170px;
    padding: 20px 0;
    margin-left: 4%;
    // margin-top: 24px;
  }
  .nav {
    height: 100px;
  }
  .nav-item {
    text-align: center;
    padding: 0 30px;
  }

  .el-carousel__item h3 {
    color: #475669;
    font-size: 18px;
    opacity: 0.75;
    line-height: 300px;
    margin: 0;
  }

  .banners >>> .el-carousel__container button {
    display: none !important;
  }

  // .el-carousel__item:nth-child(2n) {
  //   background-color: #99a9bf;
  // }

  // .el-carousel__item:nth-child(2n + 1) {
  //   background-color: #ffffff;
  // }

  .el-carousel--horizontal img {
    display: block;
    width: 100%;
    // min-width: 1920px;
    margin: 0 auto;
    margin-top: -83px;
  }

  .box >>> .el-carousel__indicators--outside {
    margin-top: -30px;
    position: relative;
    top: 0;
    left: 0;
  }

  .banner {
    position: relative;
    z-index: 10;
  }

  .banner .tit {
    position: absolute;
    top: 0px;
    left: 8%;
    z-index: 10;
    box-sizing: border-box;
    padding: 180px 100px 60px 40px;
    background: rgb(255, 255, 255);
    border-bottom-right-radius: 100px;
  }

  .tit p {
    font-family: "Gilroy";
    font-weight: 500;
    font-size: 26px;
    color: #828282;
  }

  .tit h1 {
    font-size: 58px;
  }

  .banns .swiper-container {
    width: 100%;
    height: 100%;
  }

  .banns .swiper-slide {
    text-align: center;
    font-size: 18px;
    background: #fff;

    /* Center slide text vertically */
    display: -webkit-box;
    display: -ms-flexbox;
    display: -webkit-flex;
    display: flex;
    -webkit-box-pack: center;
    -ms-flex-pack: center;
    -webkit-justify-content: center;
    justify-content: center;
    -webkit-box-align: center;
    -ms-flex-align: center;
    -webkit-align-items: center;
    align-items: center;
  }
}

.banners {
  position: relative;
  z-index: 10;
  .tit {
    position: absolute;
    top: 0px;
    left: 8%;
    z-index: 10;
    box-sizing: border-box;
    // padding: 180px 100px 60px 40px;
    padding: 9rem 4% 3% 3%;
    background: rgb(255, 255, 255);
    border-bottom-right-radius: 30%;
    p {
      font-family: "Gilroy";
      font-weight: 500;
      // font-size: 26px;
      font-size: 1.3rem;
      color: #828282;
    }
    h1 {
      // font-size: 58px;
      font-size: 2.9rem;
    }
  }
}

.bannerH {
  width: 1920px;
  height: 970px;
}

.txtbanner {
  width: 100%;
  padding: 2% 20%;
  margin: 0 auto;
  .swiper-container {
    // width: 920px;
    height: 100%;
    cursor: default;
    .title {
      font-size: 30px;
      margin-bottom: 20px;
      display: block;
      text-decoration: none;
      line-height: 1.4;
      color: #666;
    }
    .text {
            p {
        font-size: 16px;
        line-height: 1.8em;
        // max-height: 5.4em;
        overflow: hidden;
        -o-text-overflow: ellipsis;
        text-overflow: ellipsis;
        // -webkit-line-clamp: 10;
        -webkit-box-orient: vertical;
        display: -webkit-box;
        color: #777;
      }
    }
  }
}

.boxLR {
  background: #005bac;
  .row {
    height: 666px;
    .col {
      padding: 0;
      .left {
        padding: 24% 10% 0;
        color: #fff;
        h5 {
          margin: 1em 0 2em 0;
          line-height: 2em;
        }
        button {
          margin: 0 0 1.5em 0;
          border-radius: 0;
          padding: 8px 40px;
        }
        button:hover {
          color: #00bef0;
        }
        .next:hover {
          color: #00bef0;
          cursor: pointer;
        }
      }
      .card {
        border: none;
        background: none;
      }
      .right1 {
        width: 100%;
        height: 100%;
        float: left;
        box-sizing: border-box;
        overflow-y: auto;
        background-size: cover;
        background: url("https://www.neusoft.com/cn/upload/img/20210106-2507/epitesting-0105.jpg")
          no-repeat center;
        color: #fff;
        display: flex;
        align-items: center;
        .ol {
          display: none;
          margin: 0 auto;
        }
        h5 {
          margin: 1em 0 2em 0;
          line-height: 2em;
        }
        button {
          margin: 0 0 1.5em 0;
          border-radius: 0;
          padding: 8px 40px;
          border-color: #00bef0;
          background: #00bef0;
        }
        button:hover {
          color: #00bef0;
          background: #fff;
        }
      }
      .right2 {
        width: 100%;
        height: 100%;
        float: left;
        box-sizing: border-box;
        overflow-y: auto;
        background-size: cover;
        background: url("https://www.neusoft.com/cn/upload/img/index/section-saca-echo-trust.jpg")
          no-repeat center;
        color: #fff;
        display: flex;
        align-items: center;
        .ol {
          display: none;
          margin: 0 auto;
        }
        h5 {
          margin: 1em 0 2em 0;
          line-height: 2em;
        }
        button {
          margin: 0 0 1.5em 0;
          border-radius: 0;
          padding: 8px 40px;
          border-color: #00bef0;
          background: #00bef0;
        }
        button:hover {
          color: #00bef0;
          background: #fff;
        }
      }
      .right3 {
        width: 100%;
        height: 100%;
        float: left;
        box-sizing: border-box;
        overflow-y: auto;
        background-size: cover;
        background: url("https://www.neusoft.com/cn/upload/img/index/pic-1.jpg")
          no-repeat center;
        color: #fff;
        display: flex;
        align-items: center;
        .ol {
          display: none;
          margin: 0 auto;
        }
        h5 {
          margin: 1em 0 2em 0;
          line-height: 2em;
        }
        button {
          margin: 0 0 1.5em 0;
          border-radius: 0;
          padding: 8px 40px;
          border-color: #00bef0;
          background: #00bef0;
        }
        button:hover {
          color: #00bef0;
          background: #fff;
        }
      }
      .right4 {
        width: 100%;
        height: 100%;
        float: left;
        box-sizing: border-box;
        overflow-y: auto;
        background-size: cover;
        background: url("https://www.neusoft.com/cn/upload/img/index/section-story-main-pic1.jpg")
          no-repeat center;
        color: #fff;
        display: flex;
        align-items: center;
        .ol {
          display: none;
          margin: 0 auto;
        }
        h5 {
          margin: 1em 0 2em 0;
          line-height: 2em;
        }
        button {
          margin: 0 0 1.5em 0;
          border-radius: 0;
          padding: 8px 40px;
          border-color: #00bef0;
          background: #00bef0;
        }
        button:hover {
          color: #00bef0;
          background: #fff;
        }
      }
    }
  }
}

.cards {
  background: #e3e7ea;
  // padding: 80px 140px;
  padding: 4% 8%;
  .card {
    button {
      border: 1px solid #00bef0;
      border-radius: 0;
      padding: 8px 40px;
      background: #00bef0;
      color: #fff;
      box-sizing: border-box;
      transition: 0.3s;
    }
    p {
      font-size: 14px;
      color: #aeb5ba;
      margin: 0.7em 0 1.5em 0;
      padding: 0 10px;
    }
  }
  .card:hover {
    cursor: pointer;
    button {
      color: #00bef0;
      background: #fff;
    }
  }
}

.boxLRB {
  background: #005bac;
  .row {
    height: 666px;
    .col {
      padding: 0;
      .left {
        padding: 24% 10% 0;
        color: #fff;
        h5 {
          margin: 1em 0 2em 0;
          line-height: 2em;
        }
        button {
          margin: 0 0 1.5em 0;
          border-radius: 0;
          padding: 8px 40px;
        }
        button:hover {
          color: #00bef0;
        }
        .next:hover {
          color: #00bef0;
          cursor: pointer;
        }
      }
      .card {
        border: none;
        background: none;
      }
      .right4 {
        width: 100%;
        height: 100%;
        float: left;
        box-sizing: border-box;
        overflow-y: auto;
        background-size: cover;
        background: url("https://www.neusoft.com/cn/upload/img/index/section-story-main-pic1.jpg")
          no-repeat center;
        color: #fff;
        display: flex;
        align-items: center;
        .ol {
          display: none;
          margin: 0 auto;
        }
        h5 {
          margin: 1em 0 2em 0;
          line-height: 2em;
        }
        button {
          margin: 0 0 1.5em 0;
          border-radius: 0;
          padding: 8px 40px;
          border-color: #00bef0;
          background: #00bef0;
        }
        button:hover {
          color: #00bef0;
          background: #fff;
        }
        .next:hover {
          color: #00bef0;
          cursor: pointer;
        }
      }
    }
  }
}

.three {
  background: #4b5564;
  box-sizing: border-box;
  padding: 120px 60px 80px;
  color: #fff;
  .card {
    background: #4b5564;
    border: none;
    cursor: pointer;
    .borders {
      width: 160px;
      height: 160px;
      border: 3px solid #00bef0;
      border-radius: 50%;
      margin: 0 auto;
      transition: 0.4s;
      img {
        display: block;
        width: 160px;
        height: 160px;
        padding: 40px;
      }
    }
    p {
      color: #aeb5ba;
      font-size: 14px;
    }
  }
  .card:hover .borders {
    transform: translateY(-20px);
  }
}

.footer {
  background: #3c8cff;
  img {
    display: block;
    width: 180px;
    height: 43px;
    margin: 0 auto 10%;
  }
  .card {
    background: #3c8cff;
    border: none;
    text-align: center;
    li:first-child {
      font-weight: bolder;
      font-size: 16px;
      padding-top: 20px;
      padding-bottom: 20px;
      cursor: text;
    }
    li:first-child:hover {
      color: #fff;
    }
    .list-group-item {
      background: #3c8cff;
      border: none;
      color: #fff;
      padding-top: 4px;
      padding-bottom: 4px;
      cursor: pointer;
    }
    .list-group-item:hover {
      color: #78e6dc;
    }
  }
  .end {
    margin-top: 30px;
    span {
      display: block;
      font-size: 14px;
      color: #fff;
      img {
        display: inline;
        width: 20px;
        height: 20px;
        margin: 0;
        position: relative;
        top: -2px;
      }
    }
  }
}
</style>