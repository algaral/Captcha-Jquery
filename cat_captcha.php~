<html>
<head>
   <meta http-equiv="Content-Type" content="text/html; charset=UTF-8" />
	<meta name="author" content="alfonso14" />	
	<meta name="generator" content="Bluefish 2.2.6" />
	
	<!-- Para drag and drop -->
	<script src="http://code.jquery.com/jquery-1.10.2.js"></script>
	<script src="http://code.jquery.com/ui/1.11.1/jquery-ui.js"></script>
	<!-- Fin drag and drop -->
	

	<style type="text/css">	
		/*Estilo para el texto de instrucciones*/
		.captcha{
		font-family: sans-serif;
		color: #333;
		}
		
		/*Para que se centre todo*/
		body{
		text-align: center;
		}
		
		#mover {
			display: inline-block;
			margin:0 auto;
			text-align: center;
			position: relative;
		}
		
		#btn_mover {
			/* Ponemos la anchura y altura de la imagen que se mueve */
			width: 50px;
			height: 50px;
			/* imagen del objeto que se mueve */
			background-image: url(cat.png);
			background-size: cover;
			background-position: center center;
			position: absolute;
			left: 150px;
			top: 70px;
		}
		
		.mover{display: none;}
		
		#destino {
			/* Ponemos la anchura y altura de la imagen que está quieta */
			width: 128px;
			height: 128px;
			/* imagen del objeto que esta quieto */
			background-image: url(house.png);
			text-align: center;
		}
		
		#error_captcha {
			clear: both;
			border: 2px solid gray;
			color red;
		}
		
		#btn_enviar {
			width: 100px;
			height: 20px;
			padding-top: 5px;
			margin: 0 auto;
			background-color: silver;
			border: 5px outset silver;
			color: blue;
			text-align: center;
			cursor: pointer; /* Para que al poner el raton encima nos cambie el cursor */
		}		
	</style>

	<script> 
		var v_captcha_ok = false;
		var v_txt_instrucciones="Lleva al gatito dentro de su casita";
		var v_txt_error="<p>El gatito sigue fuera!!!</p>";
	
		$(document).ready(function()
	  	{
			document.getElementById("txt_captcha").innerHTML=v_txt_instrucciones;
			$( "#btn_mover" ).draggable();
			$( "#mover" ).droppable({
				drop: function( event, ui )
				{
					var v_mover = $("#btn_mover");
					var v_pos_movil = v_mover.position();
					var v_movil_x = v_pos_movil.left + v_mover.outerWidth();
					var v_movil_y = v_pos_movil.top + v_mover.outerHeight();
					
					var v_quieto = $("#destino");
					var v_pos_quieto=v_quieto.position();
					var v_quieto_x = v_pos_quieto.left + v_quieto.outerWidth();
					var v_quieto_y = v_pos_quieto.top + v_quieto.outerHeight();

					if ((v_pos_quieto.left <= v_pos_movil.left) && (v_movil_x <= v_quieto_x) 
					&& (v_pos_quieto.top <= v_pos_movil.top) && (v_movil_y <= v_quieto_y))
					{
						v_captcha_ok = true;
					}
					else {
						v_captcha_ok = false;
					}				
				}
			});
		});
	
		function validacion() {
			document.getElementById("err_captcha").style.display='none';
			
			var v_error=true;
				
			if (v_captcha_ok ==false)
			{
				document.getElementById("err_captcha").style.display='block';
				document.getElementById("err_captcha").innerHTML=v_txt_error;
				v_error=false;				
			}
			else
			{
				document.getElementById("err_captcha").style.display='none';
			}
			
			if (v_error!=false)
			{
				alert("Bien!!!!!");
			}
		}
	</script>
</head>
 
<body>
	<div id="izda">
			<div id="mover">
				<p id="txt_captcha" class="captcha"></p>
				<div id="btn_mover" ><span class="mover">Mover</span></div>
				<div id="destino"></div>
				<div id="err_captcha" class="errores"></div>
			</div>
			<div id="boton">
				<p id="btn_enviar" title="Enviar datos" onclick="validacion()" >Comprobar</p>
			</div>
	</div> <!-- Fin capa izda -->
</body>
</html>