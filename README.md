# Ex.07 Restaurant Website
# Date:05.10.2025
# AIM:
To develop a static Restaurant website to display the food items and services provided by them.

# DESIGN STEPS:
## Step 1:
Requirement collection.

## Step 2:
Creating the layout using HTML and CSS.

## Step 3:
Updating the sample content.

## Step 4:
Choose the appropriate style and color scheme.

## Step 5:
Validate the layout in various browsers.

## Step 6:
Validate the HTML code.

## Step 7:
Publish the website in the given URL.

# PROGRAM:
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Delizia Restaurant</title>
  <style>
    * {margin: 0; padding: 0; box-sizing: border-box; font-family: 'Poppins', sans-serif;}
    body {background-color: #fffaf2; color: #333; scroll-behavior: smooth;}

    /* Header */
    header {
      background: linear-gradient(135deg, #ff7b00, #ffcc33);
      color: white;
      text-align: center;
      padding: 50px 20px;
      border-bottom: 5px solid #ff6a00;
    }
    header h1 {font-size: 3rem; letter-spacing: 2px; animation: glow 2s infinite alternate;}
    header p {font-size: 1.1rem; margin-top: 10px;}
    @keyframes glow {from {text-shadow: 0 0 10px #fff0b3;} to {text-shadow: 0 0 25px #fff;}}

    /* Navigation */
    nav {
      background-color: #222;
      display: flex;
      justify-content: center;
      flex-wrap: wrap;
    }
    nav a {
      color: white;
      text-decoration: none;
      padding: 15px 25px;
      transition: 0.3s;
      font-weight: 600;
    }
    nav a:hover {background-color: #ff7b00; border-radius: 5px;}

    /* Hero */
    .hero {
      background: url('https://images.unsplash.com/photo-1601924579440-30be44b3049b?auto=format&fit=crop&w=1400&q=80') center/cover no-repeat;
      height: 75vh;
      position: relative;
      display: flex;
      justify-content: center;
      align-items: center;
      text-align: center;
      color: white;
    }
    .hero::after {
      content: ""; position: absolute; top:0; left:0; right:0; bottom:0;
      background-color: rgba(0,0,0,0.5);
    }
    .hero-content {position: relative; z-index: 1;}
    .hero-content h2 {font-size: 3rem; margin-bottom: 10px;}
    .hero-content p {font-size: 1.2rem; margin-bottom: 20px;}
    .hero-content a {
      text-decoration: none; background-color: #ff7b00; color: white;
      padding: 12px 25px; border-radius: 25px; font-weight: bold;
      transition: 0.3s;
    }
    .hero-content a:hover {background-color: #ffcc33;}

    /* Menu Section */
    .menu {padding: 70px 20px; background-color: #fff5e1; text-align: center;}
    .menu h2 {font-size: 2.5rem; color: #ff7b00; margin-bottom: 40px;}
    .menu-items {
      display: flex; flex-wrap: wrap; justify-content: center; gap: 30px;
    }
    .dish {
      background: white; width: 250px; border-radius: 15px;
      box-shadow: 0 4px 12px rgba(0,0,0,0.1);
      transition: transform 0.3s;
    }
    .dish:hover {transform: scale(1.05);}
    .dish img {
      width: 100%; height: 180px; border-radius: 15px 15px 0 0; object-fit: cover;
    }
    .dish h3 {color: #ff7b00; margin: 10px 0 5px;}
    .dish p {font-size: 0.95rem; color: #555; padding: 0 10px 15px;}

    /* Admin Section */
    .admin {padding: 70px 20px; text-align: center; background-color: #fffdf7;}
    .admin h2 {font-size: 2.5rem; color: #ff7b00; margin-bottom: 40px;}
    .team {
      display: flex; flex-wrap: wrap; justify-content: center; gap: 30px;
    }
    .member {
      background: white; width: 250px; border-radius: 15px;
      box-shadow: 0 4px 12px rgba(0,0,0,0.1);
      transition: transform 0.3s; padding-bottom: 15px;
    }
    .member:hover {transform: scale(1.05);}
    .member img {
      width: 100%; height: 220px; border-radius: 15px 15px 0 0; object-fit: cover;
    }
    .member h3 {color: #ff7b00; margin: 10px 0 5px;}
    .member p {font-size: 0.95rem; color: #555;}

    /* Contact */
    .contact {
      background-color: #ffefd1;
      text-align: center;
      padding: 70px 20px;
    }
    .contact h2 {
      font-size: 2.5rem;
      color: #ff7b00;
      margin-bottom: 30px;
    }
    .contact-info {
      max-width: 600px;
      margin: auto;
      background: white;
      padding: 30px;
      border-radius: 15px;
      box-shadow: 0 4px 12px rgba(0,0,0,0.1);
      line-height: 1.8;
      font-size: 1.1rem;
    }
    .contact-info p {margin: 10px 0;}

    /* Footer */
    footer {
      background-color: #222;
      color: white;
      text-align: center;
      padding: 20px;
      font-size: 0.95rem;
    }
    footer span {color: #ff7b00; font-weight: bold;}

    @media (max-width: 768px) {
      .hero-content h2 {font-size: 2.2rem;}
      .menu-items, .team {flex-direction: column; align-items: center;}
    }
  </style>
</head>
<body>

  <!-- Header -->
  <header>
    <h1>Delizia Restaurant</h1>
    <p>Where Flavor Meets Passion</p>
  </header>

  <!-- Navigation -->
  <nav>
    <a href="#home">Home</a>
    <a href="#menu">Menu</a>
    <a href="#admin">Administration</a>
    <a href="#contact">Contact Us</a>
  </nav>

  <!-- Hero -->
  <section class="hero" id="home">
    <div class="hero-content">
      <h2>Welcome to Delizia</h2>
      <p>Experience World-Class Dining Crafted With Love</p>
      <a href="#menu">Explore Our Menu</a>
    </div>
  </section>

  <!-- Menu Section -->
  <section class="menu" id="menu">
    <h2>Our Special Menu</h2>
    <div class="menu-items">
      <div class="dish">
        <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTmfnz3YQhIcY3tsiZa5V_0AlJeMHDgxlQymQ&s" alt="Pizza">
        <h3>Firewood Pizza</h3>
        <p>Classic Italian style pizza baked in a wood-fired oven.</p>
      </div>
      <div class="dish">
        <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTGj5fp8DwKOgB02Y1w-suEvsEg_E0eYYdO_A&s "alt="Pasta">
        <h3>Truffle Pasta</h3>
        <p>Rich creamy sauce with truffle essence and parmesan.</p>
      </div>
      <div class="dish">
        <img src="https://www.allrecipes.com/thmb/5JVfA7MxfTUPfRerQMdF-nGKsLY=/1500x0/filters:no_upscale():max_bytes(150000):strip_icc()/25473-the-perfect-basic-burger-DDMFS-4x3-56eaba3833fd4a26a82755bcd0be0c54.jpg" alt="Burger">
        <h3>Gourmet Burger</h3>
        <p>Juicy beef patty with crispy fries and house dressing.</p>
      </div>
      <div class="dish">
        <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQmDus8QTlj9N82AuUUBT7MGB9SuCzaWfuUFA&s" alt="Salad">
        <h3>Caesar Salad</h3>
        <p>Fresh greens with tangy dressing and grilled chicken.</p>
      </div>
      <div class="dish">
        <img src="https://images.getrecipekit.com/20250325120225-how-20to-20make-20chocolate-20molten-20lava-20cake-20in-20the-20microwave.png?width=650&quality=90&" alt="Dessert">
        <h3>Chocolate Lava Cake</h3>
        <p>Warm chocolate cake with molten center and ice cream.</p>
      </div>
      <div class="dish">
        <img src="https://www.fannetasticfood.com/wp-content/uploads/2021/09/Berry-Yogurt-Smoothie-FF-featured-image-735x735.jpg" alt="Drink">
        <h3>Fresh Fruit Smoothie</h3>
        <p>Refreshing blend of tropical fruits for a healthy twist.</p>
      </div>
    </div>
  </section>

  <!-- Administration -->
  <section class="admin" id="admin">
    <h2>Our Administration Team</h2>
    <div class="team">
      <div class="member">
        <img src="https://randomuser.me/api/portraits/men/11.jpg" alt="Manager">
        <h3>Arun Kumar</h3>
        <p>General Manager</p>
      </div>
      <div class="member">
        <img src="https://randomuser.me/api/portraits/women/12.jpg" alt="Chef">
        <h3>Divya Sharma</h3>
        <p>Head Chef</p>
      </div>
      <div class="member">
        <img src="https://randomuser.me/api/portraits/men/13.jpg" alt="Finance">
        <h3>Rohit Menon</h3>
        <p>Finance Officer</p>
      </div>
      <div class="member">
        <img src="https://randomuser.me/api/portraits/women/14.jpg" alt="HR">
        <h3>Priya Nair</h3>
        <p>Human Resources</p>
      </div>
      <div class="member">
        <img src="https://randomuser.me/api/portraits/men/15.jpg" alt="Marketing">
        <h3>Vikram Patel</h3>
        <p>Marketing Head</p>
      </div>
      <div class="member">
        <img src="https://randomuser.me/api/portraits/women/16.jpg" alt="Operations">
        <h3>Anjali Verma</h3>
        <p>Operations Manager</p>
      </div>
    </div>
  </section>

  <!-- Contact -->
  <section class="contact" id="contact">
    <h2>Contact Us</h2>
    <div class="contact-info">
      <p>📍 Address: 123 Food Street, Chennai, India</p>
      <p>📞 Phone: +91 98765 43210</p>
      <p>📧 Email: delizia.restaurant@gmail.com</p>
      <p>🕒 Open Hours: 10 AM – 11 PM (All Days)</p>
    </div>
  </section>

  <!-- Footer -->
  <footer>
    <p>© 2025 Delizia Restaurant | Designed by <span>Rachanaa</span></p>
  </footer>

</body>
</html>
```
# OUTPUT:
![alt text](<Screenshot 2025-10-05 220458.png>)

![alt text](<Screenshot 2025-10-05 220517.png>)

![alt text](<Screenshot 2025-10-05 220533.png>)

![alt text](<Screenshot 2025-10-05 220547.png>)
# RESULT:
The program for designing software company website using HTML and CSS is completed successfully.
