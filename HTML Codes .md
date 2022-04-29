# CSS 
1. box shadow inset
```css
  box-shadow: inset 0 1px 3px rgba(0, 0, 0, 0.12),
              inset 0 1px 2px rgba(0, 0, 0, 0.24);
```

2. Transform
```css
  div:hover{
      curser : pointer;
      transition : all 2s linear;
      transform : rotate(10deg); / transform : translateX(10px);
```

3. Transition Property
```css
  div {
    width: 100px;
    height: 100px;
    background: red;
    transition: width 2s;
  }

  div:hover {
    width: 300px;
  }
```

# HTML
1. <b>Bootstrap5 CDN</b> [ fontawesome + OWL ]
```html
  <!DOCTYPE html>
  <html lang="en">
      <head>
          <meta charset="utf-8">
          <meta name="viewport" content="width=device-width, initial-scale=1">
          <title> Bootstrap5 </title>
          <!-- Bootstrap5 CSS -->
          <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/css/bootstrap.min.css" rel="stylesheet">
          <!-- Fontawesome CSS -->
          <link rel="stylesheet" href="https://pro.fontawesome.com/releases/v5.10.0/css/all.css" />
          <!-- OWL CSS -->
          <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/OwlCarousel2/2.3.4/assets/owl.carousel.min.css" />
          <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/OwlCarousel2/2.3.4/assets/owl.theme.default.min.css" />
      </head>
      <body>
        <style>
          .owl-theme .owl-dots .owl-dot span{
               background: #ffd7b2;
            }
            .owl-theme .owl-dots .owl-dot.active > span{
               background: var(--primary);
            }
        </style>
        
        
        <!-- Bootstrap5 JS -->
        <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/js/bootstrap.bundle.min.js"></script>
        <!-- OWL JS -->
        <script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/3.6.0/jquery.min.js"></script>
        <script src="https://cdnjs.cloudflare.com/ajax/libs/OwlCarousel2/2.3.4/owl.carousel.min.js"></script>
        <script>
          $('.owl-carousel').owlCarousel({
                loop:true,
                margin:10,
                nav:false,
                dots:true,
                autoplay:true,
                autoplayTimeout: 3000,
                autoplaySpeed: 1000,
                responsive:{
                    0:{
                        items:1
                    },
                    600:{
                        items:3
                    },
                    1000:{
                        items:5
                    }
                }
            })
        </script>
      </body>
  </html>
```
Fontawesome - https://fontawesome.com/v5/search <br/>
OWL - https://owlcarousel2.github.io/OwlCarousel2/
<br/>
<br/>
<br/>
<br/>
carousel-example
```html
<style>
  
.owl-carousel {
   position: relative;
}

.owl-prev,
.owl-next {
   position: absolute;
   z-index: 1000;
}

.owl-prev {
   left: -80px;
   bottom: 50%;
   
   background-color: transparent;
}

.owl-next {
   right: -80px;
   bottom: 50%;
}
   .owl-theme .owl-dots .owl-dot span {
      background: #DFDCFB;
   }
   
   .owl-theme .owl-dots .owl-dot.active>span {
      background:$primary
   }
}  
</style>
<section id="POPULAR">
      <div class="popular">
         <div class="container">
            <div class="popular-wrapper">
               <h3 class="title">Most&nbsp;Popular</h3>
               <div class="owl-carousel owl-theme owl-loaded">
                  <div class="owl-carousel carousel-1 owl-theme mt-5">
                     <div class="item">
                        <img src="images/img-1.png" alt="">
                        <div class="content">
                           <h4>Some Title About This place</h4>
                           <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Augue at a turpis massa amet
                              fermentum non.</p>
                        </div>
                     </div>
                     <div class="item">
                        <img src="images/img-2.png" alt="">
                        <div class="content">
                           <h4>Some Title About This place</h4>
                           <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Augue at a turpis massa amet
                              fermentum non.</p>
                        </div>
                     </div>
                  </div>
                  <div class="owl-nav">
                     <div class="owl-prev" style="background-color: transparent;">
                        <img src="images/icons/left.svg" alt="">
                     </div>
                     <div class="owl-next" style="background-color: transparent;">
                        <img src="images/icons/right.svg" alt="">
                     </div>
                  </div>
                  <div class="owl-dots">
                     <div class="owl-dot active"><span></span></div>
                     <div class="owl-dot"><span></span></div>
                     <div class="owl-dot"><span></span></div>
                  </div>
               </div>
            </div>
         </div>
      </div>
   </section>

<script>
      $('.carousel-1').owlCarousel({
         loop: true,
         margin: 20,
         nav: true,
         dots: false,
         autoplay: true,
         autoplayTimeout: 3000,
         autoplaySpeed: 1000,
         navText: ['<i class="fa fa-angle-left" aria-hidden="true"></i>', '<i class="fa fa-angle-right" aria-hidden="true"></i>'],
         responsive: {
            0: {
               items: 1
            },
            600: {
               items: 1
            },
            1000: {
               items: 2
            }
         }
      })
   </script>
```


2. <b>Scroll To Top</b> 

```html
  <a href="#" class="scrollToTop"><i class="fad fa-arrow-alt-to-top"></i></a>
  <!-- scrollToTop -->
  <script src="./scrollToTop.js"

```

```css

.scrollToTop {
  padding: 8px;
  border-radius: 30px;
  text-align: center;
  background: transparent;
  border: 2px solid green;
  font-size: 18px;
  color: green;
  text-decoration: none;
  position: fixed;
  bottom: 25px;
  right: 40px;
  display: none;
  z-index: 1000;
  transform: rotate(180deg);
  transition: 0.3s ease-in-out;
}

.scrollToTop:hover {
  text-decoration: none;
  color: white;
  background: green;
}

```

```js


$(document).ready(function () {

   // if the window is top if not then display button
   
   $(window).scroll(function () {
      if ($(this).scrollTop() > 100) {
      $('.scrollToTop').fadeIn();
      } else {
      $('.scrollToTop').fadeOut();
      }
   });
   
   // scroll to top
   
   $('.scrollToTop').click(function () {
      $('html, body').animate({ scrollTop: 0 }, 800);
      return false;
   });

});


```

3. <b>Image card overlay</b> 

```html
<style>

</style>
.card {
  position: relative;
}
.card img{
  vertical-align: middle;
}
.card .card-overlay {
  position: absolute;
  top: 0;
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: center;
  flex-direction: column;
  align-items: center;
  background: var(--primary);
  color: var(--black);
  width: 100%;
  text-align: center;
  opacity: 0;
  cursor: pointer;
  transition: 0.2s ease-in-out;
}
.card .card-overlay h5 {
  font-size: 17px;
  font-weight: 500;
  line-height: normal;
}
.card .card-overlay p {
  font-size: 16px;
  font-weight: 400;
  line-height: normal;
  margin-bottom: 0px;
}
.card .card-overlay span {
  font-size: 14px;
  font-weight: 400;
  line-height: normal;
}
.card:hover > .card-overlay {
  opacity: 1;
}


<a href="#">
                        <div class="card">
                           <img src="./images/projects/img1.jpg" class="card-img-top" alt="...">
                           <div class="card-body">
                              <h5 class="card-title">Project Name Comes Here</h5>
                              <div class="d-flex justify-content-between">
                                 <p class="card-text">
                                    <i class="fas fa-map-marker-alt"></i> Location
                                 </p>
                                 <p class="card-text">
                                    Project Category
                                 </p>
                              </div>
                           </div>
                           <div class="card-overlay">
                              <h5>Project Name Comes Here</h5>
                              <p>Kozhikode</p>
                              <span>Project Category</span>
                           </div>
                        </div>
                     </a>
```
