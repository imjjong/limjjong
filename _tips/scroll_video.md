---
date: "201w-11-08 12:45:07"
layout: tips
title: scroll_video
description: 그냥 테스툥
image: /images/index/kitchen_design01.png
category: tips
tags:
  - jjong
author: JJong
paginate: false
---

이것은 무엇이오 웹에서 입력가능하옹? 뭐짐 이제되
<head>
<style>
  body {
    /* sets the page defaults e.g. background and default typography */
    background: #fff;
    font-family: 'Noto Serif', serif;
    margin: 0;
    font-size: 20px;
    line-height: 1.5;
    color: rgba(0, 0, 0, 0.74);
}


/* a few tweaks here and there */

h2 {
    margin: 0;
}

figure {
    margin: 0;
    /* resets the left margin in the figure*/
}

figure img {
    max-width: 100%;
    /* images will shrink to fit inside the main conent column*/
    box-shadow: 0px 1px 3px rgba(0, 0, 0, 0.7);
}

figcaption {
    font-size: 14px;
    color: #555;
}

blockquote {
    width: 66%;
    margin: 1em auto;
    background: #ddd;
    padding: 1em;
    font-size: 1.25em;
    text-align: center;
    color: #696969;
    border-bottom: 1px solid #999;
    border-top: 1px solid #999;
}


/* Styling the full-page background headers */

.image_bg, .color_bg {
    height: 100vh;
    /* this sets the height of each full width image section to that of the viewport.*/
    position: relative;
    /*display: flex;  */
    background-position: center !important;
}


/* the text inside the headers */




/* Styles for individual header sections by class name. */

.title {
    background: url(../images/IMG_20150714_101239.jpg) no-repeat;
    background-size: cover;
    background-attachment: fixed;
    /* the background image doesn't move when scrolling*/
}


/* the above style gets copied for every new section header with background image. Each new copy has a new class name. */

.paris {
    background: url(../images/Paris2013.jpg);
    background-size: cover;
    background-attachment: fixed;
}

.green_header {
    /* this sets the background colour of the coloured header. */
    background: #AED581;
}


/* Content sections */

.content {
    margin: 0 auto;
    padding: 1em 20%;
    /* this in-effect sets the content section's width e.g. 20% = 60% width. */
}

footer {
    height: 100px;
    background: #000;
    color: #eee;
    text-align: center;
    padding: 1em;
}

/* This is the mobile responsive stylesheet */

@media only screen and (min-width: 768px) {
    /* tablets and desktop */
}

@media only screen and (max-width: 767px) {
    /* phones */
    .content {
      margin: 0 auto;
      position: relative;

      padding: 1em;
    }

    blockquote.left {

        margin: 0 1em 1em 0;
        background: wheat;
        padding: 1em;
        font-size: 1.5em;
        width: 90%;
        position: relative;
    }


}

@media only screen and (max-width: 767px) and (orientation: portrait) {
    /* portrait phones */
}

</style>
</head>


<body>
  <article>
    
<!-- 영상 -->
<video id="uke" src="https://d2xch9q88t25k4.cloudfront.net/main-page-media/PC/mannacea.mp4" type="video/mp4" width="640" height="360" muted loop>
</video>

          <h3>Images with captions</h3>
          <p>Donec ullamcorper nulla non metus auctor fringilla. Vivamus sagittis lacus vel augue laoreet rutrum faucibus dolor auctor. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Curabitur blandit tempus porttitor. </p>
          <p>Praesent commodo cursus magna, vel scelerisque nisl consectetur et. Duis mollis, est non commodo luctus, nisi erat porttitor ligula, eget lacinia odio sem nec elit. Vivamus sagittis lacus vel augue laoreet rutrum faucibus dolor auctor.</p>

          <video id="uke2" width="640" height="360" muted loop>
              <source src="https://d2xch9q88t25k4.cloudfront.net/main-page-media/PC/mannacea.mp4" type="video/mp4">
          </video>

         

  </article>


  <script src="/assets/scroll_video/ScrollMagic.min.js"></script>
  <script src="./assets/scroll_video/plugins/debug.addIndicators.min.js"></script>
  <script src='/assets/js/jquery.min.js'></script>
  <script src="/assets/wow_animate/wow.min.js"></script>
  <script src="assets/slick/slick.min.js"></script>
  <script>
    // Uncomment to initialise WOW.js
new WOW().init();

$(document).ready(function(){
  $('.carousel').slick({
    dots: true
  });
});

  var ukeVid = document.getElementById('uke');
  var ukeVid2 = document.getElementById('uke2');

// init controller
var controller = new ScrollMagic.Controller();

// build scene
var scene = new ScrollMagic.Scene({triggerElement: "#uke", duration: 200})
        .addTo(controller)
        .addIndicators() // add indicators (requires plugin)

        .on("enter", function () {
          ukeVid.play();
        })
        .on("leave", function () {
          ukeVid.pause();
        })

        // build scene
var scene2 = new ScrollMagic.Scene({triggerElement: "#uke2", duration: 200})
.addTo(controller)
.addIndicators() // add indicators (requires plugin)

.on("enter", function () {
  ukeVid2.play();
})
.on("leave", function () {
  ukeVid2.pause();
})

  </script>  

</body>
