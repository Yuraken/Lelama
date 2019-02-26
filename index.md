<html>
<head>
	<meta charset="utf-8">
	<title>TP 2 Lazy Load</title>
	<style type="text/css">

		body{
		margin: 0;

		}
		.meublage{
			height: 100vh;
		}
	</style>
</head>
<body>
	<div class="scroll" >
		<div class="Le meublage">
			
		</div>
		<div class="Le meublage">
			
		</div>
		<div class="Le meublage">
			
		</div>
		<img data-lazy=https://previews.123rf.com/images/annamoskvina/annamoskvina1604/annamoskvina160400233/55833475-llama-lama-smile-and-for-fun-children.jpg alt="Une belle image" style="height: 400px; width: 200px;">


	</div>
	

</body>
<script type="text/javascript">
	window.addEventListener("scroll", lazy);
        
        function lazy(){
            document.querySelectorAll("[data-lazy]").forEach(function(img){
                if(img.getBoundingClientRect().y < window.innerHeight + 300){
                    img.src = img.dataset.lazy;
                    img.removeAttribute("data-lazy");
                }
            });
        }
        
        lazy();

</script>
</html>
