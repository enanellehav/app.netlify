<!DOCTYPE html>
<html lang="en">
	<head>
		<meta charset="utf-8">
		<meta content="width=device-width, initial-scale=1, shrink-to-fit=no" name="viewport">
				
		<title>Chat with Amahle</title>
		
		<!-- css -->
		<link href="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/css/bootstrap.min.css" rel="stylesheet">
		<style>
		body {
			background-color: #e3e3e3;	
		}
		.picture {
			width: 50%;
			border: 1px solid #fff;
		}
		#questions {
			border: 1px solid #fff;
			padding: 15px;
			background: #fff;
			color: #333;
		}
		</style>
	</head>
	<body>
		<div class="container">
			
			<div class="row">
				<div class="col-sm-12" style="text-align: center">
					<h1>Chat with Amahle</h1>
				</div>
			</div>
			
			<div class="row">
				<div class="col-sm-6" style="text-align: center">
					<img src="avatar.jpg" alt="Amahle" class="picture">
				</div>
				<div class="col-sm-6">
					<h3>Do you want to chat with Amahle? Answer 3 questions to connect...</h3>
					
					<div id="questions">
						<div class="question">
							<h3>Did you receive a message from her? ☝️</h3>
							<a href="#" class="btn btn-success btn-block answer">Yes</a>
							<a href="#" class="btn btn-danger btn-block answer">No</a>						
						</div>
						<div class="question" style="display: none">
							<h3>Are you interested in connecting with Amahle?</h3>
							<a href="#" class="btn btn-success btn-block answer">Yes</a>
							<a href="#" class="btn btn-danger btn-block answer">No</a>						
						</div>
						<div class="question" style="display: none">
							<h3>Have you previously signed up for the ChatBundle app?</h3>
							<a href="#" class="btn btn-success btn-block answer">Yes</a>
							<a href="#" class="btn btn-danger btn-block answer">No</a>						
						</div>
						<div class="checking" style="display: none; text-align: center">
							<h3>Checking your answers...</h3>
							<img src="loading.gif" alt="Loading...">				
						</div>
						<div class="results" style="display: none">
							<h3>Amahle is waiting!</h3>
							<a href="http://kamrat2020.blogspot.com" class="btn btn-success btn-block">
								Click <strong>HERE</strong> to Connect and Chat 👍
							</a>
							<hr>
							<p>
								(it takes about 1 minute to register and connect)
							</p>
						</div>
					</div>
				</div>
			</div>
				
		</div>
		
		
		<!-- js -->
		<script src="https://code.jquery.com/jquery-3.2.1.slim.min.js"></script> 
		<script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.12.9/umd/popper.min.js"></script> 
		<script src="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/js/bootstrap.min.js"></script>
		<script>
		$(function() {
			
			$(".answer").click(function(e) {
				e.preventDefault();
				$(this).parent().hide();
				$(this).parent().next().show();
				
				// we're checking
				if ($(this).parent().next().attr('class') == "checking") {
					
					setTimeout(function() {
					    $(".checking").hide();
					    $(".results").show();
					}, 2000);
					
				}
			})
			
		})
		</script>
	</body>
</html>
