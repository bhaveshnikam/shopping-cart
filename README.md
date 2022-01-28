# shopping-cart
<!DOCTYPE html>

<html>

<head>

	<title>Shopping Cart</title>

	<link rel="stylesheet" type="text/css" href="cart.css">

	<link rel="stylesheet" type="text/css" href="https://stackpath.bootstrapcdn.com/font-awesome/4.7.0/css/font-awesome.min.css">

</head>

<body>



<div class="container">

	<h1>Shopping Cart</h1>

	<div class="cart">

		<div class="products">

			<div class="product">

				<img src="shoes.jpg">

				<div class="product-info">

					<h3 class="product-name">New Shoes</h3>

					<h4 class="product-price">₹ 1,000</h4>

					<h4 class="product-offer">50%</h4>

					<p class="product-quantity">Qnt: <input value="1" name="">

					<p class="product-remove">

						<i class="fa fa-trash" aria-hidden="true"></i>

						<span class="remove">Remove</span>

					</p>

				</div>

			</div>

			<div class="product">

				<img src="bag1.jpg">

				<div class="product-info">

					<h3 class="product-name">New Bag</h3>

					<h4 class="product-price">₹ 2,000</h4>

					<h4 class="product-offer">40%</h4>

					<p class="product-quantity">Qnt: <input value="1" name="">

					<p class="product-remove">

						<i class="fa fa-trash" aria-hidden="true"></i>

						<span class="remove">Remove</span>

					</p>

				</div>

			</div>

		</div>

		<div class="cart-total">

			<p>

				<span>Total Price</span>

				<span>₹ 3,000</span>

			</p>

			<p>

				<span>Number of Items</span>

				<span>2</span>

			</p>

			<p>

				<span>You Save</span>

				<span>₹ 1,000</span>

			</p>

			<a href="#">Proceed to Checkout</a>

		</div>

	</div>

</div>



</body>


</html>



CSS - 



@import url('https://fonts.googleapis.com/css2?family=Comfortaa&display=swap');

*{

	font-family: 'Comfortaa', cursive;

	margin: 0;

	padding: 0;

	box-sizing: border-box;

}

.container{

	max-width: 1200px;

	margin: 0 auto;

}

.container > h1{

	padding: 20px 0;

}

.cart{

	display: flex;

}

.products{

	flex: 0.75;

}

.product{

	display: flex;

	width: 100%;

	height: 200px;

	overflow: hidden;

	border: 1px solid silver;

	margin-bottom: 20px;

}

.product:hover{

	border: none;

	box-shadow: 2px 2px 4px rgba(0,0,0,0.2);

	transform: scale(1.01);

}

.product > img{

	width: 300px;

	height: 200px;

	object-fit: cover;

}

.product > img:hover{

	transform: scale(1.04);

}

.product-info{

	padding: 20px;

	width: 100%;

	position: relative;

}

.product-name, .product-price, .product-offer{

	margin-bottom: 20px;

}

.product-remove{

	position: absolute;

	bottom: 20px;

	right: 20px;

	padding: 10px 25px;

	background-color: green;

	color: white;

	cursor: pointer;

	border-radius: 5px;

}

.product-remove:hover{

	background-color: white;

	color: green;

	font-weight: 600;

	border: 1px solid green;

}

.product-quantity > input{

	width: 40px;

	padding: 5px;

	text-align: center;

}

.fa{

	margin-right: 5px;

}

.cart-total{

	flex: 0.25;

	margin-left: 20px;

	padding: 20px;

	height: 240px;

	border: 1px solid silver;

	border-radius: 5px;

}

.cart-total p{

	display: flex;

	justify-content: space-between;

	margin-bottom: 30px;

	font-size: 20px;

}

.cart-total a{

	display: block;

	text-align: center;

	height: 40px;

	line-height: 40px;

	background-color: tomato;

	color: white;

	text-decoration: none;

}

.cart-total a:hover{

	background-color: red;

}

@media screen and (max-width: 700px){

	.remove{

		display: none;

	}

	.product{

		height: 150px;

	}

	.product > img{

		height: 150px;

		width: 200px;

	}

	.product-name, .product-price, .product-offer{

		margin-bottom: 10px;

	}

}

@media screen and (max-width: 900px){

	.cart{

		flex-direction: column;

	}

	.cart-total{

		margin-left: 0;

		margin-bottom: 20px;

	}

}

@media screen and (max-width: 1220px){

	.container{

		max-width: 95%;

	}

}

