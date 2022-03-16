# GBR-NETWORK


<!DOCTYPE html>
<html>
<head>
<!-- Website name | ชื่อเว็บไซต์ -->
<title>GBR NETWORK</title>
<!-- Website icon | ไอคอนเว็บไซต์ -->
<!-- href="https://api.mcsrvstat.us/icon/ip-server-you > -->
<!-- href="https://api.mcsrvstat.us/icon/ใส่ไอพีเซิร์ฟเวอร์ > -->
<link rel="icon" href="https://api.mcsrvstat.us/icon/hypixel.net">
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<link rel="stylesheet" type="text/css" href="./styles.css">
<link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.4.1/css/bootstrap.min.css" integrity="sha384-Vkoo8x4CGsO3+Hhxv8T/Q5PaXtkKtu6ug5TOeNV6gBiFeWPGFN9MuhOf23Q9Ifjh" crossorigin="anonymous">
<script src="https://kit.fontawesome.com/e198ddcfbb.js" crossorigin="anonymous"></script>
<script src="http://code.jquery.com/jquery-3.4.1.js"></script>
<script type="text/javascript">

      /* If you not understand, do not fix | หากไม่เข้าใจ ไม่แนะนำให้แก้ไข */
  $(document).ready(function(){
    $('.menu').click(function(){
      $('.button-box').toggleClass('active');
    })
  })

      /* If you not understand, do not fix | หากไม่เข้าใจ ไม่แนะนำให้แก้ไข */
  function myFunction() {
    alert("Copy success | Join now. I'm waiting for you.");
  }

      /* If you not understand, do not fix | หากไม่เข้าใจ ไม่แนะนำให้แก้ไข */
  function copyip(element) {
    var $temp = $("<input>");
    $("body").append($temp);
    $temp.val($(element).text()).select();
    document.execCommand("copy");
    $temp.remove();
  }
        /* For this box, edit only ip. | สำหรับช่องนี้แก้ไขเฉพาะ ip */
	 /* example | ตัวอย่าง  edit > (let url = "hypixel.net";) to (let url = "ip address";) */
  let url = "hypixel.net";
  $(document).ready(() => {
      $.getJSON("https://api.mcsrvstat.us/1/" + url, (status) => {
          if (status.debug.ping) {
              $("#motd").append(status.motd.raw);
              $("#status").append("online");
              $("#version").append(status.version);
              $("#players_num").append(status.players.online + "/" + status.players.max)
              $.each(status.players.list, function (index, player) {
                  $("#players_list").append("<li>" + player + "</li>")
              });
          } else {
              $("#motd").append(status.hostname);
              $("#status").append("offline");
              $("#version").hide();
              $("#players_num").hide();
          }
          $("body").fadeIn(2000);
      });
  });

</script>
</head>
<body>

<!-- Navigation bar | แถบนำทาง -->
<div class="header">
  <div class="sv-name-and-menu">
    <a class="server-name" href="./index.html">server name</a>
    <a class="toggle menu" style="color:#fff;">MENU</a>
  </div>

  <div class="button-box">
    <ul>
      <li><a href="#Set-link-ตั้งค่าลิงก์">webshop</a></li>
      <li><a href="#Set-link-ตั้งค่าลิงก์">discord</a></li>
      <li><a href="#Set-link-ตั้งค่าลิงก์">fb page</a></li>
      <li><a href="#Set-link-ตั้งค่าลิงก์">fb group</a></li>
    </ul>
  </div>
</div>

<!-- background | พื้นหลัง, ภาพพื้นหลัง -->
<div class="bg">

  <div class="container">
   <div class="row">
     <div class="col-sm-12 wellcome">
       <!-- Server icon | ไอคอน เซิร์ฟเวอร์ -->
         <div class="icon">
           <img src="https://api.mcsrvstat.us/icon/hypixel.net" alt="Erros">
         </div>

       <!-- Logo | โลโก้ -->
         <div class="logo">
         <img src="./img/logo.png" alt="Erros">
         </div>

         <!-- Information and status | ข้อมูลและสถานะ -->
         <div class="info-and-status">
           <h1>Hypixel server <span id="status"></span>!</h1> <br>
           <h1>Join now</h1> <br>
           <span id="players_num">Players: </span> <p id="version">Version: </p>
         </div>

         <!-- server ip | ip ของเซิร์ฟเวอร์ -->
       <!-- edit <p id="p1">mc-server-name.com</p> to <p id="p1">Server name</p> -->
       <!-- แก้ไข <p id="p1">mc-server-name.com</p> เป็น <p id="p1">ชื่อเซิร์ฟเวอร์</p> -->
         <div class="server-ip">
         <img src="https://api.mcsrvstat.us/icon/hypixel.net" alt="Erros">
         <p id="p1">mc-server-name.com</p>
         <button class="btn-computer" onclick="copyip('#p1');myFunction();"><i class="far fa-copy"></i></button>
         <button class="btn-mobile" onclick="copyip('#p1');myFunction();"><i class="far fa-copy"></i></button>
         </div>

         <hr>
         <p>The Hypixel Network is a Minecraft mini-game server, released on April 13, 2013, by Simon Collins-Laflamme and Philippe Touchette, and is managed by Hypixel Inc. Hypixel is only available on the Java Edition of Minecraft.
         <a href="https://en.wikipedia.org/wiki/Hypixel" target="_blank">Read more..</a></p>
     </div>
   </div>
  </div>

<!-- If you have conscience, you should not edit or delete name of developer. -->
<!-- หากคุณมีมโนธรรม คุณไม่ควรแก้ไขหรือลบชื่อผู้พัฒนา -->
<footer>
  <div class="center-s-d">
    <div class="skills">develop skills only <a href="https://bit.ly/3bTSktw" target="_blank">(free download)</a></div>
    <div class="designed">Designed by <a href="https://www.facebook.com/THETOPTHAILAND1107" target="_blank">anuwat avera</a></div>
  </div>
</footer>

</div>

</body>
</html>
