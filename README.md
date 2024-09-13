# portaldenoticias

<!DOCTYPE HTML>
<html lang="pt-br">
	<head>
		<meta charset="UTF-8">

		<title>Portal de not?ias</title>
		
		<!-- JQuery -->
		<script src="js/jquery-2.2.1.js"></script>

		<!-- bootstrap - link cdn -->
		<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.6/css/bootstrap.min.css" integrity="sha384-1q8mTJOASx8j1Au+a5WDVnPi2lkFfwwEAa8hDDdjZlpLegxhjVME1fgjWPGmkzs7" crossorigin="anonymous">
	
		<!-- incluindo css -->
		<link href="css/style.css" rel="stylesheet">

		<!-- favicon -->
		<link rel="shortcut icon" href="images/favicon.ico" />
	</head>

	<body>

		<nav class="navbar navbar-default navbar-static-top">
			<div class="container">
				<div class="navbar-header">
					<button type="button" class="navbar-toggle collapsed" data-toggle="collapse" data-target="#navbar" aria-expanded="false" aria-controls="navbar">
						<span class="sr-only">Toggle navigation</span>
						<span class="icon-bar"></span>
						<span class="icon-bar"></span>
						<span class="icon-bar"></span>
					</button>
					
					<img src="images/logo.png" />
				</div>

				<div id="navbar" class="navbar-collapse collapse">
					<ul class="nav navbar-nav navbar-right">
						<li><a href="index.html">HOME</a></li>
					</ul>
				</div>
			</div>
		</nav>


	    <div class="container">
	    	<div class="row">
	    		<div class="col-md-8">
	    			<div class="noticia_wrapper">
		    			<span class="noticia_autor"><%= noticias[0].autor %></span>
		    			<a href="noticia?id_noticia=<%= noticias[0].id_noticia %>" class="noticia_titulo"><%= noticias[0].titulo %></a>
		    			<span class="noticia_data"><%= noticias[0].data_noticia %></span>
		    			<br />
		    			<p class="noticia_resumo">
		    				<%= noticias[0].resumo %>
		    			</p>
		    		</div>
		    	</div>

	    		<div class="col-md-4">
	    			<div class="noticia_wrapper">
		    			<span class="noticia_autor"><%= noticias[1].autor %></span>
		    			<a href="noticia?id_noticia=<%= noticias[1].id_noticia %>" class="noticia_titulo"><%= noticias[1].titulo %></a>
		    			<span class="noticia_data"><%= noticias[1].data_noticia %></span>

		    			<br />
		    			<p class="noticia_resumo">
		    				<%= noticias[1].resumo %>
		    			</p>
		    		</div>
		    	</div>
	    	</div>

	    	<div class="row">
	    		<% for(var i = 2; i < noticias.length; i++) {%>
		    		<div class="col-md-4">
		    			<div class="noticia_wrapper">
			    			<span class="noticia_autor"><%= noticias[i].autor %></span>
			    			<a href="noticia?id_noticia=<%= noticias[i].id_noticia %>" class="noticia_titulo"><%= noticias[i].titulo %></a>
			    			<span class="noticia_data"><%= noticias[i].data_noticia %></span>
			    			<br />
			    			<p class="noticia_resumo">
			    				<%= noticias[i].resumo %>
			    			</p>
			    		</div>
			    	</div>

			    <% } %>
	    	</div>

	    	<div class="row ver_mais">
	    		<button type="button" class="btn btn-default"><a href="noticias">Ver todas as noticias</a></button>
	    	</div>

	    </div>
	
		<script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.6/js/bootstrap.min.js" integrity="sha384-0mSbJDEHialfmuBBQP6A4Qrprq5OVfW37PRR3j5ELqxss1yVqOtnepnHVP9aJ7xS" crossorigin="anonymous"></script>
	
	</body>
</html>
