# Advanced-Styling-with-Responsive-Design
Responsive photo gallery using the grid system of Bootstrap and custom jQuery for the modal


index.html


<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="">
    <meta name="author" content="">
    <title>Responsive Photo Gallery </title>
    <link href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.5/css/bootstrap.min.css" rel="stylesheet">
    <link href="jquery.bsPhotoGallery.css" rel="stylesheet">
    <script src="//code.jquery.com/jquery-1.10.2.min.js"></script>
    <script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.5/js/bootstrap.min.js"></script>
    <script src="jquery.bsPhotoGallery.js"></script>
  </head>
  <style>
      ul {
          padding:0 0 0 0;
          margin:0 0 0 0;
      }
      ul li {
          list-style:none;
          margin-bottom:25px;
      }
      ul li img {
          cursor: pointer;
      }
      .modal-body {
          padding:5px !important;
      }
      .modal-content {
          border-radius:0;
      }
      .modal-dialog img {
          text-align:center;
          margin:0 auto;
      }
    .controls{
        width:50px;
        display:block;
        font-size:11px;
        padding-top:8px;
        font-weight:bold;
    }
    .next {
        float:right;
        text-align:right;
    }
      /*override modal for demo only*/
      .modal-dialog {
          max-width:500px;
          padding-top: 90px;
      }
      @media screen and (min-width: 768px){
          .modal-dialog {
              width:500px;
              padding-top: 90px;
          }
      }
      @media screen and (max-width:1500px){
          #ads {
              display:none;
          }
      }
  </style>
  <body>
    <div class="container">
        <div class="row" style="text-align:center; border-bottom:1px dashed #ccc;  padding:0 0 20px 0; margin-bottom:40px;">
            <h3 style="font-family:arial; font-weight:bold; font-size:30px;">
                Responsive Photo Gallery
        </h3>
        </div>

        <ul class="row">
            <li class="col-lg-2 col-md-2 col-sm-3 col-xs-4">
                <img class="img-responsive" src="https://cdn.pixabay.com/photo/2015/12/01/20/28/road-1072823_960_720.jpg" data-content="data 1">
            </li>
            <li class="col-lg-2 col-md-2 col-sm-3 col-xs-4">
                <img class="img-responsive" src="https://image.shutterstock.com/image-photo/country-road-260nw-628141070.jpg" data-content="data 2">
            </li>
            <li class="col-lg-2 col-md-2 col-sm-3 col-xs-4">
                <img class="img-responsive" src="https://cdn.pixabay.com/photo/2015/06/19/21/24/the-road-815297__340.jpg" data-content='data 3'>
            </li>
            <li class="col-lg-2 col-md-2 col-sm-3 col-xs-4">
                <img class="img-responsive" src="https://cdn.pixabay.com/photo/2015/09/09/16/05/forest-931706__340.jpg" data-content="data 4">
            </li>
            <li class="col-lg-2 col-md-2 col-sm-3 col-xs-4">
                <img class="img-responsive" src="https://cdn.pixabay.com/photo/2015/01/28/23/35/landscape-615429__340.jpg" data-content="data 5">
            </li>
            <li class="col-lg-2 col-md-2 col-sm-3 col-xs-4">
                <img class="img-responsive" src="https://cdn.pixabay.com/photo/2018/01/14/23/12/nature-3082832__340.jpg" data-content="data 6">
            </li>
            <li class="col-lg-2 col-md-2 col-sm-3 col-xs-4">
                <img class="img-responsive" src="https://cdn.pixabay.com/photo/2016/11/14/04/45/elephant-1822636__340.jpg" data-content="data 7">
            </li>
            <li class="col-lg-2 col-md-2 col-sm-3 col-xs-4">
                <img class="img-responsive" src="https://cdn.pixabay.com/photo/2016/10/22/17/46/scotland-1761292__340.jpg" data-content="data 8">
            </li>
            <li class="col-lg-2 col-md-2 col-sm-3 col-xs-4">
                <img class="img-responsive" src="https://cdn.pixabay.com/photo/2018/09/23/18/30/drop-3698073__340.jpg" data-content="data 9">
            </li>
            <li class="col-lg-2 col-md-2 col-sm-3 col-xs-4">
                <img class="img-responsive" src="https://cdn.pixabay.com/photo/2014/08/01/00/08/pier-407252__340.jpg" data-content="data 10">
            </li>
            <li class="col-lg-2 col-md-2 col-sm-3 col-xs-4">
                <img class="img-responsive" src="https://cdn.pixabay.com/photo/2017/04/09/09/56/avenue-2215317__340.jpg" data-content="data 11">
            </li>
            <li class="col-lg-2 col-md-2 col-sm-3 col-xs-4">
                <img class="img-responsive" src="https://cdn.pixabay.com/photo/2016/03/27/22/22/fox-1284512__340.jpg" data-content="data 12">
            </li>
            <li class="col-lg-2 col-md-2 col-sm-3 col-xs-4">
                <img class="img-responsive" src="https://cdn.pixabay.com/photo/2018/05/30/00/24/thunderstorm-3440450__340.jpg" data-content="data 13">
            </li>
            <li class="col-lg-2 col-md-2 col-sm-3 col-xs-4">
                <img class="img-responsive" src="https://cdn.pixabay.com/photo/2016/12/27/21/03/lone-tree-1934897__340.jpg" data-content="data 14">
            </li>
            <li class="col-lg-2 col-md-2 col-sm-3 col-xs-4">
                <img class="img-responsive" src="https://cdn.pixabay.com/photo/2016/10/14/19/21/canyon-1740973__340.jpg" data-content="data 15">
            </li>
            <li class="col-lg-2 col-md-2 col-sm-3 col-xs-4">
                <img class="img-responsive" src="https://cdn.pixabay.com/photo/2017/01/14/12/59/iceland-1979445__340.jpg" data-content="data 16">
            </li>
            <li class="col-lg-2 col-md-2 col-sm-3 col-xs-4">
                <img class="img-responsive" src="https://cdn.pixabay.com/photo/2016/12/11/12/02/bled-1899264__340.jpg" data-content="data 17">
            </li>
            <li class="col-lg-2 col-md-2 col-sm-3 col-xs-4">
                <img class="img-responsive" src="https://cdn.pixabay.com/photo/2017/12/17/19/08/away-3024773__340.jpg" data-content="data 18">
            </li>
            <li class="col-lg-2 col-md-2 col-sm-3 col-xs-4">
                <img class="img-responsive" src="https://cdn.pixabay.com/photo/2018/01/22/14/13/animal-3099035__340.jpg" data-content="data 19">
            </li>
            <li class="col-lg-2 col-md-2 col-sm-3 col-xs-4">
                <img class="img-responsive" src="https://cdn.pixabay.com/photo/2016/11/12/11/51/forest-1818690__340.jpg" data-content="data 20">
            </li>
            <li class="col-lg-2 col-md-2 col-sm-3 col-xs-4">
                <img class="img-responsive" src="https://cdn.pixabay.com/photo/2013/07/25/01/31/sunlight-166733__340.jpg" data-content="data 21">
            </li>
            <li class="col-lg-2 col-md-2 col-sm-3 col-xs-4">
                <img class="img-responsive" src="https://cdn.pixabay.com/photo/2018/08/21/23/29/fog-3622519__340.jpg" data-content="data 22">
            </li>
            <li class="col-lg-2 col-md-2 col-sm-3 col-xs-4">
                <img class="img-responsive" src="https://cdn.pixabay.com/photo/2018/01/30/22/50/forest-3119826__340.jpg" data-content="data 23">
            </li>
            <li class="col-lg-2 col-md-2 col-sm-3 col-xs-4">
                <img class="img-responsive" src="https://cdn.pixabay.com/photo/2016/12/05/11/39/fox-1883658__340.jpg" data-content="data 24">
            </li>
          </ul>
    </div> <!-- /container -->


    <div class="modal fade" id="myModal" tabindex="-1" role="dialog" aria-labelledby="myModalLabel" aria-hidden="true">
      <div class="modal-dialog">
        <div class="modal-content">
          <div class="modal-body">
          </div>
        </div><!-- /.modal-content -->
      </div><!-- /.modal-dialog -->
    </div><!-- /.modal -->

  </body>

</html>



jquery.bsPhotoGallery.css

#bsPhotoGalleryModal .modal-content {
    border-radius:0;
}
#bsPhotoGalleryModal .modal-dialog img {
    text-align:center;
    margin:0 auto;
    width:100%;
}
#bsPhotoGalleryModal .modal-body {
    padding:0px !important;
}
#bsPhotoGalleryModal .bsp-close {
  position: absolute; 
  right: -14px; 
  top: -11px; 
  font-size: 30px; 
  color:#fff; 
  text-shadow: 1px 1px 18px #000;
}

#bsPhotoGalleryModal .bsp-close:hover {
  cursor: pointer;
  opacity:.6;
  text-shadow: none;
  
}
.bspHasModal {
  cursor: pointer;
}
.bspHasModal .text {
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}
.imgWrapper {
  overflow: hidden;
  max-height: 99px;
}

a.bsp-controls, 
a.bsp-controls:visited, 
a.bsp-controls:active {
  position: absolute;
  top: 44%;
  font-size: 26px;
  color: #fff;
  text-shadow: 1px 1px 18px #000;
}
a.bsp-controls.next {
  right:-10px;
}
a.bsp-controls.previous {
  left:-10px;
}
a.bsp-controls:hover {
  opacity:.6;
  text-shadow: none;
}
.bsp-text-container {
  clear:both;
  display:block;
  padding-bottom: 5px;
}
#bsPhotoGalleryModal h6{
  margin-bottom: 0;
  font-weight: bold;
  color: #000;
  font-size: 14px;
  padding-left: 12px;
  padding-right: 12px;
  margin-bottom: 5px;
}
#bsPhotoGalleryModal .pText {
  font-size: 11px;
  margin-bottom: 0px;
  padding: 0 12px 5px;
} 
 

@media screen and (max-width: 380px){
   .col-xxs-12 {
     width:100%;
   }
   .col-xxs-12 img {
     width:100%;
   }
}



jquery.bsPhotoGallery.js

(function($) {
  "use strict";
  $.fn.bsPhotoGallery = function(options) {

      var settings = $.extend({}, $.fn.bsPhotoGallery.defaults, options);
      var id = generateId();
      var classesString = settings.classes;
      var classesArray = classesString.split(" ");
      var clicked = {};

      function getCurrentUl(){
        return 'ul[data-bsp-ul-id="'+clicked.ulId+'"][data-bsp-ul-index="'+clicked.ulIndex+'"]';
      }
      function generateId() {
        //http://fiznool.com/blog/2014/11/16/short-id-generation-in-javascript/
        var ALPHABET = '0123456789abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ';
        var ID_LENGTH = 4;
        var out = '';
        for (var i = 0; i < ID_LENGTH; i++) {
          out += ALPHABET.charAt(Math.floor(Math.random() * ALPHABET.length));
        }
        return 'bsp-'+out;
      }
      function createModalWrap(){

        if($('#bsPhotoGalleryModal').length !== 0){
          return false;
        }

        var modal = '';
        modal += '<div class="modal fade" id="bsPhotoGalleryModal" tabindex="-1" role="dialog"';
        modal += 'aria-labelledby="myModalLabel" aria-hidden="true">';
        modal += '<div class="modal-dialog modal-lg"><div class="modal-content">';
        modal += '<div class="modal-body"></div></div></div></div>';
        $('body').append(modal);

      }
      function showHideControls(){
    		var total = $(getCurrentUl()+' li[data-bsp-li-index]').length;

    		if(total === clicked.nextImg){
    			$('a.next').hide();
    		}else{
    			$('a.next').show()
    		}
    		if(clicked.prevImg === -1){
    			$('a.previous').hide();
    		}else{
    			$('a.previous').show()
    		}
    	}
      function showModal(){

          var src = $(this).find('img').attr('src');
          var largeImg = $(this).find('img').attr('data-bsp-large-src');
          if(typeof largeImg === 'string'){
                src = largeImg;
          }
          var index = $(this).attr('data-bsp-li-index');
          var ulIndex = $(this).parent('ul').attr('data-bsp-ul-index');
          var ulId = $(this).parent('ul').attr('data-bsp-ul-id');
          var theImg = $(this).find('img');
          var pText = $(this).find('.text').html();        
          var modalText = typeof pText !== 'undefined' ? pText : 'undefined';
          var alt =  typeof theImg.attr('alt') == 'string' ? theImg.attr('alt') : null;
          
          clicked.img = src;
          clicked.prevImg = parseInt(index) - parseInt(1);
      		clicked.nextImg = parseInt(index) + parseInt(1);
          clicked.ulIndex = ulIndex;
          clicked.ulId = ulId;


          $('#bsPhotoGalleryModal').modal();

          var html = '';
          var img = '<img src="' + clicked.img + '" class="img-responsive"/>';

          html += img;
          html += '<span class="' + settings.iconClose + ' bsp-close"></span>';
          html += '<div class="bsp-text-container">';
          
          if(alt !== null){
            html += '<h6>'+alt+'</h6>'
          }
          if(typeof pText !== 'undefined'){
            html += '<p class="pText">'+pText+'</p>'
          }        
          html += '</div>';
          html += '<a class="bsp-controls next" data-bsp-id="'+clicked.ulId+'" href="'+ (clicked.nextImg) + '"><span class="' + settings.iconRight + '"></span></a>';
          html += '<a class="bsp-controls previous" data-bsp-id="'+clicked.ulId+'" href="' + (clicked.prevImg) + '"><span class="' + settings.iconLeft + '"></span></a>';
        
          $('#bsPhotoGalleryModal .modal-body').html(html);
          $('.bsp-close').on('click', closeModal);
          showHideControls();
      }

      function closeModal(){
        $('#bsPhotoGalleryModal').modal('hide');
      }

      function nextPrevHandler(){

          var ul = $(getCurrentUl());
          var index = $(this).attr('href');

          var src = ul.find('li[data-bsp-li-index="'+index+'"] img').attr('src');
          var largeImg = ul.find('li[data-bsp-li-index="'+index+'"] img').attr('data-bsp-large-src');
          if(typeof largeImg === 'string'){
                src = largeImg;
          } 
          
          var pText = ul.find('li[data-bsp-li-index="'+index+'"] .text').html();        
          var modalText = typeof pText !== 'undefined' ? pText : 'undefined';
          var theImg = ul.find('li[data-bsp-li-index="'+index+'"] img');
          var alt =  typeof theImg.attr('alt') == 'string' ? theImg.attr('alt') : null;
           
          $('.modal-body img').attr('src', src);
          var txt = '';
          if(alt !== null){
            txt += '<h6>'+alt+'</h6>'
          }
          if(typeof pText !== 'undefined'){
            txt += '<p class="pText">'+pText+'</p>'
          }        
          
          $('.bsp-text-container').html(txt); 

          clicked.prevImg = parseInt(index) - 1;
          clicked.nextImg = parseInt(clicked.prevImg) + 2;

          if($(this).hasClass('previous')){
              $(this).attr('href', clicked.prevImg);
              $('a.next').attr('href', clicked.nextImg);
          }else{
              $(this).attr('href', clicked.nextImg);
              $('a.previous').attr('href', clicked.prevImg);
          }
          // console.log(clicked);
        showHideControls();
        return false;
      }
      function clearModalContent(){
        $('#bsPhotoGalleryModal .modal-body').html('');
        clicked = {};
      }
      function insertClearFix(el,x){
        var index = (x+1);
        $.each(classesArray,function(e){
           switch(classesArray[e]){
             //large
             case "col-lg-1":
                  if($(el).next('li.clearfix').length == 0){
                    $(el).after('<li class="clearfix visible-lg-block"></li>');
                  }
              break;
             case "col-lg-2":
                if(index%6 === 0){
                  $(el).after('<li class="clearfix visible-lg-block"></li>');
                }
              break;
             case "col-lg-3":
              if(index%4 === 0){
                $(el).after('<li class="clearfix visible-lg-block"></li>');
              }
             break;
             case "col-lg-4":
              if(index%3 === 0){
                $(el).after('<li class="clearfix visible-lg-block"></li>');
              }
             break;
             case "col-lg-5":
             case "col-lg-6":
              if(index%2 === 0){
                $(el).after('<li class="clearfix visible-lg-block"></li>');
              }
             break;
             //medium
             case "col-md-1":
                  if($(el).next('li.clearfix').length == 0){
                    $(el).after('<li class="clearfix visible-md-block"></li>');
                  }
              break;
             case "col-md-2":
                if(index%6 === 0){
                  $(el).after('<li class="clearfix visible-md-block"></li>');
                }
              break;
             case "col-md-3":
              if(index%4 === 0){
                $(el).after('<li class="clearfix visible-md-block"></li>');
              }
             break;
             case "col-md-4":
              if(index%3 === 0){
                $(el).after('<li class="clearfix visible-md-block"></li>');
              }
             break;
             case "col-md-5":
             case "col-md-6":
              if(index%2 === 0){
                $(el).after('<li class="clearfix visible-md-block"></li>');
              }
             break;
             //small
             case "col-sm-1":
                  if($(el).next('li.clearfix').length == 0){
                    $(el).after('<li class="clearfix visible-sm-block"></li>');
                  }
              break;
             case "col-sm-2":
                if(index%6 === 0){
                  $(el).after('<li class="clearfix visible-sm-block"></li>');
                }
              break;
             case "col-sm-3":
              if(index%4 === 0){
                $(el).after('<li class="clearfix visible-sm-block"></li>');
              }
             break;
             case "col-sm-4":
              if(index%3 === 0){
                $(el).after('<li class="clearfix visible-sm-block"></li>');
              }
             break;
             case "col-sm-5":
             case "col-sm-6":
              if(index%2 === 0){
                $(el).after('<li class="clearfix visible-sm-block"></li>');
              }
             break;
             //x-small
             case "col-xs-1":
                  if($(el).next('li.clearfix').length == 0){
                    $(el).after('<li class="clearfix visible-xs-block"></li>');
                  }
              break;
             case "col-xs-2":
                if(index%6 === 0){
                  $(el).after('<li class="clearfix visible-xs-block"></li>');
                }
              break;
             case "col-xs-3":
              if(index%4 === 0){
                $(el).after('<li class="clearfix visible-xs-block"></li>');
              }
             break;
             case "col-xs-4":
              if(index%3 === 0){
                $(el).after('<li class="clearfix visible-xs-block"></li>');
              }
             break;
             case "col-xs-5":
             case "col-xs-6":
              if(index%2 === 0){
                $(el).after('<li class="clearfix visible-xs-block"></li>');
              }
             break;
           }
        });
      }


      this.each(function(i){
        //ul
        var items = $(this).find('li');
        $(this).attr('data-bsp-ul-id', id);
        $(this).attr('data-bsp-ul-index', i);

        items.each(function(x){
          var theImg = $(this).find('img'); 
          insertClearFix(this,x);
          $(this).addClass(classesString);
          $(this).attr('data-bsp-li-index', x);
          theImg.addClass('img-responsive');
          if(settings.fullHeight){
            theImg.wrap('<div class="imgWrapper"></div>')
          }
          if(settings.hasModal === true){
            $(this).addClass('bspHasModal');
            $(this).on('click', showModal);
          }
        });
      })

      if(settings.hasModal === true){
        //this is for the next / previous buttons
        $(document).on('click', 'a.bsp-controls[data-bsp-id="'+id+'"]', nextPrevHandler);
        $(document).on('hidden.bs.modal', '#bsPhotoGalleryModal', clearModalContent);
        //start init methods
        createModalWrap();
      }

      return this;
  };
  /*defaults*/
  $.fn.bsPhotoGallery.defaults = {
    'classes' : 'col-lg-2 col-md-2 col-sm-3 col-xs-4',
    'hasModal' : true, 
    'fullHeight' : true,
    'iconClose' : 'glyphicon glyphicon-remove-circle',
    'iconLeft' : 'glyphicon glyphicon-chevron-left',
    'iconRight' : 'glyphicon glyphicon-chevron-right'
  }


}(jQuery));
