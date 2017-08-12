

<!DOCTYPE html>
<html>
<head>


<script type="text/javascript" src="http://code.jquery.com/jquery-1.6.4.min.js"></script>



<script type="text/javascript">
$(document).ready(function() {
var monthNames = [ "January", "February", "March", "April", "May", "June", "July", "August", "September", "October", "November", "December" ]; 
var dayNames= ["Sunday","Monday","Tuesday","Wednesday","Thursday","Friday","Saturday"]


var newDate = new Date();

newDate.setDate(newDate.getDate());   
$('#Date').html(dayNames[newDate.getDay()] + " " + newDate.getDate() + ' ' + monthNames[newDate.getMonth()] + ' ' + newDate.getFullYear());

setInterval( function() {
	
	var seconds = new Date().getSeconds();
	
	$("#sec").html(( seconds < 10 ? "0" : "" ) + seconds);
	},1000);
	
setInterval( function() {
	
	var minutes = new Date().getMinutes();
	
	$("#min").html(( minutes < 10 ? "0" : "" ) + minutes);
    },1000);
	
setInterval( function() {
	var hours = new Date().getHours();
	
	$("#hours").html(( hours < 10 ? "0" : "" ) + hours);
    }, 1000);	
});
</script>
</head>



<body>
<div class="clock">
<div id="Date"></div>
  <ul>
      <li id="hours"></li>
      <li id="point">:</li>
      <li id="min"></li>
      <li id="point">:</li>
      <li id="sec"></li>
  </ul>
</div>
</body>

<style>
@font-face {
    font-family: 'BebasNeueRegular';
    src: url('BebasNeue-webfont.eot');
    src: url('BebasNeue-webfont.eot?#iefix') format('embedded-opentype'),
         url('BebasNeue-webfont.woff') format('woff'),
         url('BebasNeue-webfont.ttf') format('truetype'),
         url('BebasNeue-webfont.svg#BebasNeueRegular') format('svg');
    font-weight: normal;
    font-style: normal;
}

.container {
    width: 960px;
    margin: 0 auto;
    overflow: hidden;
}

.clock {
    width: 800px;
    margin: 0 auto;
    padding: 30px;
    border: 1px solid #333;
    color: #fff;
}

#Date {
    font-family: 'BebasNeueRegular', Arial, Helvetica, sans-serif;
    font-size: 36px;
    text-align: center;
    text-shadow: 0 0 5px #00c6ff;
}

ul {
    width: 800px;
    margin: 0 auto;
    padding: 0px;
    list-style: none;
    text-align: center;
}

ul li {
    display: inline;
    font-size: 10em;
    text-align: center;
    font-family: 'BebasNeueRegular', Arial, Helvetica, sans-serif;
    text-shadow: 0 0 5px #00c6ff;
}

#point {
    position: relative;
    -moz-animation: mymove 1s ease infinite;
    -webkit-animation: mymove 1s ease infinite;
    padding-left: 10px;
    padding-right: 10px;
}


@-webkit-keyframes mymove {
    0% {opacity: 1.0;
    text-shadow: 0 0 20px #00c6ff;
}

50% {
    opacity: 0;
    text-shadow: none;
}

100% {
    opacity: 1.0;
    text-shadow: 0 0 20px #00c6ff;
}	
}

@-moz-keyframes mymove {
    0% {
        opacity: 1.0;
        text-shadow: 0 0 20px #00c6ff;
    }

    50% {
        opacity: 0;
        text-shadow: none;
    }

    100% {
        opacity: 1.0;
        text-shadow: 0 0 20px #00c6ff;
    };
}
</style>
</html>
