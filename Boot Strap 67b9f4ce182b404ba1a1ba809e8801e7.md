# Boot Strap

# **Creating Containers with Bootstrap**

Containers are the most basic layout element in Bootstrap and are required when using the grid system. Containers are basically used to wrap content with some padding. They are also used to align the content horizontally center on the page in case of fixed width layout.

Bootstrap provides three different types containers:

- `.container`, which has a max-width at each responsive breakpoint.
- `.container-fluid`, which has 100% width at all breakpoints.
- `.container-{breakpoint}`, which has 100% width until the specified breakpoint.

### **Creating Responsive Fixed-width Containers**

You can simply use the `.container` class to create a responsive, fixed-width container. The width of the container will change at different breakpoints or screen sizes.

```html
<div class="container">
    <h1>This is a heading</h1>
    <p>This is a paragraph of text.</p>
</div>
```

### **Creating Fluid Containers**

You can use the `.container-fluid` class to create a full width container. The width of the fluid container will always be 100% irrespective of the devices or screen sizes

```html
<div class="container-fluid">
    <h1>This is a heading</h1>
    <p>This is a paragraph of text.</p>
</div>
```

### **Specify Responsive Breakpoints for Containers**

Since Bootstrap v4.4, you can also create containers that is 100% wide until the specified breakpoint is reached, after which max-width for each of the higher breakpoints will be applied.

For example, `.container-xl` will be 100% wide until the xl breakpoint is reached (i.e., viewport width ≥ 1200px), after which max-width for xl breakpoint is applied, which is 1140px.

```html
<div class="container-sm">100% wide until screen size less than 576px</div>
<div class="container-md">100% wide until screen size less than 768px</div>
<div class="container-lg">100% wide until screen size less than 992px</div>
<div class="container-xl">100% wide until screen size less than 1200px</div>
```

****Bootstrap Cards****

Bootstrap card is a flexible and extensible content container. It includes options for headers and footers, a wide variety of content, contextual background colors, and powerful display options.

### **Creating a Basic Card**

The card markup is pretty straight forward. The outer wrapper require the base class `.card`, whereas content can be placed inside the `.card-body` element. The following example will show you how to create a card with a picture, mixed with some text content and a button

```html
<div class="card" style="width: 300px;">
    <img src="images/sample.svg" class="card-img-top" alt="...">
    <div class="card-body text-center">
        <h5 class="card-title">Alice Liddel</h5>
        <p class="card-text">Alice is a freelance web designer and developer based in London. She is specialized in HTML5, CSS3, JavaScript, Bootstrap, etc.</p>
        <a href="#" class="btn btn-primary">View Profile</a>
    </div>
</div>
```

### **Card with Titles, Text, and Links**

Further, you can also place title and links inside the card along with text, like this:

```html
<div class="card" style="width: 300px;">
    <div class="card-body">
        <h5 class="card-title">Eiffel Tower</h5>
        <h6 class="card-subtitle mb-3 text-muted">Champ de Mars, Paris, France</h6>
        <p class="card-text">Built in 1889 Eiffel Tower is one of the most iconic landmarks in the world.</p>
        <a href="#" class="card-link">View pictures</a>
        <a href="#" class="card-link">Discover history</a>
    </div>
</div>
```

### **Adding Navigation to Cards**

You can also add [Bootstrap's nav components](https://www.tutorialrepublic.com/twitter-bootstrap-tutorial/bootstrap-navs.php) such as tabs and pills to the card header.

To add tabs navigation to a card simply place the tabs markup inside the card header, and the tabs content inside the card body. You are also required to use an additional class `.card-header-tabs` on the `.nav` element along with the class `.nav-tabs` for proper alignment.

Let's try out the following example which creates an elegant tabbed navigation.

```html
<div class="card text-center">
    <div class="card-header">
        <ul class="nav nav-tabs card-header-tabs">
            <li class="nav-item">
                <a href="#home" class="nav-link active" data-bs-toggle="tab">Home</a>
            </li>
            <li class="nav-item">
                <a href="#profile" class="nav-link" data-bs-toggle="tab">Profile</a>
            </li>
            <li class="nav-item">
                <a href="#messages" class="nav-link" data-bs-toggle="tab">Messages</a>
            </li>
        </ul>
    </div>
    <div class="card-body">
        <div class="tab-content">
            <div class="tab-pane fade show active" id="home">
                <h5 class="card-title">Home tab content</h5>
                <p class="card-text">Here is some example text to make up the tab's content. Replace it with your own text anytime.</p>
                <a href="#" class="btn btn-primary">Go somewhere</a>
            </div>
            <div class="tab-pane fade" id="profile">
                <h5 class="card-title">Profile tab content</h5>
                <p class="card-text">Here is some example text to make up the tab's content. Replace it with your own text anytime.</p>
                <a href="#" class="btn btn-primary">Go somewhere</a>
            </div>
            <div class="tab-pane fade" id="messages">
                <h5 class="card-title">Messages tab content</h5>
                <p class="card-text">Here is some example text to make up the tab's content. Replace it with your own text anytime.</p>
                <a href="#" class="btn btn-primary">Go somewhere</a>
            </div>
        </div>
    </div>
</div>
```

## ****Bootstrap Grid System****

Bootstrap grid system provides an easy and powerful way to create responsive layouts of all shapes and sizes. It is built with [flexbox](https://www.tutorialrepublic.com/css-tutorial/css3-flexible-box-layouts.php) with mobile-first approach. Also, it is fully responsive and uses twelve column system (12 columns available per row) and six default responsive tiers.

You can use the Bootstrap's predefined grid classes for quickly making the layouts for different types of devices like mobile phones, tablets, laptops, desktops, and so on. For example, you can use the `.col-*` classes to create grid columns for extra small devices like mobile phones in portrait mode, and the `.col-sm-*` classes for mobile phones in landscape mode.

Similarly, you can use the `.col-md-*` classes to create grid columns for medium screen devices like tablets, the `.col-lg-*` classes for devices like small laptops, the `.col-xl-*` classes for laptops and desktops, and the `.col-xxl-*` classes for large desktop screens.

The following table summarizes the key features of the Bootstrap's grid system.

![Screenshot 2023-11-30 173118.png](Boot%20Strap%2067b9f4ce182b404ba1a1ba809e8801e7/Screenshot_2023-11-30_173118.png)

### **Creating Two Column Layouts**

The following example will show you how to create two column layouts for medium, large and extra large devices like tables, laptops and desktops etc. However, on mobile phones (screen width less than 768px), the columns will automatically become horizontal (2 rows, 1 column).

```html
<div class="container">
    <!--Row with two equal columns-->
    <div class="row">
        <div class="col-md-6">Column left</div>
        <div class="col-md-6">Column right</div>
    </div>
    
    <!--Row with two columns divided in 1:2 ratio-->
    <div class="row">
        <div class="col-md-4">Column left</div>
        <div class="col-md-8">Column right</div>
    </div>
    
    <!--Row with two columns divided in 1:3 ratio-->
    <div class="row">
        <div class="col-md-3">Column left</div>
        <div class="col-md-9">Column right</div>
    </div>
</div>
```

## **Creating Navbar with Bootstrap**

You can use the Bootstrap navbar component to create responsive navigation header for your website or application. These responsive navbar will be collapsed on devices having small viewports like mobile phones but expand when user click the toggle button. However, it will be horizontal as normal on the medium and large devices such as laptop or desktop.

You can also create different variations of the navbar such as navbars with dropdown menus and search boxes as well as fixed positioned navbar with much less effort. The following example will show you how to create a simple static navbar with navigation links.

```html
<nav class="navbar navbar-expand-lg navbar-light bg-light">
    <div class="container-fluid">
        <a href="#" class="navbar-brand">Brand</a>
        <button type="button" class="navbar-toggler" data-bs-toggle="collapse" data-bs-target="#navbarCollapse">
            <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarCollapse">
            <div class="navbar-nav">
                <a href="#" class="nav-item nav-link active">Home</a>
                <a href="#" class="nav-item nav-link">Profile</a>
                <a href="#" class="nav-item nav-link">Messages</a>
                <a href="#" class="nav-item nav-link disabled" tabindex="-1">Reports</a>
            </div>
            <div class="navbar-nav ms-auto">
                <a href="#" class="nav-item nav-link">Login</a>
            </div>
        </div>
    </div>
</nav>
```

## **Creating Responsive Layout with Bootstrap**

With the Bootstrap powerful mobile first [flexbox](https://www.tutorialrepublic.com/css-tutorial/css3-flexible-box-layouts.php) grid system creating the responsive and mobile friendly websites and applications has become much easier.

Bootstrap is responsive and mobile friendly from the start. Its [six tier grid classes](https://www.tutorialrepublic.com/twitter-bootstrap-tutorial/bootstrap-grid-system.php) provides better control over the layout as well as how it will be rendered on different types of devices like mobile phones, tablets, laptops and desktops, large screen devices, and so on.

The following example will create a responsive layout that is rendered as 4 column layout in extra-large devices (viewport ≥ 1200px), and 3 column layout in large devices (992px ≤ viewport < 1200px), whereas 2 column layout in medium devices (768px ≤ viewport < 992px), and 1 column layout in small and extra-small devices (viewport < 768px). Let's try it out and see how it works:

```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Bootstrap Responsive Layout Example</title>
<link rel="stylesheet" href="css/bootstrap.min.css">
<script src="js/bootstrap.bundle.min.js"></script>
</head>
<body>
<nav class="navbar navbar-expand-lg navbar-dark bg-dark">
    <div class="container-fluid">
        <a href="#" class="navbar-brand">Tutorial Republic</a>
        <button type="button" class="navbar-toggler" data-bs-toggle="collapse" data-bs-target="#navbarCollapse">
            <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarCollapse">
            <div class="navbar-nav">
                <a href="#" class="nav-item nav-link active">Home</a>
                <a href="#" class="nav-item nav-link">Services</a>
                <a href="#" class="nav-item nav-link">About</a>
                <a href="#" class="nav-item nav-link">Contact</a>
            </div>
            <div class="navbar-nav ms-auto">
                <a href="#" class="nav-item nav-link">Register</a>
                <a href="#" class="nav-item nav-link">Login</a>
            </div>
        </div>
    </div>
</nav>
<div class="container">
    <div class="p-5 my-4 bg-light rounded-3">
        <h1>Learn to Create Websites</h1>
        <p class="lead">In today's world internet is the most popular way of connecting with the people. At <a href="https://www.tutorialrepublic.com" class="text-success" target="_blank">tutorialrepublic.com</a> you will learn the essential web development technologies along with real life practice examples, so that you can create your own website to connect with the people around the world.</p>
        <p><a href="https://www.tutorialrepublic.com" target="_blank" class="btn btn-success btn-lg">Get started today</a></p>
    </div>
    <div class="row g-3">
        <div class="col-md-6 col-lg-4 col-xl-3">
            <h2>HTML</h2>
            <p>HTML is the standard markup language for describing the structure of the web pages. Our HTML tutorials will help you to understand the basics of latest HTML5 language, so that you can create your own website.</p>
            <p><a href="https://www.tutorialrepublic.com/html-tutorial/" target="_blank" class="btn btn-success">Learn More &raquo;</a></p>
        </div>
        <div class="col-md-6 col-lg-4 col-xl-3">
            <h2>CSS</h2>
            <p>CSS is used for describing the presentation of web pages. CSS can save a lot of time and effort. Our CSS tutorials will help you to learn the essentials of latest CSS3, so that you can control the style and layout of your website.</p>
            <p><a href="https://www.tutorialrepublic.com/css-tutorial/" target="_blank" class="btn btn-success">Learn More &raquo;</a></p>
        </div>
        <div class="col-md-6 col-lg-4 col-xl-3">
            <h2>JavaScript</h2>
            <p>JavaScript is the most popular and widely used client-side scripting language. Our JavaScript tutorials will provide in-depth knowledge of the JavaScript including ES6 features, so that you can create interactive websites.</p>
            <p><a href="https://www.tutorialrepublic.com/javascript-tutorial/" target="_blank" class="btn btn-success">Learn More &raquo;</a></p>
        </div>
        <div class="col-md-6 col-lg-4 col-xl-3">
            <h2>Bootstrap</h2>
            <p>Bootstrap is a powerful front-end framework for faster and easier web development. Our Bootstrap tutorials will help you to learn all the features of latest Bootstrap 4 framework so that you can easily create responsive websites.</p>
            <p><a href="https://www.tutorialrepublic.com/twitter-bootstrap-tutorial/" target="_blank" class="btn btn-success">Learn More &raquo;</a></p>
        </div>
        <div class="col-md-6 col-lg-4 col-xl-3">
            <h2>PHP</h2>
            <p>PHP is the most popular server-side scripting language for creating dynamic web pages. Our PHP tutorials will help you to learn all the features of latest PHP7 scripting language so that you can easily create dynamic websites.</p>
            <p><a href="https://www.tutorialrepublic.com/twitter-bootstrap-tutorial/" target="_blank" class="btn btn-success">Learn More &raquo;</a></p>
        </div>
        <div class="col-md-6 col-lg-4 col-xl-3">
            <h2>SQL</h2>
            <p>SQL is a standard language designed for managing data in relational database management system. Our SQL tutorials will help you to learn the fundamentals of the SQL language so that you can efficiently manage your databases.</p>
            <p><a href="https://www.tutorialrepublic.com/twitter-bootstrap-tutorial/" target="_blank" class="btn btn-success">Learn More &raquo;</a></p>
        </div>
        <div class="col-md-6 col-lg-4 col-xl-3">
            <h2>References</h2>
            <p>Our references section outlines all the standard HTML5 tags and CSS3 properties along with other useful references such as color names and values, character entities, web safe fonts, language codes, HTTP messages, and more.</p>
            <p><a href="https://www.tutorialrepublic.com/twitter-bootstrap-tutorial/" target="_blank" class="btn btn-success">Learn More &raquo;</a></p>
        </div>
        <div class="col-md-6 col-lg-4 col-xl-3">
            <h2>FAQ</h2>
            <p>Our Frequently Asked Questions (FAQ) section is an extensive collection of FAQs that provides quick and working solution of common questions and queries related to web design and development with live demo.</p>
            <p><a href="https://www.tutorialrepublic.com/twitter-bootstrap-tutorial/" target="_blank" class="btn btn-success">Learn More &raquo;</a></p>
        </div>
    </div>
    <hr>
    <footer>
        <div class="row">
            <div class="col-md-6">
                <p>Copyright &copy; 2021 Tutorial Republic</p>
            </div>
            <div class="col-md-6 text-md-end">
                <a href="#" class="text-dark">Terms of Use</a>
                <span class="text-muted mx-2">|</span>
                <a href="#" class="text-dark">Privacy Policy</a>
            </div>
        </div>
    </footer>
</div>
</body>
</html>
```