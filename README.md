## Nama  : Anggi Ringgo Kuncoro Jati
## Kelas : TI.19.B2
## NIM   : 311910743

# PRAKTIKUM 4

## Membuat Dokumen HTML Lab4Web.html
```
<!DOCTYPE html>
<html lang="en">
<head>
 <meta charset="UTF-8">
 <meta name="viewport" content="width=device-width, initial-scale=1.0">
 <title>Box Element</title>
</head>
<body>
 <header>
 <h1>Box Element</h1>
 <section>
 <div class="div1">Div 1</div>
 <div class="div2">Div 2</div>
 <div class="div3">Div 3</div> 
</section>
 </header>
</body>
</html>

```
## Menambahkan Style pada HTML
```
<style>
 div {
 float:left;
 padding: 10px; 
 }
 .div1 {
 background: red;
 }
 .div2 {
 background: yellow;
 }
 .div3 {
 background: green;
 }
</style>
```
![Screenshot (62)](https://user-images.githubusercontent.com/81921974/115327698-9540b680-a1b9-11eb-8cdd-157d7cf7c7c7.png)

## Mengatur Clearfix Element
### Clearfix digunakan untuk mengatur element setelah float element. Property clear digunakan untuk mengaturnya. Tambahkan element div lainnya seteleah div3 seperti berikut.
```
<section>
<div class="div1">Div 1</div>
<div class="div2">Div 2</div>
<div class="div3">Div 3</div>
<div class="div4">Div 4</div>
</section>
```
### Kemudian atur property clear pada CSS, seperti berikut.
```.div4 {
background-color: blue;
clear: left;
float: none;
}
```
![Screenshot (65)](https://user-images.githubusercontent.com/81921974/115328504-ed2bed00-a1ba-11eb-94f4-e6653c6ff3b3.png)

## Membuat Layout Sederhana
### Buat folder baru dengan nama lab4_layout, kemudian buatlah file baru didalamnya dengan nama home.html, dan file css dengan nama style.css.
```
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Layout Sederhana</title>
<link rel="stylesheet" href="style.css">
</head>
<body>
<div id="container">
</div>
</body>
</html>
```
### Kemudian tulis kode berikut.
```<header>
<h1>Layout Sederhana</h1>
</header>
<nav>
<a href="home.html" class="active">Home</a>
<a href="artikel.html">Artikel</a>
<a href="about.html">About</a>
<a href="kontak.html">Kontak</a>
</nav>
<section id="hero"></section>
<section id="wrapper">
<section id="main"></section>
<aside id="sidebar"></aside>
</section>
<footer>
<p>&copy; 2021 - Universitas Pelita Bangsa</p>
</footer>
```
![Screenshot (67)](https://user-images.githubusercontent.com/81921974/115328859-822ee600-a1bb-11eb-93f5-6577ddc4fb6f.png)

### Kemudian tambahkan kode CSS untuk membuat layoutnya.
```/* import google font */
@import
url('https://fonts.googleapis.com/css2?family=Open+Sans:ital,wght@0,300;0,400
;0,600;0,700;0,800;1,300;1,400;1,600;1,700;1,800&display=swap');
@import
url('https://fonts.googleapis.com/css2?family=Open+Sans+Condensed:ital,wght@0
,300;0,700;1,300&display=swap');
/* Reset CSS */
* {
margin: 0;
padding: 0;
}
body {
line-height:1;
font-size:100%;
font-family:'Open Sans', sans-serif;
color:#5a5a5a;
}
#container {
width: 980px;
margin: 0 auto;
box-shadow: 0 0 1em #cccccc;
}
/* header */
header {
padding: 20px;
}
header h1 {
margin: 20px 10px;
color: #b5b5b5;
}
```
![Screenshot (69)](https://user-images.githubusercontent.com/81921974/115328972-b6a2a200-a1bb-11eb-8446-48ef0cb22d53.png)

### Membuat Navigasi
Kemudian selanjutnya mengatur navigasi.
```
/* navigasi */
nav {
display: block;
background-color: #1f5faa;
}
nav a {
padding: 15px 30px;
display: inline-block;
color: #ffffff;
font-size: 14px;
text-decoration: none;
font-weight: bold;
}
nav a.active,
nav a:hover {
background-color: #2b83ea;
}
```
![Screenshot (71)](https://user-images.githubusercontent.com/81921974/115329036-dd60d880-a1bb-11eb-9974-1cfcfe4666d4.png)

### Membuat Hero Panel.
Selanjutnya membuat hero panel. Tambahkan kode HTML dan CSS seperti berikut.
```
<section id="hero">
<h1>Hello World!</h1>
<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem
elit, iaculis innisl volutpat, malesuada tincidunt arcu. Proin in leo fringilla,
vestibulum mi porta, faucibus felis. Integer pharetra est nunc, nec pretium nunc
pretium ac.</p>
<a href="home.html" class="btn btn-large">Learn more &raquo;</a>
</section>
```
CSS
```
/* Hero Panel */
#hero {
background-color: #e4e4e5;
padding: 50px 20px;
margin-bottom: 20px;
}
#hero h1 {
margin-bottom: 20px;
font-size: 35px;
}
#hero p {
margin-bottom: 20px;
font-size: 18px;
line-height: 25px;
}
```
![Screenshot (76)](https://user-images.githubusercontent.com/81921974/115329332-5d873e00-a1bc-11eb-9310-f05824870eac.png)

### Mengatur Layout Main dan Sidebar
Selanjutnya mengatur main content dan sidebar, tambahkan CSS float.
```
/* main content */
#wrapper {
margin: 0;
}
#main {
float: left;
width: 640px;
padding: 20px;
}
/* sidebar area */
#sidebar {
float: left;
width: 260px;
padding: 20px;
}
```
### Membuat Sidebar Widget
Kemudian selanjutnya menambahkan element lain dalam sidebar.
```
<aside id="sidebar">
<div class="widget-box">
<h3 class="title">Widget Header</h3>
<ul>
<li><a href="#">Widget Link</a></li>
<li><a href="#">Widget Link</a></li>
<li><a href="#">Widget Link</a></li>
<li><a href="#">Widget Link</a></li>
<li><a href="#">Widget Link</a></li>
</ul>
</div>
<div class="widget-box">
<h3 class="title">Widget Text</h3>
<p>Vestibulum lorem elit, iaculis in nisl volutpat, malesuada tincidunt
arcu. Proin in leo fringilla, vestibulum mi porta, faucibus felis. Integer
pharetra est nunc, nec pretium nunc pretium ac.</p>
</div>
</aside>
```
kemudian tambahkan CSS.
```
/* widget */
.widget-box {
border:1px solid #eee;
margin-bottom:20px;
}
.widget-box .title {
padding:10px 16px;
background-color:#428bca;
color:#fff;
}
.widget-box ul {
list-style-type:none;
}
.widget-box li {
border-bottom:1px solid #eee;
}
.widget-box li a {
padding:10px 16px;
color:#333;
display:block;
text-decoration:none;
}
.widget-box li:hover a {
background-color:#eee;
}
.widget-box p {
padding:15px;
line-height:25px;
}
```
![Screenshot (80)](https://user-images.githubusercontent.com/81921974/115329489-97f0db00-a1bc-11eb-8227-b16049fe0b21.png)

### Mengatur Footer
Selanjutnya mengatur tampilan footer. Tambahkan CSS untuk footer.
```
/* footer */
footer {
clear:both;
background-color:#1d1d1d;
padding:20px;
color:#eee;
}
```
![Screenshot (81)](https://user-images.githubusercontent.com/81921974/115329588-b48d1300-a1bc-11eb-85d5-a39747979891.png)
### Menambahkan Elemen lainnya pada Main Content.
```
<section id="main">
<div class="row">
<div class="box">
<img src="https://dummyimage.com/120/db7d25/fff.png" alt=""
class="image-circle">
<h3>Heading</h3>
<p>Donec sed odio dui. Etiam porta sem malesuada magna mollis
euismod.</p>
<a href="#" class="btn btn-default">View detail</a>
</div>
<div class="box">
<img src="https://dummyimage.com/120/3e73e6/fff.png" alt=""
class="image-circle">
<h3>Heading</h3>
<p>Donec sed odio dui. Etiam porta sem malesuada magna mollis
euismod.</p>
<a href="#" class="btn btn-default">View detail</a>
</div>
<div class="box">
<img src="https://dummyimage.com/120/71e6d4/fff.png" alt=""
class="image-circle">
<h3>Heading</h3>
<p>Donec sed odio dui. Etiam porta sem malesuada magna mollis
euismod.</p>
<a href="#" class="btn btn-default">View detail</a>
</div>
</div>
</section>
```
### Kemudian tambahkan CSS.
```/* box */
.box {
display:block;
float:left;
width:33.333333%;
box-sizing:border-box;
-moz-box-sizing:border-box;
-webkit-box-sizing:border-box;
padding:0 10px;
text-align:center;
}
.box h3 {
margin: 15px 0;
}
.box p {
line-height: 20px;
font-size: 14px;
margin-bottom: 15px;
}
box img {
border: 0;
vertical-align: middle;
}
.image-circle {
border-radius: 50%;
}
.row {
margin: 0 -10px;
box-sizing: border-box;
-moz-box-sizing: border-box;
-webkit-box-sizing: border-box;
}
.row:after, .row:before,
.entry:after, .entry:before {
content:'';
display:table;
}
.row:after,
.entry:after {
clear:both;
}
```
![Screenshot (84)](https://user-images.githubusercontent.com/81921974/115329763-f918ae80-a1bc-11eb-911a-ed4cef0de03d.png)
### Menambahkan Content Artikel
Selanjutnya membuat content artikel. Tambahkan HTML berikut pada main content.
```<hr class="divider" />
<article class="entry">
<h2>First featurette heading.</h2>
<img src="https://dummyimage.com/150/7b8a70/fff.png" alt="">
<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem
elit, iaculis in nisl volutpat, malesuada tincidunt arcu. Proin in leo fringilla,
vestibulum mi porta, faucibus felis. Integer pharetra est nunc, nec pretium nunc
pretium ac.</p>
</article>
<hr class="divider" />
<article class="entry">
<h2>First featurette heading.</h2>
<img src="https://dummyimage.com/150/7b8a70/fff.png" alt=""
class="right-img">
<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem
elit, iaculis in nisl volutpat, malesuada tincidunt arcu. Proin in leo fringilla,
vestibulum mi porta, faucibus felis. Integer pharetra est nunc, nec pretium nunc
pretium ac.</p>
</article> 
```
Kemudian tambahkan CSS.
```.divider {
border:0;
border-top:1px solid #eeeeee;
margin:40px 0;
}
/* entry */
.entry {
margin: 15px 0;
}
.entry h2 {
margin-bottom: 20px;
}
.entry p {
line-height: 25px;
}
.entry img {
float: left;
border-radius: 5px;
margin-right: 15px;
}
.entry .right-img {
float: right;
}
```![Screenshot (87)](https://user-images.githubusercontent.com/81921974/115329898-32e9b500-a1bd-11eb-9664-f121eafd37d0.png)

```
