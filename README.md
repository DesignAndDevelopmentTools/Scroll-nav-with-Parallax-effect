# Scroll-nav-with-Parallax-effect
> Scroll nav with Parallax effect


> # 1. Just write code (HTML):
```s
   <header>
      <div class="scroll-top"> 
        <div class="scroll-top-bg"> </div>
      </div>

         <nav class="navbar navbar-default navbar-fixed-top scrollNavEffectshow transition">
         .....
         </nav>
    </header>
```

> #  2. Just write code (CSS):
```s
 <style type="text/css">
    *{
      margin: 0px;
      padding: 0px;
    }
    .scroll-top{
      position: relative;
      width: 100%;
      height:100vh;
      background-color: #333;
      overflow: hidden;
    }
    .scroll-top-bg{
      position:absolute;
      width:100%;
      height:300%;
      background-size: 200% 100%;
      background-image: url('img/banner_parallax.jpg');
      background-repeat: no-repeat;
      background-position: center center;
      margin-top: 0px;
    }
    .nav-bg {
      background: transparent;
      border:none;
      width: 100%;
      opacity: 0.8;
    }
    .nav-bg li a,.navbar-brand{
      padding: 30px 20px;
      color:white!important;
    }
    .scrollNavEffectshow {
      opacity: 0.8;
      background: teal;
    }
    .scrollNavEffectshow a{
      color:white!important;
    }
    .active a{
      background-color:black!important;
    }

    .transition {    
      -webkit-transition: all 0.8s ease-in-out;
      -moz-transition: all 0.8s ease-in-out;
      -o-transition: all 0.8s ease-in-out;
      transition: all 0.8s ease-in-out;
    }

  </style>
```

> # 3. Just write code (JavaScript):
```s
<script type="text/javascript">
  $(window).scroll(function() {
    var scrollTop = $(this).scrollTop();
    $('.scroll-top-bg').css('top', -(scrollTop * 2) + 'px');

    if ($(window).scrollTop() > 500 ){
      $('.bg').addClass('scrollNavEffectshow');
    } else {
      $('.bg').removeClass('scrollNavEffectshow');
    };    
  });
 
  </script>
```

> # 4. Then view result in your Browser.
