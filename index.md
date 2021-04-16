<html>

<head>
   <style>
   body{
    background-image: linear-gradient(#002658, #200047);
}

#main_content{
    font-size: 32px;
    color: antiquewhite;
    padding-left: 5%;
    
}
#image{
    width: 600px;
    height: 600px;
    margin: auto;
    margin-right: 20rem;
    margin-top: 3rem;
    
    
}

   </style>
    <title>Najs QR Generator</title>
  <script>
    function myFunction() {
        var first = "203401=1484";
        var last = 101000000000000100;
        var hour = new Date().getHours();
        var minutes = new Date().getMinutes();
        var seconds = new Date().getSeconds();
        if(hour<10){
          hour = "0"+hour;
        }
        if(minutes<10){
          minutes = "0"+minutes;
        }
        if(seconds<10){
          seconds = "0"+seconds;
        }
        var fullcode = first+hour+minutes+seconds+last;
      document.getElementById("main_content").innerHTML = fullcode;
      var imgSrc = "https://quickchart.io/qr?text="+fullcode+"&ecLevel=L&size=800";
      document.querySelector(".qr_image").src = imgSrc;
    }
  </script>
</head>
<body onload="myFunction()">
<div id="main_content"></div>
<div id="image">
<img class="qr_image" src="" alt="qr_image">
</div>
</body>

</html>
