<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Brown Fenning Tea</title>

    <style>
        body {
            margin: 0;
            font-family: Arial, sans-serif;
            background: #f1f1f1;
        }

        /* NAVBAR */
        .navbar {
            background: #f57c00;
            color: white;
            padding: 12px 22px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .brand {
            display: flex;
            align-items: center;
            gap: 10px;
        }

        /* ✅ FIXED LOGO CSS */
        .brand img {
            width: 48px;
            height: 48px;
            border-radius: 50%;
            object-fit: cover;
        }

        .brand-name {
            font-size: 20px;
            font-weight: bold;
        }

        .tagline {
            font-size: 12px;
        }

        .nav-buttons button {
            padding: 6px 12px;
            border: none;
            border-radius: 8px;
            cursor: pointer;
            background: white;
            color: #f57c00;
            font-weight: bold;
        }

        /* MAIN MENU BOX */
        .menu-section {
            width: 90%;
            margin: 25px auto;
            background: white;
            padding: 20px;
            border-radius: 14px;
        }

        .menu-title {
            font-size: 26px;
            font-weight: bold;
            margin-bottom: 8px;
        }

        .menu-subtitle {
            color: #555;
            margin-bottom: 22px;
        }

        .category {
            font-size: 20px;
            font-weight: bold;
            margin: 16px 0 10px;
            color: #333;
        }

        /* GRID CARD STYLE */
        .cards {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(220px, 1fr));
            gap: 18px;
        }

        .card {
            background: #fff6e9;
            padding: 16px;
            border-radius: 10px;
            box-shadow: 0 3px 6px rgba(0,0,0,0.08);
        }

        .item {
            font-size: 18px;
            font-weight: 600;
        }

        .price {
            margin: 4px 0 10px;
        }

        .add-btn {
            width: 100%;
            padding: 6px 0;
            border: none;
            background: #f57c00;
            color: white;
            border-radius: 6px;
            cursor: pointer;
        }

        .add-btn:hover {
            opacity: 0.85;
        }

        /* ✅ CART POPUP */
        #cartBox{
            position:fixed;
            right:20px;
            top:80px;
            background:white;
            padding:15px;
            width:260px;
            box-shadow:0 0 10px gray;
            display:none;
            border-radius:10px;
        }
    </style>
</head>
<body>

    <!-- NAV BAR -->
    <div class="navbar">
        <div class="brand">
            <img src="bft.png" alt="BFT Logo">
            <div>
                <div class="brand-name">Brown Fenning Tea</div>
                <div class="tagline">Fast Delivery to Your Hostel</div>
            </div>
        </div>
        
        <div class="nav-buttons">
            <button>Menu</button>
            <button onclick="openCart()">🛒 Cart</button>
        </div>
    </div>

    <!-- MENU -->
    <div class="menu-section">
        <div class="menu-title">Our Menu</div>

        <!-- CATEGORY 1 -->
        <div class="category">Beverages</div>
        <div class="cards">

            <div class="card">
                <div class="item">Tea</div>
                <div class="price">₹10</div>
                <button class="add-btn" onclick="addToCart('Tea',10)">Add</button>
            </div>

            <div class="card">
                <div class="item">Coffee</div>
                <div class="price">₹15</div>
                <button class="add-btn" onclick="addToCart('Coffee',15)">Add</button>
            </div>

            <div class="card">
                <div class="item">Boost</div>
                <div class="price">₹25</div>
                <button class="add-btn" onclick="addToCart('Boost',25)">Add</button>
            </div>

            <div class="card">
                <div class="item">Horlicks</div>
                <div class="price">₹25</div>
                <button class="add-btn" onclick="addToCart('Horlicks',25)">Add</button>
            </div>

            <div class="card">
                <div class="item">Lemon Juice</div>
                <div class="price">₹20</div>
                <button class="add-btn" onclick="addToCart('Lemon Juice',20)">Add</button>
            </div>

            <div class="card">
                <div class="item">Badham Milk</div>
                <div class="price">₹30</div>
                <button class="add-btn" onclick="addToCart('Badham Milk',30)">Add</button>
            </div>
        </div>

        <!-- CATEGORY 2 -->
        <div class="category">Snacks & More</div>
        <div class="cards">
            <div class="card">
                <div class="item">Egg</div>
                <div class="price">₹20</div>
                <button class="add-btn" onclick="addToCart('Egg',20)">Add</button>
            </div>

            <div class="card">
                <div class="item">Veg</div>
                <div class="price">₹20</div>
                <button class="add-btn" onclick="addToCart('Veg',20)">Add</button>
            </div>

            <div class="card">
                <div class="item">Mushroom</div>
                <div class="price">₹20</div>
                <button class="add-btn" onclick="addToCart('Mushroom',20)">Add</button>
            </div>

            <div class="card">
                <div class="item">Chicken</div>
                <div class="price">₹35</div>
                <button class="add-btn" onclick="addToCart('Chicken',35)">Add</button>
            </div>

            <div class="card">
                <div class="item">Samosa</div>
                <div class="price">₹20</div>
                <button class="add-btn" onclick="addToCart('Samosa',20)">Add</button>
            </div>

            <div class="card">
                <div class="item">Cake</div>
                <div class="price">₹20</div>
                <button class="add-btn" onclick="addToCart('Cake',20)">Add</button>
            </div>

            <div class="card">
                <div class="item">Jam Bun</div>
                <div class="price">₹20</div>
                <button class="add-btn" onclick="addToCart('Jam Bun',20)">Add</button>
            </div>

            <div class="card">
                <div class="item">Bread Omelette</div>
                <div class="price">₹40</div>
                <button class="add-btn" onclick="addToCart('Bread Omelette',40)">Add</button>
            </div>

            <div class="card">
                <div class="item">Maggi (Egg)</div>
                <div class="price">₹50</div>
                <button class="add-btn" onclick="addToCart('Maggi (Egg)',50)">Add</button>
            </div>
        </div>
    </div>

    <!-- ✅ CART BOX -->
    <div id="cartBox">
        <h3>Cart</h3>
        <div id="cartItems"></div>
        <h4 id="totalPrice"></h4>
        <button onclick="closeCart()">Close</button>
    </div>


<script>

let cart = [];
let total = 0;

function addToCart(item,price){
    cart.push(item);
    total += price;
    alert(item + " added to cart");
}

function openCart(){

    document.getElementById("cartBox").style.display="block";

    let list="";

    cart.forEach(i=>{
        list += "<p>"+i+"</p>";
    });

    document.getElementById("cartItems").innerHTML=list;
    document.getElementById("totalPrice").innerHTML="Total: ₹"+total;
}

function closeCart(){
    document.getElementById("cartBox").style.display="none";
}

</script>

</body>
</html>
