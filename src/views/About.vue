<!--
 * @Description: 关于我们页面组件，未完成
 * @Author: hai-27
 * @Date: 2020-02-07 16:23:00
 * @LastEditors: hai-27
 * @LastEditTime: 2020-03-04 22:16:54
 -->
<template>
    <div class="about" id="about" name="about">
        <div class="about-header">
            <div class="about-title">
                <i class="el-icon-tickets" style="color: #ff6700;"></i>
                关于我们
            </div>
        </div>
        <div class="footerall">
            <div class='demo' style=" ;width: 1226px;margin: 0 auto ">
                <video-player class="video-player vjs-custom-skin"
                              ref="videoPlayer"
                              :playsinline="true"
                              :options="playerOptions">
                </video-player>
            </div>
            <ul class="textt">
                <li><h2>永远相信美好的事情即将发生</h2></li>
                <li>小米公司正式成立于2010年4月，是一家以手机、智能硬件和 IoT 平台为核心的互联网公司。创业仅7年时间， 小米的年收入就突破了千亿元人民币。截止2018年，
                    小米的业务遍及全球80多个国家和地区。
                </li>
                <li>小米的使命是，始终坚持做“感动人心、价格厚道”的好产品， 让全球每个人都能享受科技带来的美好生活。</li>
            </ul>
            <img class="back"
                 src="//cdn.cnbj1.fds.api.mi-img.com/mi-mall/510d5f68e56e60f583bbbb0c12bd1b1d.jpg?w=1226&h=690" alt="">
            <ul class="textt">
                <li>“和用户交朋友，做用户心中最酷的公司”的愿景都在驱动着我们努力创新，不断追求极致的产品和效率，成就了一个不断缔造成长奇迹的小米。</li>
            </ul>
            <img class="back"
                 src="https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/3fb39b908a57ae925f870277a07526a2.jpg?w=1226&h=634"
                 alt="">
            <ul class="textt">
                <li>
                    目前，小米是全球第四大智能手机制造商，在30余个国家和地区的手机市场进入了前五名，特别是在印度，连续5个季度保持手机出货量第一。通过独特的“生态链模式”，小米投资、带动了更多志同道合的创业者，同时建成了连接超过1.3亿台智能设备的IoT平台。
                </li>
                <li>2018年7月9日，小米成功在香港主板上市，成为了港交所首个同股不同权上市公司，创造了香港史上最大规模科技股IPO，以及当时历史上全球第三大科技股IPO。</li>
                <li>感谢您关注小米，和我们并肩投身于创造商业效率新典范，用科技改善人类生活的壮丽事业。许商业以敦厚，许科技以温暖，许大众以幸福，我们的征途是星辰大海，请和我们一起，永远相信美好的事情即将发生。</li>
            </ul>
            <img class="back"
                 src="https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/2c4ec0786726524f2d4d436c811d799e.jpg?w=1226&h=672"
                 alt="">
        </div>
    </div>

</template>
<script>

    export default {
        data() {
            return {
                playerOptions: {
                    playbackRates: [0.7, 1.0, 1.5, 2.0], //播放速度
                    autoplay: false, //如果true,浏览器准备好时开始回放。
                    muted: false, // 默认情况下将会消除任何音频。
                    loop: false, // 导致视频一结束就重新开始。
                    preload: "auto", // 建议浏览器在<video>加载元素后是否应该开始下载视频数据。auto浏览器选择最佳行为,立即开始加载视频（如果浏览器支持）
                    language: "zh-CN",
                    aspectRatio: "16:9", // 将播放器置于流畅模式，并在计算播放器的动态大小时使用该值。值应该代表一个比例 - 用冒号分隔的两个数字（例如"16:9"或"4:3"）
                    fluid: true, // 当true时，Video.js player将拥有流体大小。换句话说，它将按比例缩放以适应其容器。
                    sources: [
                        {
                            type: "video/ogg", //这里的种类支持很多种：基本视频格式、直播、流媒体等，具体可以参看git网址项目
                            src:"https://v.mifile.cn/b2c-mimall-media/71fa48c0e68fe732a3b7c28e1b33278d.mp4" //url地址
                        }
                    ],
                    poster: "http://images.tmtpost.com/uploads/images/2019/03/20190320161502846.jpg?imageMogr2/strip/interlace/1/quality/85/thumbnail/1400x967/gravity/center/crop/%211400x967&ext=.jpg", //你的封面地址
                    width: document.documentElement.clientWidth, //播放器宽度

                    notSupportedMessage: "此视频暂无法播放，请稍后再试", //允许覆盖Video.js无法播放媒体源时显示的默认信息。
                    controlBar: {
                        timeDivider: true,
                        durationDisplay: true,
                        remainingTimeDisplay: false,
                        fullscreenToggle: true //全屏按钮
                    }
                },
            };
        },
        methods: {

    }

    }
</script>
<style scoped>
    .about {
        background-color: #f5f5f5;
    }

    .about .about-header {
        height: 64px;
        background-color: #fff;
        border-bottom: 2px solid #ff6700;
    }

    .about .about-header .about-title {
        width: 1225px;
        margin: 0 auto;
        height: 64px;
        line-height: 64px;
        font-size: 28px;
    }

    .footerall {
        margin: 0 auto;
    }
    .textt {
        width: 43%;
        margin: 0 auto;
        padding: 67px 310px;
    }

    .textt h2 {
        font-size: 28px;
        color: #333;
        font-weight: normal;
    }

    .textt li {
        color: #757575;
        margin: 10px 0 0 0;
    }

    .back {
        display: block;
        height: 450px;
        width: 1226px;
        margin: 0 auto;
    }

    .about .content {
        padding: 20px 0;
        width: 1225px;
        margin: 0 auto;
    }

    .about .content .goods-list {
        margin-left: -13.7px;
        overflow: hidden;
    }
</style>
