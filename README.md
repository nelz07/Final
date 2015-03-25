# Final

<!DOCTYPE html>
<html>
	<head>
	
	<!-- JQM and CSS design of page -->
		<link rel="stylesheet" href="css/jquery.mobile-1.2.0.min.css" />
		<script src="js/jquery-1.8.2.min.js"></script>
		<script src="js/jquery.mobile-1.2.0.min.js"></script>
		<script>
		
		
		<!-- Date of dead function -->

		function getRandomDate(from, to) {
		
<!-- Validation -->
		
		if(document.getElementById('txt1').value==""){
		alert("Please Fill the required data")}	
		else if(document.getElementById('txt2').value==""){
		alert("Please Fill the required data")}
		else if(document.getElementById('txt3').value==""){
		alert("Please Fill the required data")}
		else if(document.getElementById('txt4').value==""){
		alert("Please Fill the required data")}
	else		{
	
	<!-- Get the random date -->
	
    if (!from) {
        from = new Date(2015, 0, 1).getTime();
    } else {
        from = from.getTime();
    }
    if (!to) {
        to = new Date(2100, 0, 1).getTime();
    } else {
        to = to.getTime();
    }
    dateto =  new Date(from + Math.random() * (to - from));
	document.getElementById('try1').innerHTML ="Base on given health information you will be dead at " +" <br>"+ "<img src='images/images.jpg' height='180' width='200' position='center' />"+ "<br>" + dateto;
	document.getElementById('try').disabled=true;
	}
}


	function again1(){
			document.getElementById('try').disabled=false;
			document.getElementById('try1').value="Results";
			
			}
<!--Exit Application-->
   function exitFromApp()
       {
            window.close();
       }


</script>
		
	<!-- Fade in Fade out of Results -->	
		
		<script>
	$(document).ready(function(){
    $(".datedeath").click(function(){
        $("p").fadeOut();
		$("p").fadeIn();
    });
    $(".choice").click(function(){
         $("p").fadeOut();
		$("p").fadeIn();
    });
});
</script>
	</head>


	
	<body>
	

<!-- Home Page -->


	<div data-role="page" data-theme="b" id="home">
	<center> <img src="images/Nelson.jpg" height="390px" width="100%" ></center>
		<div data-role="header" data-theme="e">
			<h1>Your Fortune teller</h1>
	
		</div>
	
		<div data-role="content">
			<a data-transition="flip" href="#like"><button class=choice" id="choice" >LookaLike</button></a>
			<a data-transition="flip" href="#datepage"><button class="datedeath" id="datedeath">Date of Death</button></a>
			<button onClick="exitFromApp()">Exit</button>
	
<!-- API -->


<center><iframe src="http://www.facebook.com/plugins/like.php?href=https://www.facebook.com/pages/IPredict/652476734857841&amp;
width=500&amp;layout=standard&amp;action=like&amp;show_faces=false&amp;share=true&amp;height=30"
     scrolling="no"
     frameborder="0"
     allowTransparency="true"></center>
</iframe>	
		</div>
		<div data-role="footer" data-position="fixed">

		</div>
	</div>
	
<!-- Page for the date of death -->	
	
	
	<div data-role="page" data-theme="b" id="datepage">
		<div src="images/Nelson.jpg" data-role="header" data-theme="e">
		<center> <img src="images/Rip.jpg" height="200px" width="100%" ></center>
			<h1>Are you scared of Death?</h1>
	
		</div>
	
		<div data-role="content">
			<b><p>Enter Height<input id="txt1" type="text"></p>
			<p>Enter Weight<input id="txt2" type="text"></p>
			<p>Enter Blood Type<input id="txt3" type="text"></p>
			<p>Enter Illness<input id="txt4" type="text"></p>
			<p>Gender<select id="txtOne"><br>
				<option value="Male">Male</option>
				<option value="Female">Female</option>
			</select></p>
			<center><p id="try1">Results<center></p>
			<button onClick="getRandomDate()" id="try">Predict</button>
			<button onClick="again1()">Try again</button>
			<a data-transition="flip" href="#home"><button>Back</button></a></b>
			
	

		</div>
		<div data-role="footer" data-position="fixed">
		</div>
	</div>
	
	<!-- Page of look a like -->
	
	
	<div data-role="page" data-theme="b" id="like">
	<center><img src="images/like.jpg" height="200px" width="100%"></center>	
		<div data-role="header" data-theme="e">
			<h1>Who will it be??</h1>
		</div>
		<div data-role="content">
		<b><center><p>WARNING THIS LOOK A LIKE IS NOT BASE ON GENDER</p></center></b>
		<b><p>Gender<select id="txtone"><br>
				<option value="Male">Male</option>
				<option value="Female">Female</option>
			</select></p>
			<p>Eyes Color<select id="txttwo"><br>
				<option value="black">Black</option>
				<option value="brown">Brown</option>
				<option value="blue">Blue</option>
			</select></p>
			<p>Skin Color<select id="txtthree"><br>
				<option value="black">Black</option>
				<option value="brown">Brown</option>
				<option value="white">White</option>
			</select></p>
			<p>Zodiac Sign<select id="txtthree"><br>
				<option value="black">Aries</option>
				<option value="brown">Taurus</option>
				<option value="white">Gemini</option>
				<option value="black">Leo</option>
				<option value="brown">Cancer</option>
				<option value="white">Virgo</option>
				<option value="black">Libra</option>
				<option value="brown">Scorpio</option>
				<option value="white">Pisces</option>
				<option value="white">Sagittarius</option>
				<option value="white">Capricorn</option>
			</select></p>
			<b><center><p id="try3">Results</p></center></b>
			<button onClick="choice()" id="hahaha">Predict</button>
			<button onClick="again()">Try again</button>
			<a data-transition="flip" href="#home"><button>Back</button></a></b>
			
			
			<!-- Array of Kalokalike also function that will determine who will it be? -->
			
			<script>
	function choice(){
			imagens = new Array();
			imagens[0]="<img src='images/1.jpg' width='300' height='200' />"
			imagens[1]="<img src='images/2.jpg' width='300' height='200' />"
			imagens[2]="<img src='images/3.jpg' width='300' height='200' />"
			imagens[3]="<img src='images/4.jpg' width='300' height='200' />"
			imagens[4]="<img src='images/5.jpg' width='300' height='200' />"
			imagens[5]="<img src='images/6.jpg' width='300' height='200' />"
			imagens[6]="<img src='images/7.jpg' width='300' height='200' />"
			imagens[7]="<img src='images/8.jpg'  width='300' height='200' />"
			imagens[8]="<img src='images/9.jpg' width='300' height='200' />"
			imagens[9]="<img src='images/10.jpg' width='300' height='200' />"
			imagens[10]="<img src='images/11.jpg' width='300' height='200' />"
			imagens[11]="<img src='images/12.jpg' width='300' height='200' />"
			imagens[12]="<img src='images/13.jpg' width='300' height='200' />"
			imagens[13]="<img src='images/14.jpg'  width='300' height='200' />"
			imagens[14]="<img src='images/15.jpg' width='300' height='200' />"
			imagens[15]="<img src='images/16.jpg' width='300' height='200' />"
			imagens[16]="<img src='images/17.jpg' width='300' height='200' />"
			imagens[17]="<img src='images/18.jpg' width='300' height='200' />"
			imagens[18]="<img src='images/19.jpg' width='300' height='200' />"
			imagens[19]="<img src='images/20.jpg' width='300' height='200' />"
			imagens[20]="<img src='images/21.jpg' width='300' height='200' />"
			imagens[21]="<img src='images/22.jpg' width='300' height='200' />"
			imagens[22]="<img src='images/23.jpg' width='300' height='200' />"
			imagens[23]="<img src='images/24.jpg' width='300' height='200' />"
			imagens[24]="<img src='images/25.jpg' width='300' height='200' />"
			imagens[25]="<img src='images/26.jpg' width='300' height='200' />"
			imagens[26]="<img src='images/27.jpg' width='300' height='200' />"
			imagens[27]="<img src='images/28.jpg'  width='300' height='200' />"
			imagens[28]="<img src='images/29.jpg' width='300' height='200' />"
			imagens[29]="<img src='images/30.jpg' width='300' height='200' />"
			imagens[30]="<img src='images/31.jpg' width='300' height='200' />"
			imagens[31]="<img src='images/32.jpg' width='300' height='200' />"
			imagens[32]="<img src='images/33.jpg' width='300' height='200' />"
			imagens[33]="<img src='images/34.jpg' width='300' height='200' />"
			imagens[34]="<img src='images/35.jpg' width='300' height='200' />"
			imagens[35]="<img src='images/36.jpg' width='300' height='200' />"

			var randNum = Math.floor(Math.random()*imagens.length);
			
			document.getElementById('try3').innerHTML="Base on  the given information you look like"+"<br>" + imagens[randNum];
			document.getElementById('hahaha').disabled=true;
				}
				
			function again(){
			document.getElementById('try3').value="Results";
			document.getElementById('hahaha').disabled=false;
			}
</script>
		</div>
		<div data-role="footer" data-position="fixed">

		</div>
	</div>
	
	</body>
</html>
