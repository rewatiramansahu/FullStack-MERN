Meta
Sudhakar Sharma
•
Aug 22
HTML Page Structure
1. Document Declaration
    <!DOCTYPE html>

2. Document Scope
    <html lang="en-in">

3. Head Section
    <head>
   
4. Title

5. Link

                            Meta in Head Section
- The  term meta refers to "Meta Data".
- Meta data comprises of information about your web page.
- Meta is required for a web page to make it Responsive and SEO friendly.

Meta Responsive Attributes:
- A responsive web page can adjust according the device.
- It can fit the content to device screen. [Mobile, Tab, PC, Laptop, Watch etc..]
- To test responsive pages you can download and install
            "chrome mobile simulator"

- You can add following elements into head section

  <meta  name="viewport"  content="width=device-width, initial-scale=1.0">

    a) Viewport        : It refers to screen type and its dimensions.
    b) width            : It refers to current page content width
    c) initial-scale        : It refers to zoom level. [1=100]


   <meta http-equiv="refresh"  content="5">

    a) http-equiv        : It refers to request handler, which can process your request
                      for page by refreshing every few seconds.
    b) content        : It defines the number of seconds.

- Meta provides following attributes to make the page SEO friendly.

    <meta  name="keywords"  content="some keywords used for finding your site">
    <meta  name="description"  content="something about your website">
    <meta  charset="utf-8">

        a) UTF is Unicode Transformation Format
        b) 8 = 8 bit [memory size]
       
            charset="utf-8"    => english
            charset="utf-16"    => korean, german
            charset="utf-32"    => chinese etc..
            charset="utf-64"    => arabic

Syntax:
<!DOCTYPE html>
<html lang="en-in">
<head>
  <title> Fashion Store </title>
  <link rel="shortcut icon"  href="public/images/favicon.ico">
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta http-equiv="refresh" content="5">
  <meta name="keywords" content="kids, mens, women, fashion, best offers, shirts..">
  <meta name="description"  content="Online fashion store with best offers...">
</head>
</html>

4. <style>  is used to embed css into web page

Syntax:
        <style type="text/css">

        </style>

5. <script>  is used to embed javascript into webpage

Syntax:
        <script  type="text/javascript">

        </script>
Body Section
Sudhakar Sharma
•
Aug 23
HTML Body Section
- Body section comprises of content which is rendered directly in browser.
- Body section is defined with <body> token and comprises of following attributes.

Attributes:
1. bgcolor        : It sets background color for page.
2. text            : It sets text color.


Note: HTML colors are defined by using 3 techniques
        a) Color Name
        b) Color Shade Name
        c) Hexa Decimal Code

Syntax:
    <body  bgcolor="red"  text="white">
    <body  bgcolor="lightyellow"  text="lightgreen">

Syntax: Hexa Decimal Code
- Hexa color code starts with "#"
- It can be 3 or 6 chars color code.
- 3 or 6 chars have combination of "RGB" or "RRGGBB"  [Red Green Blue]

        #RGB
        #RRGGBB

- Every color value will start from "0 to f"

        0,1,2,3,4,5,6,7,8,9,a,b,c,d,e,f            => RGB
         
- "0" to "f" is a scale which set color shade dark to bright.

        0 = dark
        f  = bright

        bgcolor="#000"            black
        bgcolor="#fff"                white
        bgcolor="#f00"            red
        bgcolor="#0f0"            green
        bgcolor="#00f"            blue

        bgcolor="#000000"            black
        bgcolor="#ff0000"            red
        bgcolor="#ad0000"            red shade

3. background            : It sets background image for body section.

Syntax:
    <body background="public/images/banner.jpg">

Note: You can control background image by using CSS attributes.
      CSS attributes are defined in a <style> container.
      CSS attributes for background are:
           
          background-repeat :  repeat | no-repeat | repeat-x | repeat-y
          background-size      :  contain | cover | width & height in pixels
          background-position: top | center | right | left | bottom [1200px or 100%]
          background-attachment: fixed | scroll

Syntax:
<head>
  <style>
      body {
       background-repeat : no-repeat;
       background-size: cover;
       background-position: center  center;
       background-attachment: fixed;
    }
  </style>
</head>
<body  background="public/images/banner.jpg">
</body>

4. align        : It aligns the body content left, center, right or justified.

Syntax:
  <body align="left | center | right | justify">
  </body>


5. leftmargin            ]    margin will set space between content and page
6. rightmargin            ]    margin is defined in pixels.
7. topmargin            ]
8. bottommargin        ]

Syntax:
  <body leftmargin="50px" rightmargin="50px" topmargin="25px" bottommargin="40px">

9. alink            : It sets color for active links in page.

10. vlink            : It sets color for visited links in page.

Syntax:
  <body  alink="red"  vlink="gray">

        <a href="http://www.amazon.in"&gt; Amazon </a>

  </body>

                    Semantics in Body Section
- Semantic elements are HTML elements defined for specific purpose.
- There are some roughly 100 semantic elements in HTML. [MDN]
- HTML 5 introduced new semantics for body section to make it more SEO friendly.
Body Section Semantics for Layout Design

- HTML 4 uses "table" element for designing a layout.
- Table is not SEO friendly.
- Tables leads to a situation known as "Kiss-Of-Death".
- HTML 5 introduced new "Semantics" for designing layout.
- The new semantics will make page SEO friendly.
- The new layout related semantics are

1. <aside>
2. <article>
3. <dialog>
4. <main>
5. <section>
6. <nav>
7. <header>
8. <footer>
9. <div>
10. <span>
11. <figure>
12. <figcaption>

Ex:
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Layout</title>
    <style>
        div {
            border: 1px solid black;
            padding: 15px;
            margin:5px;
        }
        span {
            background-color: yellow;
        }
    </style>
</head>
<body>
    <div>
        Web Technologies
        <div>
            Front End
            <div>
                HTML
                <div>
                    It is a <span>markup</span> language.
                </div>
            </div>
            <div>
                CSS
                <div>
                    It defines styles.
                </div>
            </div>
        </div>
        <div>
            Back End
            <div>
                MongoDB
                <div>
                    It is database.
                </div>
                Node JS
                <div>
                    It is server side scripting.
                </div>
            </div>
        </div>
    </div>
</body>
</html>

                            <header>
- It is used to configure header section of webpage.
- Typically every header of web page comprises of
    a) Brand Name
    b) Brand Icon
    c) Navbar
    d) Shortcut buttons etc..

                   www.getbootstrap.com => themes

Shopper Theme URL:
https://themes.getbootstrap.com/preview/?theme_id=37702

Setup Bootstrap Icons for Project
--------------------------------------------
1. Open Terminal in your project

2. Switch to command prompt

3.  Type the following command

    > npm  install  bootstrap-icons   --save

4.  NPM adds a new folder into your project by name "node_modules". It comprises of
     all library files installed using NPM.

5. To use Icons in any web page you have to link  bootstrap-icons.css file

<head>
   <link rel="stylesheet"  href="node_modules/bootstrap-icons/font/bootstrap-icons.css">
</head>

6. Every icons is stored under a class name , you have to apply the class for any container element in page.
   
        <span class="bi bi-facebook"> </span>
Install Bootstrap Icons
> npm  i  bootstrap-icons  --save

CSS File
node_modules/bootstrap-icons/font/bootstrap-icons.css

Icon Classes
bi bi-facebook
bi bi-twitter
bi bi-bell  ....

                             <header>
- It is a container that defines content to display at top margin of page.
- Typically a header in webpage comprises of brand-name, logo, shortcut buttons, navigation etc.

Syntax:
 <header>
    ........ your content....
</header>

CSS Style Attributes:
    font-size            It changes the character size [px]
    font-weight        It sets bold
    font-style            It sets italics
    font-family        It sets text  style using a font family name.
                    [Arial, Brush Script MT, Times New Roman...]
    margin            It sets all directions
    margin-left
    margin-right
    margin-top
    margin-bottom

    background-color    It sets background color for container.
    color            It sets text color.
   
    display            It can display elements in container with various styles
                    a) none
                    b) block
                    c) inline
                    d) inline-block
                    e) grid
                    f) flex

    justify-content        It can justify the elements in container with following values
                    a) space-between
                    b) space-around
                    c) space-evenly

    padding            It sets space around content in all directions
    padding-top
    padding-bottom
    padding-right
    padding-left

    border            It sets border style, side and color for container
    border-radius        It sets rounded corners
    text-align            It aligns text left, center, right or justify

Note: You can't change width and height of any span element using CSS directly.
      To set width and height for span you have to define "display:inline-block"


                            <nav>
- It is used to configure a navigation area in webpage.
- Typically nav area comprises of various nav-items or shortcut buttons.

Syntax:
    <nav>
        <span> Home </span>
        <span> Shop </span>
        <span> About </span>
    </nav>

                            <article>
- It is a container element that keeps the highlights of web page content.
- It is typically the offers, announcements, news, updates etc..

Syntax:
    <article>
         40% OFF on Electronics - Sale Ends on 31-Aug-2023
    </article>

Shopper-Template.html

<!DOCTYPE html>
<html lang="en-in">
    <head>
        <title>Shopper Template</title>
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <meta charset="utf-8">
        <link rel="stylesheet" href="node_modules/bootstrap-icons/font/bootstrap-icons.css">
        <style>
            header
            {
                font-size:25px;
                font-family: Arial;
                display: flex;
                justify-content: space-between;
                padding: 15px;
            }
            .brand-title
            {
                font-size: 30px;
                font-weight: bold;
            }
            nav span {
                margin-right: 15px;
            }
            .cart-count
            {
                background-color: red;
                color:white;
                padding: 3px;
                width: 25px;
                display: inline-block;
                border-radius: 25px;
                text-align: center;
                font-size: 15px;
            }
            article {
                background-color: black;
                text-align: center;
                color:white;
                font-size: 20px;
                padding: 20px;
            }
            .bi-lightning-fill {
                color: gold;
            }
        </style>
    </head>
    <body>
        <header>
            <div>
                <span class="brand-title">Shopper.</span>
            </div>
            <div>
                <nav>
                    <span>Home</span>
                    <span>Catalog</span>
                    <span>Shop</span>
                    <span>Pages</span>
                    <span>Blog</span>
                    <span>Docs</span>
                </nav>
            </div>
            <div>
                <nav>
                    <span class="bi bi-search"></span>
                    <span class="bi bi-person"></span>
                    <span class="bi bi-heart"></span>
                    <span class="bi bi-cart3"><span class="cart-count">2</span></span>
                </nav>
            </div>
        </header>
        <article>
            <span class="bi bi-lightning-fill"></span>
            <span>HAPPY HOLIDAY DEALS ON EVERYTHING</span>
            <span class="bi bi-lightning-fill"></span>
        </article>
    </body>
</html>
Footer, Section, Main
Body Semantics
1. <header>
2. <nav>
3. <Article>
4. <div>
5. <span>
                                 <footer>
- It defines the content to display at the bottom margin of web page.
- Typically footer comprises of copyrights, contact details, social bar, services etc.

Syntax:
    <footer>
        ... your footer content...
    </footer>

                            <aside>
- It defines the content that is not relative to current contex or that navigates the user to any another website.
- It contains contents aside the current context.

Syntax:
    <aside>
        ..... ads , social network ..
    </aside>

Note:
- "display:flex" keeps flexible columns, which change according to he width of screen.
- "display:grid" keeps fixed number of columns
- Every page can split into 12 columns max. [1200px]
- You can split the grid into columns using "grid-template-columns".
- Every column size can be in pixels [px] or in fractions [fr].
            200px    2fr
- Pixels are fixed and Fractions are responsive.

Syntax:
    footer {
        display:grid;
        grid-template-columns: 600px  600px;  (or)  6fr  6fr
    }

Note: Selecting Child and Siblings in CSS.

        parent  child            => child selector
        {
        }

        ElementA+ElementB    => Adjacent Sibling
        {
        }
   
        ElementA~ElementB    => [tild] General Sibling - all elements after specific
        {
        }

Ex: Header & Footer

<!DOCTYPE html>
<html lang="en-in">
    <head>
        <title>Shopper Template</title>
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <meta charset="utf-8">
        <link rel="stylesheet" href="node_modules/bootstrap-icons/font/bootstrap-icons.css">
        <style>
            header
            {
                font-size:25px;
                font-family: Arial;
                display: flex;
                justify-content: space-between;
                padding: 15px;
            }
            .brand-title
            {
                font-size: 30px;
                font-weight: bold;
            }
            nav span {
                margin-right: 15px;
            }
            .cart-count
            {
                background-color: red;
                color:white;
                padding: 3px;
                width: 25px;
                display: inline-block;
                border-radius: 25px;
                text-align: center;
                font-size: 15px;
            }
            article {
                background-color: black;
                text-align: center;
                color:white;
                font-size: 20px;
                padding: 20px;
            }
            .bi-lightning-fill {
                color: gold;
            }
            section {
                height: 100px;
            }
            footer {
                display: grid;
                grid-template-columns: 2.4fr 2.4fr 2.4fr 2.4fr 2.4fr;
                padding: 20px;
                background-color: black;
                color:white;
                font-family: Arial;
            }
            .footer-brand-name {
                font-size: 30px;
                font-weight: bold;
                margin-bottom: 20px;
            }
            .footer-title {
                font-size: 15px;
                font-weight: bold;
                margin-bottom: 20px;
            }
            .footer-title~span {
                display: block;
                margin-bottom: 15px;
            }
            aside span {
                margin-right: 5px;
                font-size: 20px;
            }
        </style>
    </head>
    <body>
        <header>
            <div>
                <span class="brand-title">Shopper.</span>
            </div>
            <div>
                <nav>
                    <span>Home</span>
                    <span>Catalog</span>
                    <span>Shop</span>
                    <span>Pages</span>
                    <span>Blog</span>
                    <span>Docs</span>
                </nav>
            </div>
            <div>
                <nav>
                    <span class="bi bi-search"></span>
                    <span class="bi bi-person"></span>
                    <span class="bi bi-heart"></span>
                    <span class="bi bi-cart3"><span class="cart-count">2</span></span>
                </nav>
            </div>
        </header>
        <article>
            <span class="bi bi-lightning-fill"></span>
            <span>HAPPY HOLIDAY DEALS ON EVERYTHING</span>
            <span class="bi bi-lightning-fill"></span>
        </article>
        <section>

        </section>
        <footer>
            <div>
                <div class="footer-brand-name">Shopper</div>
                <aside>
                    <span class="bi bi-facebook"></span>
                    <span class="bi bi-twitter"></span>
                    <span class="bi bi-instagram"></span>
                    <span class="bi bi-linkedin"></span>
                    <span class="bi bi-youtube"></span>
                </aside>
            </div>
            <div>
                <div class="footer-title">SUPPORT</div>
                <span>Contact Us</span>
                <span>FAQs</span>
                <span>Size Guide</span>
                <span>Shipping & Returns</span>
            </div>
            <div>
                <div class="footer-title">SHOP</div>
                <span>Men's Shopping</span>
                <span>Women's Shopping</span>
                <span>Kids' Shopping</span>
                <span>Discounts</span>
            </div>
            <div>
                <div class="footer-title">COMPANY</div>
                <span>Our Story</span>
                <span>Careers</span>
                <span>Terms & Conditions</span>
                <span>Privacy & Cookie policy</span>
            </div>
            <div>
                <div class="footer-title">CONTACT</div>
                <span>1-202-555-0105</span>
                <span>1-202-555-0106</span>
                <span>help@shopper.com</span>
            </div>
        </footer>
    </body>
</html>

Ex: Flipkart Footer

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Flipkart</title>
    <style>
        footer {
            display: grid;
            grid-template-columns: 6fr 6fr;
            height: 200px;
        }
        .col-left {
            display: grid;
            grid-template-columns: 3fr 3fr 3fr 3fr;
        }
        .col-right {
            display: grid;
            grid-template-columns: 6fr 6fr;
            border-left: 2px solid black;
            padding-left: 20px;
        }
    </style>
</head>
<body>
    <footer>
        <div class="col-left">
            <div>col-1</div>
            <div>col-2</div>
            <div>col-3</div>
            <div>col-4</div>
        </div>
        <div class="col-right">
            <div>col-1</div>
            <div>col-2</div>
        </div>                      
    </footer>
</body>
</html>
                          <section>
- It defines the content between header and footer area.
- Typically all website content is kept in section.

Syntax:
  <section>
    ....your content....
  </section>

                        <main>
- It is considered as entry point.
- User can start using your website from a specific entry point, which is "main".

Syntax:
    <main>
         get started with...
    </main>

Note: You can set transparent colours in CSS using the method "rgba()"

        rgba(red, green, blue, alpha);

        red , green, blue => 0 to 255
        alpha            =>  0 to 1

        rgba(255, 0, 0, 1);

Netflix:

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Netflix</title>
    <style>
        body{
            background-size: cover;
        }
        .shade {
            background-color: rgba(0,0,0,0.5);
            width: 105%;
            height: 100vh;
            margin-top: -10px;
            margin-left: -10px;

        }
    </style>
</head>
<body background="public/images/Netflix-Background.jpg">
    <div class="shade">

    </div>
</body>
</html>


Basic Semantics

<header>
<footer>
<aside>
<article>
<nav>
<div>
<span>
<section>
<main>

Ex:
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Netflix</title>
    <style>
        body{
            background-size: cover;
        }
        .shade {
            background-color: rgba(0,0,0,0.5);
            width: 105%;
            height: 100vh;
            margin-top: -10px;
            margin-left: -10px;

        }
        header {
            padding: 40px;
            color:white;
            font-family: Arial;
            display: flex;
            justify-content: space-between;
        }
        .brand-title {
            font-size: 35px;
            color:red;
            font-weight: bold;
        }
        .btn-signin {
            background-color: red;
            color:white;
            padding: 4px;
            border-radius: 5px;
        }
        section {
            color:white;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 400px;
            text-align: center;
            padding: 20px;
            font-family: Arial;
        }
        .title {
            font-size: 54px;
            font-weight: bold;
        }
        .sub-title {
            font-size: 30px;
            font-family: Arial;
        }
        main {
            margin-top: 40px;
        }
        .email {
            background-color: white;
            padding: 20px;
            width: 300px;
            display: inline-block;
            color:gray;
            text-align: left;
            font-size: 20px;
        }
        .btn-start {
            background-color: red;
            color:white;
            padding: 20px;
            font-size: 20px;
        }
    </style>
    <link rel="stylesheet" href="node_modules/bootstrap-icons/font/bootstrap-icons.css">
</head>
<body background="public/images/Netflix-Background.jpg">
    <div class="shade">
        <header>
            <div>
                <span class="brand-title">NETFLIX</span>
            </div>
            <div>
                <div>
                    <span class="bi bi-globe"></span>
                    <span>Language</span>
                    <span class="bi bi-chevron-down"></span>
                    <span class="btn-signin">Signin</span>
                </div>
            </div>
        </header>
        <section>
            <div>
                <div class="title">The biggest Indian hits. Ready to watch here from ₹ 149.</div>
                <div class="sub-title">Join today. Cancel anytime.</div>
                <main>
                    <span class="email">Your Email Address</span>
                    <span class="btn-start">Get Started <span class="bi bi-chevron-right"></span> </span>
                </main>
            </div>
        </section>
    </div>
</body>
</html>


Note: To display any content center screen you have to following the given process.
       - First keep all elements in one container.
               <body>
                 <div>
                  ...your content here...
                 </div>
            </body>
       - Body is the container which can display its content center with the attributes

            body {
                display:flex;
                justify-content:center;        [horizontal]
                align-items:center;            [vertical]
                height: 400px;
            }

Ex:
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        .title {
            font-size: 60px;
            font-weight: bold;
        }
        .sub-title {
            font-size: 30px;
            font-weight: bold;
        }
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            text-align: center;
            background-repeat: no-repeat;
            background-size: cover;
        }
    </style>
</head>
<body background="public/images/background-banner.jpg">
   <main>
    <div class="title">HTML</div>
    <div class="sub-title">Hyper Text Markup Language</div>
   </main>
</body>
</html>
               
                            <dialog>
- It is a popup created for page.
- You can keep any content in dialog, but it is hidden.
- You can show or hide the dialog with "open" attribute.
- You can control the dialog dynamically using JavaScript.

Syntax:
    <dialog open>
        ...your content...
    </dialog>

Ex:
<body>
    <dialog open>
        Chat with our Help Desk
    </dialog>
</body>

                        <figure> & <figcpation>

- Figure is used to encapsulate any image with a caption.
- Figcaption is used to make image SEO friendly.

Syntax:
   <figure>
    ...your image...
        <figcaption> Fig-1 </figcaption>
   </figure>

Ex:
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        figure{
            border: 1px solid black;
            height: 200px;
            width: 200px;
            padding: 20px;
        }
        figure div {
            border: 1px dotted red;
            width: 150px;
            height: 150px;
        }
    </style>
</head>
<body>
   <figure>
       <div></div>
       <figcaption>Browser Engine</figcaption>
   </figure>
</body>
</html>

Summary
1. aside
2. article
3. dialog
4. figure
5. figcaption
6. main
7. section
8. header
9. footer
10.nav
11.div
12.span

                HTML Basic Entities & Semantics for Body

1. Line Break            <br>

FAQ: What is difference between <br> & <br /> ?
Ans:  There is no <br /> in HTML.
      It is just developers coding technique to represent self ending elements i.e the
      element that doesn't have end token.

2. Blank Space        &nbsp;

Syntax:
    H &nbsp;&nbsp;T &nbsp;&nbsp;M &nbsp;&nbsp;L

3. Pre Formatted Text    <pre> It can display text with the same format defined in page.

Ex:
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        pre {
            background-color: black;
            color: white;
            padding: 10px;
            width: 300px;
        }
    </style>
</head>
<body>
   <div>
      Sample C Program
   </div>
   <div>
     <pre>
        #include &lt;stdio.h&gt;
        main()
        {
          printf("Welcome to HTML");
        }
     </pre>
   </div>
</body>
</html>
Other Semantics

1. Line Break        <br>
2. Blank Space    &nbsp;
3. Preformatted    <pre>
4. Code Block        <code>        It configures a code snippet to make SEO Friendly
5. Variables        <var>        It is used for variables in program.
6. Sample Text    <samp>        It is used for comments and captions in page.

Syntax:
   <samp> Program to Print Addition </samp>
   <code>
    <pre>
         int <var> x </var> = 10;
         int  <var> y </var> = 20;
        </pre>
   </code>

Ex:
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
       var {
         color:blue;
       }
       samp {
         color:gray;
       }
       code {
         color:brown;
       }
    </style>
</head>
<body>
    <div>
      <samp>Program to print length X Height</samp>
    </div>
    <code>
       <pre>
          #include &lt;stdio.h&gt;
          int main()
          {
             int <var>length</var> = 11;
             int <var>width</var> = 12;
             printf("%d\n", <var>length</var> * <var>width</var>);
          }
       </pre>
    </code>
</body>
</html>

7. Small Text        <small>        It sets letter size small
8. Large Text        <big>        It sets letter size large

Syntax:
    <small> your text </small>
    <big> your text </big>

9. Details & Summary        

- Details is a container that can display expandable and collapsable content.
- Summary is a caption for details container.

Syntax:
    <details>
        <summary> Title </summary>
        ... your content...
    </details>

- If you want details to expand by default, then define the attribute "open".

Syntax:
     <details open>

    </details>

Ex:
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
       details div {
          background-color: black;
          padding: 10px;
          color:white;
       }
    </style>
</head>
<body>
    <details>
        <summary>What is Netflix?</summary>
        <div>
          Netflix is a streaming service that offers a wide variety of award-winning TV shows, movies, anime, documentaries and more – on thousands of internet-connected devices.
        </div>
    </details>
    <details>
        <summary>How much does Netflix cost?</summary>
        <div>
          Netflix is a streaming service that offers a wide variety of award-winning TV shows, movies, anime, documentaries and more – on thousands of internet-connected devices.
        </div>
    </details>
</body>
</html>

Ex:
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
       details span {
          display: block;
          margin-bottom: 10px;
          margin-left: 20px;
          background-color: black;
          color:white;
          padding: 4px;
          width: 150px;
       }
    </style>
</head>
<body>
    <nav>
       <details open>
         <summary>HTML</summary>
         <span>Normal Elements</span>
         <span>Void Elements</span>
         <span>Semantics</span>
         <span>Meta</span>
       </details>
       <details>
         <summary>CSS</summary>
         <span>Stles</span>
         <span>CSS Rules</span>
         <span>CSS Units</span>
         <span>CSS Colors</span>
       </details>
    </nav>
</body>
</html>

11.  Datalist with Terms and Definitions

- HTML data list can be defined using <dl>
- It is a collection of terms defined with <dt> and definitions <dd>.

Syntax:
    <dl>
       <dt> Term </dt>
       <dd> Definition </dd>
    </dl>

Ex-1:
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
       dt {
          background-color: gray;
          color:white;
          font-weight: bold;
          padding: 4px;
          margin-bottom: 5px;
       }
    </style>
</head>
<body>
  <dl>
    <dt>HTML</dt>
    <dt>Markup Language</dt>
    <dd>It is a markup language. </dd>
    <dd>It is used for presentation.</dd>
    <dd>Designed by Tim Berners Lee.</dd>
    <dt>CSS</dt>
    <dd>It defines styles.</dd>
    <dd>It can make HTML more interactive.</dd>
    <dt>JavaScript</dt>
    <dd>It manipulates DOM.</dd>
  </dl>
</body>
</html>

Ex-2:
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        dl {
          display: grid;
          grid-template-columns: 3fr 9fr;
        }
        dt {
          background-color: black;
          color:white;
          padding: 4px;
          margin-bottom: 10px;
        }
        dd {
          background-color: lightgray;
          color:black;
          padding: 4px;
          margin-bottom: 10px;
        }
    </style>
</head>
<body>
   <dl>
      <dt>First Name</dt>
      <dd>some name</dd>
      <dt>Last Name</dt>
      <dd>some name</dd>
      <dt>Father Name</dt>
      <dd>some name</dd>
      <dt>Age</dt>
      <dd>some number</dd>
      <dt>Date of Birth</dt>
      <dd>some date</dd>
   </dl>
</body>
</html>

Note: You can make any content sticky to page by using CSS "position" attribute.

Syntax:
        dt {
         position:sticky;
         top:0px;
         }

Ex:
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
      .title {
         font-size: 25px;
         font-weight: bold;
      }
      dt {
        background-color: black;
        width: 150px;
        padding: 5px;
        color:white;
        position: sticky;
        top: 0px;
      }
    </style>
</head>
<body>
  <nav>
    <div class="title">Shopper.</div>
    <dl>
      <dt>Electronics</dt>
      <dd>Televisions</dd>
      <dd>Mobiles</dd>
      <dd>Watches</dd>
      <dd>Televisions</dd>
      <dd>Mobiles</dd>
      <dd>Watches</dd>
      <dd>Televisions</dd>
      <dd>Mobiles</dd>
      <dd>Watches</dd>
      <dd>Televisions</dd>
      <dd>Mobiles</dd>
      <dd>Watches</dd>
      <dd>Televisions</dd>
      <dd>Mobiles</dd>
      <dd>Watches</dd>
      <dd>Televisions</dd>
      <dd>Mobiles</dd>
      <dd>Watches</dd>
      <dd>Televisions</dd>
      <dd>Mobiles</dd>
      <dd>Watches</dd>
      <dd>Televisions</dd>
      <dd>Mobiles</dd>
      <dd>Watches</dd>
      <dd>Televisions</dd>
      <dd>Mobiles</dd>
      <dd>Watches</dd>
      <dt>Footwear</dt>
      <dd>Casuals</dd>
      <dd>Sneakers</dd>
      <dd>Boots</dd>
      <dd>Casuals</dd>
      <dd>Sneakers</dd>
      <dd>Boots</dd>
      <dd>Casuals</dd>
      <dd>Sneakers</dd>
      <dd>Boots</dd>
      <dd>Casuals</dd>
      <dd>Sneakers</dd>
      <dd>Boots</dd>
      <dd>Casuals</dd>
      <dd>Sneakers</dd>
      <dd>Boots</dd>
      <dd>Casuals</dd>
      <dd>Sneakers</dd>
      <dd>Boots</dd>
      <dd>Casuals</dd>
      <dd>Sneakers</dd>
      <dd>Boots</dd>
      <dd>Casuals</dd>
      <dd>Sneakers</dd>
      <dd>Boots</dd>
      <dd>Casuals</dd>
      <dd>Sneakers</dd>
      <dd>Boots</dd>
      <dd>Casuals</dd>
      <dd>Sneakers</dd>
      <dd>Boots</dd>
      <dt>Fashion</dt>
      <dd>Kids</dd>
      <dd>Women</dd>
      <dd>Men</dd>
      <dd>Kids</dd>
      <dd>Women</dd>
      <dd>Men</dd>
      <dd>Kids</dd>
      <dd>Women</dd>
      <dd>Men</dd>
      <dd>Kids</dd>
      <dd>Women</dd>
      <dd>Men</dd>
      <dd>Kids</dd>
      <dd>Women</dd>
      <dd>Men</dd>
      <dd>Kids</dd>
      <dd>Women</dd>
      <dd>Men</dd>
      <dd>Kids</dd>
      <dd>Women</dd>
      <dd>Men</dd>
      <dd>Kids</dd>
      <dd>Women</dd>
      <dd>Men</dd>
      <dd>Kids</dd>
      <dd>Women</dd>
      <dd>Men</dd>
      <dd>Kids</dd>
      <dd>Women</dd>
      <dd>Men</dd>
    </dl>
  </nav>
</body>
</html>

12. Fieldset and Legend

- Fieldset is a container with frame.
- Legend is a caption set for fieldset.
- Usually it is used for creating a group of elements in page.

Syntax:
    <fieldset>
        <legend> Title </legend>
        ...your content...
    </fieldset>

Note: You can set shadow for any container by using "box-shadow"

        {
          box-shadow : horizontal  vertical  blur  color;
        }

        horizontal, vertical, blur        =>  defined in pixels.
       
Ex:
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
      dl {
        display: grid;
        grid-template-columns: 3fr 9fr;
      }
      dt {
        background-color: black;
        color:white;
        padding: 4px;
        margin-bottom: 5px;
      }
      dd {
        background-color: lightgray;
        color:black;
        padding: 4px;
        margin-bottom: 5px;
      }
      fieldset {
        margin-bottom: 20px;
        box-shadow: 10px 10px 2px black;
        border-radius: 20px;
        background-image: url("public/images/kids.jpg");
        background-size: cover;
        width: 500px;
      }
      legend {
        text-align: center;
        background-color: black;
        color:white;
        font-weight: bold;
        padding: 4px;
        width: 150px;
        box-shadow: 5px 5px 5px gray;
        border-radius: 20px;
      }
    </style>
</head>
<body>
     <fieldset>
       <legend>Personal Details</legend>
      <dl>
        <dt>First Name</dt>
        <dd>some name</dd>
        <dt>Last Name</dt>
        <dd>some name</dd>
        <dt>Age</dt>
        <dd>some number</dd>
      </dl>
     </fieldset>
     <fieldset>
      <legend>Contact Details</legend>
      <dl>
        <dt>City</dt>
        <dd>cityname</dd>
        <dt>State</dt>
        <dd>state name</dd>
        <dt>Postal Code</dt>
        <dd>some code</dd>
      </dl>
     </fieldset>
</body>
</html>
Headings, Paragraphs, Blockquote, 

Headings in HTML

- Headings are used to keep content titles SEO friendly.
- So that SEO can make a summary of topics your page.
- Headings are defined by using <hn> token where 'n' refers to level number 1 to 6.

Syntax:
        <h1> Heading - 1 </h1>
        <h2> Heading - 2 </h2>
        .............
        <h6> Heading - 6 </h6>

FAQ's:
1. Why we have to use heading element for headings, can we configure using HTML text styles or CSS styles?
A. You can configure with HTML text style and CSS but they are not SEO friendly.
     To keep headings SEO Friendly you need <hn> element.

2. Can we change the default heading styles?
A. Yes. By using CSS.

3. Can we remove the default styles defined for heading?
A. By using CSS inheritance values you can control the default style.
    You have to use CSS inheritance value "unset".

Syntax:
    h1 {
        font-weight: unset;
        font-size:unset;        =>  all : unset;
        display:unset;
      }

Ex:
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        h1 {
            all:unset;
        }
    </style>
</head>
<body>
    <h1>Web Technologies</h1> Welcome
    <h2>Front End</h2>
    <h3>HTML</h3>
    It is a markup language.
    <h3>CSS</h3>
    It defines Styles.
    <br><br>
    <font size="4"><b>JavaScript</b></font>
    <br><br>
    It is used for DOM Manipulation.
    <h2>Back End</h2>
    <h3>Node JS</h3>
    It configures server side script.
    <h3>MongoDB</h3>
    It is a database.
</body>
</html>

Note:
 - Don't use too many headings in page. It may spam your page.
 - Never use headings to highlight any word or sentence in page.

                    Paragraph and Block Quote

- Paragraph is defined with <p> element.
- Blockquote is defined with <blockquote> element.
- Paragraph is used to define contineous blocked content.
- Blockquote is used to summarize the content that you have in page.

Syntax:
    <p> your content </p>
    <p align="center"> your content </p>
   
    <blockquote align="justify">
        ..your content...
    </blockquote>

FAQ's:
1. How to set first-line indent for paragraph or blockquote?
A. By using CSS "text-indent" attribute.

Syntax:
    p {
       text-indent: 200px;
    }

2. How to set line space, word space and character space in paragraph?
A. By using following CSS attributes
       
        line-height
        word-space
        letter-space

Syntax:
    p {
       line-height: 35px;
       word-spacing: 20px;
       letter-spacing: 5px;
    }

3. How to set Dropcap?
A. By using following styles you can set dropcap.
    a) Access the first letter by using " ::first-letter " class.
    b) Apply font styles [size, bold, italics, family]
    c) Apply CSS float as left.

Syntax:
     p :: first-letter {
        font-size : 35px;
        font-weight: bold;
        font-family: Arial;
        float : left;
     }

4. How to display contineous paragraphs side by side?
A. By using CSS "columns" attribute.
        - columns
        - column-gap
        - column-width
        - column-rule [border]

Ex:
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
       header {
         background-color: black;
         color:white;
         text-align: center;
         font-size: 50px;
         font-weight: bold;
         padding: 10px;
       }
       section {
         columns: 6;
         column-gap: 25px;
         column-rule: 2px dotted black;
         margin-top: 20px;
       }
       p {
        text-align: justify;
       }
       .para-1::first-letter {
         font-size: 35px;
         float: left;
         font-weight: bold;
       }
       h3 {
        background-color: black;
        color:white;
        padding: 2px;
       }
    </style>
</head>
<body>
   <header>
       THE HINDU
   </header>
   <section>
    <p class="para-1">Depending on how you obtained the Windows software, this is a license agreement between (i) you and the device manufacturer or software installer that distributes the software with your device; or (ii) you and Microsoft Corporation (or, based on where you live or, if a business, where your principal place of business is located, one of its affiliates) if you acquired the software from a retailer. Microsoft is the device manufacturer for devices produced by Microsoft or one of its affiliates, and Microsoft is the retailer if you acquired the software directly from Microsoft. Note that if you are a volume license customer, use of this software is subject to your volume license agreement rather than this agreement</p>
    <p> This agreement describes your rights and the conditions upon which you may use the Windows software. You should review the entire agreement, including any supplemental license terms that accompany the software and any linked terms, because all of the terms are important and together create this agreement that applies to you. You can review linked terms by pasting the (aka.ms/) link into a browser window.</p>
    <h3>Sports Updates</h3>
    <p>Depending on how you obtained the Windows software, this is a license agreement between (i) you and the device manufacturer or software installer that distributes the software with your device; or (ii) you and Microsoft Corporation (or, based on where you live or, if a business, where your principal place of business is located, one of its affiliates) if you acquired the software from a retailer. Microsoft is the device manufacturer for devices produced by Microsoft or one of its affiliates, and Microsoft is the retailer if you acquired the software directly from Microsoft. Note that if you are a volume license customer, use of this software is subject to your volume license agreement rather than this agreement</p>
    <p> This agreement describes your rights and the conditions upon which you may use the Windows software. You should review the entire agreement, including any supplemental license terms that accompany the software and any linked terms, because all of the terms are important and together create this agreement that applies to you. You can review linked terms by pasting the (aka.ms/) link into a browser window.</p>
   
    <p>Depending on how you obtained the Windows software, this is a license agreement between (i) you and the device manufacturer or software installer that distributes the software with your device; or (ii) you and Microsoft Corporation (or, based on where you live or, if a business, where your principal place of business is located, one of its affiliates) if you acquired the software from a retailer. Microsoft is the device manufacturer for devices produced by Microsoft or one of its affiliates, and Microsoft is the retailer if you acquired the software directly from Microsoft. Note that if you are a volume license customer, use of this software is subject to your volume license agreement rather than this agreement</p>
    <p> This agreement describes your rights and the conditions upon which you may use the Windows software. You should review the entire agreement, including any supplemental license terms that accompany the software and any linked terms, because all of the terms are important and together create this agreement that applies to you. You can review linked terms by pasting the (aka.ms/) link into a browser window.</p>
    <p>Depending on how you obtained the Windows software, this is a license agreement between (i) you and the device manufacturer or software installer that distributes the software with your device; or (ii) you and Microsoft Corporation (or, based on where you live or, if a business, where your principal place of business is located, one of its affiliates) if you acquired the software from a retailer. Microsoft is the device manufacturer for devices produced by Microsoft or one of its affiliates, and Microsoft is the retailer if you acquired the software directly from Microsoft. Note that if you are a volume license customer, use of this software is subject to your volume license agreement rather than this agreement</p>
    <p> This agreement describes your rights and the conditions upon which you may use the Windows software. You should review the entire agreement, including any supplemental license terms that accompany the software and any linked terms, because all of the terms are important and together create this agreement that applies to you. You can review linked terms by pasting the (aka.ms/) link into a browser window.</p>

   </section>
</body>
</html>
Text Effects and Numbering

Text Formatting in HTML

1. Font            : You can change the face, size and color of text by using <font>
                  element.

Syntax:
        <font   face=""   size=""   color=""> Your Text </font>

                face            => It is font family name.
                size            => It is number 1 to 7 level.        
                color        => It is color name, code etc.

        <font  face="Arial"  size="6"  color="red">  Text </font>

FAQ: What are websafe fonts?
Ans:  These are the fonts available to all devices. The web safe fonts are:
        a) sans-serif
        b) serif
        c) monspace

Note: W3 Standards recommends not to use <font> tag in webpage. Better use styles for formatting.


2. Font Styles        : It refers to bold & italics. HMTL provides following elements
                    <b>        Bold        <strong>
                    <i>        Italics    <em> Emphasized

Syntax:
    <b> Bold </b>
    <strong> Bold </strong>
    <i> Italics </i>
    <em> Italics </i>

FAQ: What is difference between <b> & <strong>?
Ans:  Both are same in presentation.
     They differ in documentation technique, which includes
        a) Design mode  <b>
        b) Review mode <strong>

3. Font Effects            : It refers to  underline, strikeout, super script & subscript

                     <u>        underline        <ins>   Inserted [review]
                     <strike>    strikeout        <del>   Deleted [review]
                     <sup>    super script
                     <sub>     subscript

Syntax:
    X<sup>2</sup>
    H<sub>2</sub>O

Summary:
- font
- bold [strong]
- italic [em]
- underline [ins]
- strike [del]
- superscript
- subscript

                    Ordered and Unordered List
- Ordered list is defined using <ol>
- It is auto numbering style for list of items.
- Every item is defined with <li>.

Syntax:
    <ol>
       <li> Item-1 </li>            1. Item-1
       <li> Item-2 </li>            2. Item-2
    </ol>

- You can change the numbering style by using "type" attribute.

    <ol type=" 1, A, a, i, I ">

- You can set starting level for numbering by using "start" attribute.

    <ol type="1"  start="101">
    <ol type="a"  start="5">

- You can set reverse numbering style by using "reversed" attribute.

    <ol type="1"  reversed>

Syntax:
    <ol type="1"  start="3"  reversed>
       <li> Item - 1</li>
       <li> Item - 2</li>
    </ol>

- You can create a nested list for numbering. But make sure the child list is defined with in <li> element and not below the <li> element.

    <li> Item-1 </li>            => not good
     <ol>
       <li> Child-1 </li>
    </ol>

    <li> Item-1                 => good
        <ol>
         <li> Child-1 </li>
        </ol>
    </li>

Unordered List and Styles

Format Text in HTML
- Font
    size, color, face
- Font Styles
    bold, italic, strong, emphasized
- Font Effects
    underline, inserted, strike, delete, super script, subscript
- Ordered List
    <ol>
    type
    start
    reversed
- Nested List

FAQ's:
1. How to remove numbering for ordered list?
A. You can remove numbering style using css attribute
     "list-style:none"

Syntax:
    ol {
         list-style:none;
      }

Ex:
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        ol {
            list-style: none;
           
        }
        li {
            font-size: 13px;
            margin-bottom: 10px;
        }
    </style>
</head>
<body>
    <ol>
        <h5>SUPPORT</h5>
        <li>Contact Us</li>
        <li>FAQs</li>
        <li>Size Guide</li>
        <li>Shipping & Returns</li>
    </ol>
</body>
</html>

2. How to create a scrollable list?
A. Follow the steps defined below
    - Set border for container <ol>
    - Set width and height
    - Set overflow:auto

Syntax:
    ol {
    border:1px solid gray;
    width:150px;
    height:100px;
    overflow:auto;
     }

3. How to display list items inline?
A. By using "display:flex" for ordered list.

Syntax:
    ol {
       display:flex;
       justify-content:space-between;
    }

Ex:
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
       ol {
        display: flex;
        justify-content: space-around;
        width: 500px;
       }
    </style>
</head>
<body>
    <ol>
        <li>Contact Us</li>
        <li>FAQs</li>
        <li>Size Guide</li>
        <li>Shipping & Returns</li>
    </ol>
</body>
</html>

4. How to display list in columns?
A. By using display:grid => It can display numbering left to right orientation.
    By using columns  => It can display numbering top to bottom.

Ex: Grid
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
       .choice {
        display: grid;
        grid-template-columns: 6fr 6fr;
        margin-top: 20px;
        width: 500px;
       }
       li {
         margin-bottom: 20px;
       }
    </style>
</head>
<body>
    <ol type="1">
        <li>Which one of the Following is not an OOP language.
            <ol type="a" class="choice">
                <li>C</li>
                <li>Java</li>
                <li>TypeScript</li>
                <li>C++</li>
            </ol>
        </li>
    </ol>
</body>
</html>

Ex:
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
       .choice {
        columns: 2;
        margin-top: 20px;
        width: 500px;
       }
       li {
         margin-bottom: 20px;
       }
    </style>
</head>
<body>
    <ol type="1">
        <li>Which one of the Following is not an OOP language.
            <ol type="a" class="choice">
                <li>C</li>
                <li>Java</li>
                <li>TypeScript</li>
                <li>C++</li>
            </ol>
        </li>
    </ol>
</body>
</html>

Ex:
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
       .choice {
        columns: 2;
        margin-top: 20px;
        width: 500px;
        list-style: none;
       }
       li {
         margin-bottom: 20px;
       }
    </style>
</head>
<body>
    <ol type="1">
        <li>Which one of the Following is not an OOP language.
            <ol type="a" class="choice">
                <li><input type="radio" name="q1">C</li>
                <li><input type="radio" name="q1">Java</li>
                <li><input type="radio" name="q1">TypeScript</li>
                <li><input type="radio" name="q1">C++</li>
            </ol>
        </li>
    </ol>
</body>
</html>

                            Unordered List
- It can display bulleted list.
- It comprises of symbols like circle, disc and square.
- List is configured with <ul>
- Items are configured with <li>
- You can change symbol using "type" attribute.

Syntax:
    <ul type="circle | square | disc">
    <li> Item - 1 </li>
    <li> Item - 2 </li>
    </ul>

FAQ: How to set custom bullets?
Ans : By using "list-style-image" attribute from css.

1. Create a new icon for bullet  "32x32 pixels"
2. Save into project public/images folder => bullet => type "jpeg"
3. Set Image as bullet

Syntax:
    ul {
       list-style-image: url("public/images/bullet.jpg");
       font-size:34px;
    }

Ex:
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
       ul {
         list-style-image: url("public/images/bullet.jpg");
         font-size: 34px;
       }
    </style>
</head>
<body>
   <ul>
    <li>HTML</li>
    <li>CSS</li>
    <li>JavaScript</li>
   </ul>
</body>
</html>

Note: You can set bootstrap icons for list items, instead of default bullet symbols.

Ex:
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
       ul {
         font-size: 20px;
         font-family: Arial;
         list-style: none;
       }
       li {
        margin-bottom: 20px;
       }
       .bi-tag-fill {
         color:green;
       }
       li span {
        color:black;
       }
    </style>
    <link rel="stylesheet" href="node_modules/bootstrap-icons/font/bootstrap-icons.css">
</head>
<body>
   <ul>
    <li class="bi bi-tag-fill"> <span>Bank Offer5% Cashback on Flipkart Axis Bank CardT&C</span> </li>
    <li class="bi bi-tag-fill"> <span>Special PriceGet extra ₹3000 off (price inclusive of cashback/coupon)T&C</span></li>
    <li class="bi bi-tag-fill"> <span>Extra ₹500 Off on Bikes & Scooters on purchase of ₹30,000 or moreT&C</span></li>
    <li class="bi bi-tag-fill"> <span>Partner OfferSign-up for Flipkart Pay Later & get free Times Prime Benefits worth ₹10,000*Know More</span></li>
   </ul>
</body>
</html>

Ex: Every List item with different icon

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
       ul {
         font-size: 20px;
         font-family: Arial;
         list-style: none;
       }
       li {
        margin-bottom: 20px;
        color:darkcyan;
       }
       li span {
        color:lightseagreen;
       }
    </style>
    <link rel="stylesheet" href="node_modules/bootstrap-icons/font/bootstrap-icons.css">
</head>
<body>
   <ul>
      <li class="bi bi-facebook"> <span>Facebook</span> </li>
      <li class="bi bi-twitter"> <span>Twitter</span> </li>
      <li class="bi bi-instagram"> <span>Instagram</span> </li>
      <li class="bi bi-linkedin"> <span>LinkedIn</span> </li>

   </ul>
</body>
</html>

CSS Fixed Position:
- It removes element from its normal position.
- It keeps the element top, left, right or bottom with relative to window.
- It is fixed in position and will not scroll.

Syntax:
    ul {
        position:fixed;
        right: 20px;
        bottom:20px;
    }


Ex:
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
       ul {
         font-size: 20px;
         font-family: Arial;
         list-style: none;
         position:fixed;
         right: 20px;
         bottom: 20px;
         background-color: white;
         width: 30px;
         padding: 5px;
       }
       li {
        margin-bottom: 20px;
        color:darkcyan;
       }
       li span {
        color:lightseagreen;
       }
    </style>
    <link rel="stylesheet" href="node_modules/bootstrap-icons/font/bootstrap-icons.css">
</head>
<body>
    <p>Depending on how you obtained the Windows software, this is a license agreement between (i) you and the device manufacturer or software installer that distributes the software with your device; or (ii) you and Microsoft Corporation (or, based on where you live or, if a business, where your principal place of business is located, one of its affiliates) if you acquired the software from a retailer. Microsoft is the device manufacturer for devices produced by Microsoft or one of its affiliates, and Microsoft is the retailer if you acquired the software directly from Microsoft. Note that if you are a volume license customer, use of this software is subject to your volume license agreement rather than this agreement.</p>

   <ul>
      <li class="bi bi-facebook">  </li>
      <li class="bi bi-twitter">  </li>
      <li class="bi bi-instagram">  </li>
      <li class="bi bi-linkedin"> </li>

   </ul>
</body>
</html>

Ex: Pagination

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
       ul {
         list-style: none;
         display: flex;
         font-family: Arial;
       }
       li {
         margin-right: 10px;
         width: 25px;
         padding: 5px;
         border:1px solid black;
         text-align: center;
         background-color: lightcyan;
         border-radius: 5px;
       }
       li:hover {
          background-color: black;
          color:white;
          cursor: grab;
       }
       .disabled {
          background-color: gray;
          color:white;
          border:none;
       }
       .disabled:hover {
        cursor: not-allowed;
        background-color: white;
        color:black;
       }
       body {
        display: flex;
        justify-content: center;
        align-items: end;
        height: 500px;
       }
    </style>
    <link rel="stylesheet" href="node_modules/bootstrap-icons/font/bootstrap-icons.css">
</head>
<body>
    <nav>
        <ul>
            <li> <span>&laquo;</span> </li>
            <li> <span>1</span> </li>
            <li> <span>2</span> </li>
            <li> <span>3</span> </li>
            <li class="disabled"> <span>4</span> </li>
            <li> <span>5</span> </li>
            <li> <span>...</span> </li>
            <li> <span>&raquo;</span> </li>
        </ul>
    </nav>
</body>
</html>

Images in HTML

- Images are of various types.
- Web will not support all image types.
- Web supports the following image types to embed in web page.

Type        MIME Type        		Description                    			Extention
----------------------------------------------------------------------------------------------------------------
PNG        image/png      			Portable Network Graphics            .png
 
APNG        image/apng     			Animated Portable Network Graphics   .apng

JPEG        image/jpeg    			Joint Photographic Expert Group       .jpg, .jpeg, .jfif

GIF         image/gif       		Graphic Interchange Format            .gif

 TIFF       image/tiff     			Tagged Image File Format            .tiff

 SVG     	application/svg-xml   	Scalar Vector Graphics            	.svg

 BMP        image/bmp       		Bitmap                            .bmp

 ICO       	image/icon       		Microsoft Icon                    .ico

 Webp       application/webp    	Web Picture                    .webp


Purpose of Various Image Types:

PNG, APNG                :  High Definition, More Pixel Depth
                           More memory space required.
                           You have to use PNG type only for downloads.

JPG                        :  High Definition, Good Pixel Depth [less than PNG]
                           It is compressed image format. Less memory space.
                           You have to use JPG for on screen presentation.

GIF                        :  Only 256 colors, Less Pixels
                           Memory is same like JPG.
                           It can be animated.
                           You have to use for buttons, logos, bullets, borders
                           background patterns etc..

SVG                        : It is not pixel based.
                          It is vector based image.
                          It is an XML format image.
                          You have to use for architectural diagrams,
                          flow charts, maps, icons etc.

Webp                    : It is embedded into page and intergrated into page.
                          You can't separate from page.

ICO                        : It is used for shortcut icons [favicon]


Embed Images into Web Page:
- You can embed image into web page by using <img> element.
- It provides various attributes

        src                : It refers to image path and name
        alt                : It refers to alternative text to display when image fails to
                          load.
        title                : It defines a tooltip to display when mouse is over image.
        width / height        : It sets image width and height
        border            : It sets border for image
        align                : It sets image alignment left or right on page. It can
                          control the wrapping to content around image.
        vspace / hspace    : It set horizontal and vertical space between image and
                          other contents in page.

Syntax:
    <img  src="path">


Ex:
<img src="public/images/realme-black.jpg" title="30% OFF - Offer End on 5 Sep 2023" alt="Realme-Black" 
width="300" height="400">


		---  Image Attributes and Examples  ---

Formats
  PNG, APNG, JPEG, GIF, TIFF, SVG, Bitmap, ICO
Embed Image
  <img>
Attributes
    src
    alt
    title
    width
    height
    border
    align
    hspace
    vspace        

Ex:
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Image</title>
    <style>
        header {
            font-family: Arial;
            font-size: 20px;
            display: flex;
            justify-content: space-around;
            padding: 20px;
        }
        nav span {
            margin-right: 40px;
            color:grey;
        }
        .brand-title {
            font-size: 24px;
            font-weight: bold;
            color:blue;
        }
        header button {
            font-size: 20px;
            background-color: blue;
            color:white;
            border:none;
            padding: 5px;
            border-radius: 10px;
        }
        .main-title {
            font-size: 50px;
            font-family: Arial;
            margin-left: 100px;
            margin-top: 50px;
        }
        .main-subtitle {
            font-family: Arial;
            margin-left: 100px;
            margin-top: 20px;
            font-size: 25px;
            line-height: 40px;
        }
        .main-buttons {
            margin-left: 100px;
            margin-top: 50px;
        }
        .btn-pages, .btn-doc {
            font-size: 20px;
            padding: 10px;
            width: 200px;
            border: none;
        }
        .btn-pages {
            background-color: blue;
            color:white;
        }
        .btn-doc {
            background-color: whitesmoke;
        }
    </style>
    <link rel="stylesheet" href="node_modules/bootstrap-icons/font/bootstrap-icons.css">
</head>
<body>
   <header>
      <div>
         <span class="brand-title">Landkit.</span>
      </div>
      <div>
        <nav>
            <span>Landings</span>
            <span>Pages</span>
            <span>Account</span>
            <span>Documentation</span>
        </nav>
      </div>
      <div>
         <button>
            Buy now
         </button>
      </div>
   </header>
   <section>
        <main>
            <img src="public/images/work.jpg" align="right" width="600">
            <div>
                <div class="main-title">
                    Welcome to Landkit.<br>
                    Develop anything.
                </div>
                <div class="main-subtitle">
                    Build a beautiful, modern website with flexible Bootstrap components built from scratch.
                </div>
                <div class="main-buttons">
                    <button class="btn-pages">View Pages <span class="bi bi-arrow-right"></span> </button>
                    <button class="btn-doc">Documentation</button>
                </div>
            </div>
        </main>
   </section>
</body>
</html>

Advanced Attributes:

1. crossorigin [CORS]       : It controls Cross Origin Resource Sharing.
                        You can configure with "use-credentials" or "anonymous".

     <img  src="http://someserver.com/images/pic.jpg&quot;  crossorigin="use-credentials">

2. decoding              : It defines how image have to load along with other contents
                        on page. It can "Sync, Async or Auto".

      <img src="public/images/pic.jpg"  decoding="sync | async | auto">

3. importance             : It sets priority for loading images, which can be low, high or
                       auto.

    <img src="public/images/pic.jpg"  importance="low">

4. srcset                 : It can configure a set of images as source, so that they
                      can change according to situation.

    <img  srcset="collection of images">

Ex: Cards

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="node_modules/bootstrap-icons/font/bootstrap-icons.css">
    <style>
        body {
            display: flex;
            background-color: gray;
        }
        .card {
            width: 340px;
            border:1px solid gray;
            padding: 10px;
            font-family: Arial;
            margin: 20px;
            background-color: white;
        }
        .card-pic {
            float: left;
            padding-right: 20px;
        }
        .card-body {
            clear: left;
        }
        .card-subtitle {
            font-size: 15px;
            color:gray;
            margin-top: 10px;
        }
        .card-title {
            font-size: 20px;
            margin-top: 10px;
        }
        .card-rating {
            margin-top: 1%;
            color:goldenrod;
        }
        .card-body {
            text-align: justify;
            line-height: 35px;
            height: 150px;
        }
        .card-footer {
            text-align: center;
            color:gray;
        }
    </style>
</head>
<body>
   <div class="card">
      <div class="card-header">
          <img src="public/images/card-pic.jpg" class="card-pic">
          <div>
            <div class="card-subtitle">Dresses</div>
            <div class="card-title">Cotton print Dresses</div>
            <div class="card-rating">
                <span class="bi bi-star-fill"></span>
                <span class="bi bi-star-fill"></span>
                <span class="bi bi-star-fill"></span>
                <span class="bi bi-star-fill"></span>
                <span class="bi bi-star-half"></span>
            </div>
          </div>
      </div>
      <div class="card-body">
         <p>This agreement describes your rights and the conditions upon which you may use the Windows software. </p>
      </div>
      <div class="card-footer">
          30% OFF Sale Ends 10-Sep-2023
      </div>
   </div>


   <div class="card">
    <div class="card-header">
        <img src="public/images/kids.jpg" width="70" class="card-pic">
        <div>
          <div class="card-subtitle">Dresses</div>
          <div class="card-title">Cotton print Dresses</div>
          <div class="card-rating">
              <span class="bi bi-star-fill"></span>
              <span class="bi bi-star-fill"></span>
              <span class="bi bi-star-fill"></span>
              <span class="bi bi-star-fill"></span>
              <span class="bi bi-star-half"></span>
          </div>
        </div>
    </div>
    <div class="card-body">
       <p>This agreement describes your rights and the conditions upon which you may use the Windows software. </p>
    </div>
    <div class="card-footer">
        30% OFF Sale Ends 10-Sep-2023
    </div>
 </div>
</body>
</html>


Template Designs with Cards

FAQ's: How to design fluid Image?
Ans: You can design fluid images by configuring the size in "%".
   
        <img width="50%" height="40%">
        <img width="50%" height="100">

Ex: Amazon Cards-

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        section {
            display: grid;
            grid-template-columns: 3fr 3fr 3fr 3fr;
            grid-gap: 10px;
            margin-top: -250px;
        }
        .card {
            background-color: white;
            height: 400px;
            padding: 5px;
            margin: 5px;
            font-family: Arial;
        }
        .card-title {
            font-size: 25px;
            font-weight: bold;
        }
        .card-header {
            padding: 5px;
        }
        .row {
            display: grid;
            grid-template-columns: 6fr 6fr;
            grid-gap: 5px;
        }
        .row img {
            width: 100%;
        }
        .footer-title {
            color:blue;
        }
        .card-footer {
            padding: 5px;
        }
    </style>
</head>
<body bgcolor="lightgray">
    <header>
        <img src="public/images/amazonBanner.jpg" width="100%">
    </header>
    <section>
        <div class="card">
            <div class="card-header">
                <div class="card-title">Up to 60% off | Styles for men</div>
            </div>
            <div class="card-body">
                <div class="row">
                    <div>
                        <img src="public/images/a1.jpg">
                        <p>Clothing</p>
                    </div>
                    <div>
                        <img src="public/images/a2.jpg">
                        <p>Footwear</p>
                    </div>
                </div>
                <div class="row">
                    <div>
                        <img src="public/images/a3.jpg">
                        <p>Watches</p>
                    </div>
                    <div>
                        <img src="public/images/a4.jpg">
                        <p>Bags</p>
                    </div>
                </div>
            </div>
            <div class="card-footer">
                <div class="footer-title">See all offers</div>
            </div>
        </div>
        <div class="card">
            <div class="card-header">
                <div class="card-title">Up to 60% off | Styles for men</div>
            </div>
            <div class="card-body">
                <div class="row">
                    <div>
                        <img src="public/images/a1.jpg">
                        <p>Clothing</p>
                    </div>
                    <div>
                        <img src="public/images/a2.jpg">
                        <p>Footwear</p>
                    </div>
                </div>
                <div class="row">
                    <div>
                        <img src="public/images/a3.jpg">
                        <p>Watches</p>
                    </div>
                    <div>
                        <img src="public/images/a4.jpg">
                        <p>Bags</p>
                    </div>
                </div>
            </div>
            <div class="card-footer">
                <div class="footer-title">See all offers</div>
            </div>
        </div>
        <div class="card">
            <div class="card-header">
                <div class="card-title">Up to 60% off | Styles for men</div>
            </div>
            <div class="card-body">
                <div class="row">
                    <div>
                        <img src="public/images/a1.jpg">
                        <p>Clothing</p>
                    </div>
                    <div>
                        <img src="public/images/a2.jpg">
                        <p>Footwear</p>
                    </div>
                </div>
                <div class="row">
                    <div>
                        <img src="public/images/a3.jpg">
                        <p>Watches</p>
                    </div>
                    <div>
                        <img src="public/images/a4.jpg">
                        <p>Bags</p>
                    </div>
                </div>
            </div>
            <div class="card-footer">
                <div class="footer-title">See all offers</div>
            </div>
        </div>
        <div class="card">
            <div class="card-header">
                <div class="card-title">Up to 60% off | Styles for men</div>
            </div>
            <div class="card-body">
                <div class="row">
                    <div>
                        <img src="public/images/a1.jpg">
                        <p>Clothing</p>
                    </div>
                    <div>
                        <img src="public/images/a2.jpg">
                        <p>Footwear</p>
                    </div>
                </div>
                <div class="row">
                    <div>
                        <img src="public/images/a3.jpg">
                        <p>Watches</p>
                    </div>
                    <div>
                        <img src="public/images/a4.jpg">
                        <p>Bags</p>
                    </div>
                </div>
            </div>
            <div class="card-footer">
                <div class="footer-title">See all offers</div>
            </div>
        </div>
    </section>
</body>
</html>


Ex: Shopper Templates

<!DOCTYPE html>
<html lang="en-in">
    <head>
        <title>Shopper Template</title>
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <meta charset="utf-8">
        <link rel="stylesheet" href="node_modules/bootstrap-icons/font/bootstrap-icons.css">
        <style>
            header
            {
                font-size:25px;
                font-family: Arial;
                display: flex;
                justify-content: space-between;
                padding: 15px;
            }
            .brand-title
            {
                font-size: 30px;
                font-weight: bold;
            }
            nav span {
                margin-right: 15px;
            }
            .cart-count
            {
                background-color: red;
                color:white;
                padding: 3px;
                width: 25px;
                display: inline-block;
                border-radius: 25px;
                text-align: center;
                font-size: 15px;
            }
            article {
                background-color: black;
                text-align: center;
                color:white;
                font-size: 20px;
                padding: 20px;
            }
            .bi-lightning-fill {
                color: gold;
            }
            section {
                height: 600px;
            }
            footer {
                display: grid;
                grid-template-columns: 2.4fr 2.4fr 2.4fr 2.4fr 2.4fr;
                padding: 20px;
                background-color: black;
                color:white;
                font-family: Arial;
            }
            .footer-brand-name {
                font-size: 30px;
                font-weight: bold;
                margin-bottom: 20px;
            }
            .footer-title {
                font-size: 15px;
                font-weight: bold;
                margin-bottom: 20px;
            }
            .footer-title~span {
                display: block;
                margin-bottom: 15px;
            }
            aside span {
                margin-right: 5px;
                font-size: 20px;
            }
            .women-fashion {
                background-image: url("public/images/women-fashion.jpg");
                background-size: cover;
                display: flex;
                justify-content: center;
                align-items: center;
                opacity: 0.5;
            }
            .men-fashion {
                background-image: url("public/images/men-fashion.jpeg");
                background-size: cover;
                display: flex;
                justify-content: center;
                align-items: center;
                opacity: 0.5;
            }
            .kids-fashion {
                background-image: url("public/images/kids-fashion.jpg");
                background-size: cover;
                display: flex;
                justify-content: center;
                align-items: center;
                opacity: 0.5;
            }
            .kids-fashion:hover {
                opacity: 1;
            }
            .women-fashion:hover {
                opacity: 1;
            }
            .men-fashion:hover {
                opacity: 1;
            }
            main {
                height: 500px;
                display: grid;
                grid-template-columns: 4fr 4fr 4fr;
                grid-gap: 4px;
                margin-top: 5px;
            }
            .card-title {
                font-size: 50px;
                font-weight: bold;
                color:white;
                text-shadow: 2px 2px 2px black;
            }
            button {
                width: 200px;
                height: 50px;
                font-size: 20px;
                background-color: white;
                border:none;
                margin-top: 150px;
            }
        </style>
    </head>
    <body>
        <header>
            <div>
                <span class="brand-title">Shopper.</span>
            </div>
            <div>
                <nav>
                    <span>Home</span>
                    <span>Catalog</span>
                    <span>Shop</span>
                    <span>Pages</span>
                    <span>Blog</span>
                    <span>Docs</span>
                </nav>
            </div>
            <div>
                <nav>
                    <span class="bi bi-search"></span>
                    <span class="bi bi-person"></span>
                    <span class="bi bi-heart"></span>
                    <span class="bi bi-cart3"><span class="cart-count">2</span></span>
                </nav>
            </div>
        </header>
        <article>
            <span class="bi bi-lightning-fill"></span>
            <span>HAPPY HOLIDAY DEALS ON EVERYTHING</span>
            <span class="bi bi-lightning-fill"></span>
        </article>
        <section>
            <main>
                <div class="women-fashion">
                    <div class="card">
                        <div class="card-title">
                            Women
                        </div>
                        <div class="card-footer">
                            <button>
                                Shop Women <span class="bi bi-arrow-right"></span>
                            </button>
                        </div>
                    </div>
                </div>
                <div class="men-fashion">
                  <div class="card">
                    <div class="card-title">
                        Men
                    </div>
                    <div class="card-footer">
                        <button>
                            Shop Men <span class="bi bi-arrow-right"></span>
                        </button>
                    </div>
                  </div>
                </div>
                <div class="kids-fashion">
                   <div class="card">
                    <div class="card-title">
                        Kids
                    </div>
                    <div class="card-footer">
                        <button>
                            Shop Kids <span class="bi bi-arrow-right"></span>
                        </button>
                    </div>
                   </div>
                </div>
            </main>
        </section>
        <footer>
            <div>
                <div class="footer-brand-name">Shopper</div>
                <aside>
                    <span class="bi bi-facebook"></span>
                    <span class="bi bi-twitter"></span>
                    <span class="bi bi-instagram"></span>
                    <span class="bi bi-linkedin"></span>
                    <span class="bi bi-youtube"></span>
                </aside>
            </div>
            <div>
                <div class="footer-title">SUPPORT</div>
                <span>Contact Us</span>
                <span>FAQs</span>
                <span>Size Guide</span>
                <span>Shipping & Returns</span>
            </div>
            <div>
                <div class="footer-title">SHOP</div>
                <span>Men's Shopping</span>
                <span>Women's Shopping</span>
                <span>Kids' Shopping</span>
                <span>Discounts</span>
            </div>
            <div>
                <div class="footer-title">COMPANY</div>
                <span>Our Story</span>
                <span>Careers</span>
                <span>Terms & Conditions</span>
                <span>Privacy & Cookie policy</span>
            </div>
            <div>
                <div class="footer-title">CONTACT</div>
                <span>1-202-555-0105</span>
                <span>1-202-555-0106</span>
                <span>help@shopper.com</span>
            </div>
        </footer>
    </body>
</html>


Links in HTML -


- Link is clickable text, picture or graphic that navigates the user from one location to another when clicked.
- You can call a link in webpage as a "Hyperlink", as it takes you beyond what you see.
- Links are created by using <a> anchor element.

            <a>   Text  | Picture | Graphic   </a>

- Every link requires a reference path, which is defined using "href".

            <a href="path"> Text | Picture | Graphics </a>

- Links in a webpage are classified into 2 types

        1. Intra Document Links
        2. Inter Document Links

Intra Document Links:
- These are the hyperlinks that navigate user from one location to another with in the same page.
- To create intra document links the target element must have a reference ID.

        <h2  id="fashion">
        <img  id="realme">
        <ol  id="list">

- User can navigate to reference ID by using <a> element.

         <a href="#fashion">  Fashion </a>
         <a href="#realme"> Realme </a>
         <a href="#list">   <img src="">  </a>
       
FAQ: How to remove underline for hyperlinks?
Ans : By using style attribute  "text-decoration" set to "none".

Syntax:
        a {    
          text-decoration: none;
        }

FAQ: How to change color for visited  & active links?
Ans:  By using HTML <body> attributes "alink & vlink"
                (or)
      By using CSS class ":link, :visited,  :active"

Syntax:
        <body  alink="red"  vlink="gray">

        a:visited {   }
        a:active {   }
        a:link {   }

FAQ: What is difference between src & href?
Ans:   "src" is a getter, it get the value from specified path and uses for element.
       "href" is a setter, it sets the path in URL and appends into browser address bar.

Syntax:
        http://127.0.0.1:5500/public/fashion.html#kids
 
Ex:
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Shopping</title>
    <link rel="stylesheet" href="node_modules/bootstrap-icons/font/bootstrap-icons.css">
    <style>
        header {
            font-size: 30px;
            text-align: center;
            padding: 5px;
            background-color: darkcyan;
            color:white;
        }
        section {
            display: grid;
            grid-template-columns: 3fr 9fr;
            margin-top: 20px;
        }
        main {
            height: 500px;
            overflow: auto;
        }
        ul {
            list-style: none;
            margin-left: -40px;
        }
        li {
            font-size: 20px;
            width: 150px;
            border:1px solid black;
            background-color: darkcyan;
            padding: 5px;
            margin-bottom: 30px;
        }
       nav a {
            text-decoration: none;
            color:white;
        }
       nav a:visited {
            color: yellow;
        }
    </style>
</head>
<body>
    <header>
        <span class="bi bi-cart4"></span> Fashion Store
    </header>
    <section>
        <nav>
            <ul>
                <li><a href="#home">Home</a></li>
                <li><a href="#women">Women's Fashion</a></li>
                <li><a href="#men">Men's Fashion</a></li>
                <li><a href="#kid">Kid's Fashion</a></li>
            </ul>
        </nav>
        <main>
            <h2 id="home">Home</h2>
            <p>We understand that <span><a href="#realme">Mobile Offers</a></span> you may have questions about the Microsoft Services Agreement. We have an FAQ page (https://www.microsoft.com/en-us/servicesagreement/upcoming-faq.aspx) that provides more information, including what Microsoft products and services it covers. Whenever we make changes, we provide a summary of the most notable changes to the current Microsoft Services Agreement. We will also continue to provide a summary of the changes to the previous version, and a link to the previous version, of the Microsoft Services Agreement on the Summary of Changes (https://www.microsoft.com/en-us/servicesagreement/upcoming-updates.aspx) page.</p>
            
            <h2 id="women">Women's Fashion</h2>
            <img src="public/images/women-fashion.jpg" width="200" height="300">
            <div>
                <a href="#home">Back to Top</a>
            </div>
            <p>We understand that you may have questions about the Microsoft Services Agreement. We have an FAQ page (https://www.microsoft.com/en-us/servicesagreement/upcoming-faq.aspx) that provides more information, including what Microsoft products and services it covers. Whenever we make changes, we provide a summary of the most notable changes to the current Microsoft Services Agreement. We will also continue to provide a summary of the changes to the previous version, and a link to the previous version, of the Microsoft Services Agreement on the Summary of Changes (https://www.microsoft.com/en-us/servicesagreement/upcoming-updates.aspx) page.</p>
          
            <h2 id="men">Men's Fashion</h2>
            <img src="public/images/men-fashion.jpeg" width="200" height="300">
            <div>
                <a href="#home">Back to Top</a>
            </div>
            <p>We understand that you may have questions about the Microsoft Services Agreement. We have an FAQ page (https://www.microsoft.com/en-us/servicesagreement/upcoming-faq.aspx) that provides more information, including what Microsoft products and services it covers. Whenever we make changes, we provide a summary of the most notable changes to the current Microsoft Services Agreement. We will also continue to provide a summary of the changes to the previous version, and a link to the previous version, of the Microsoft Services Agreement on the Summary of Changes (https://www.microsoft.com/en-us/servicesagreement/upcoming-updates.aspx) page.</p>
            
            <figure id="realme">
                <img src="public/images/realme-black.jpg" width="300" height="300">
                <figcaption>Realme-Black 50% OFF</figcaption>
            </figure>
            <p>We understand that you may have questions about the Microsoft Services Agreement. We have an FAQ page (https://www.microsoft.com/en-us/servicesagreement/upcoming-faq.aspx) that provides more information, including what Microsoft products and services it covers. Whenever we make changes, we provide a summary of the most notable changes to the current Microsoft Services Agreement. We will also continue to provide a summary of the changes to the previous version, and a link to the previous version, of the Microsoft Services Agreement on the Summary of Changes (https://www.microsoft.com/en-us/servicesagreement/upcoming-updates.aspx) page.</p>

        </main>
    </section>
</body>
</html>

Ex:
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Shopping</title>
    <link rel="stylesheet" href="node_modules/bootstrap-icons/font/bootstrap-icons.css">
    <style>
        header {
            font-size: 30px;
            text-align: center;
            padding: 5px;
            background-color: darkcyan;
            color:white;
        }
        section {
            display: grid;
            grid-template-columns: 3fr 9fr;
            margin-top: 20px;
        }
        main {
            height: 400px;
            overflow: auto;
        }
        ul {
            list-style: none;
            margin-left: -40px;
        }
        li {
            font-size: 20px;
            width: 150px;
            border:1px solid black;
            background-color: darkcyan;
            padding: 5px;
            margin-bottom: 30px;
        }
        a{
            text-decoration: none;
        }
       nav a, header a {
           
            color:white;
        }
       nav a:visited {
            color: yellow;
        }
        header img {
            width: 100px;
            height: 100px;
            border-radius: 100px;
        }
    </style>
</head>
<body>
    <header>
        <a href="#home"><span class="bi bi-cart4"></span> Fashion Store</a>
        <div>
            <a href="#women"> <img src="public/images/women-fashion.jpg"> </a>
            <a href="#men"> <img src="public/images/men-fashion.jpeg"> </a>
            <a href="#kid"> <img src="public/images/kids-fashion.jpg"> </a>
        </div>
    </header>
    <section>
        <nav>
            <ul>
                <li><a href="#home">Home</a></li>
                <li><a href="#women">Women's Fashion</a></li>
                <li><a href="#men">Men's Fashion</a></li>
                <li><a href="#kid">Kid's Fashion</a></li>
            </ul>
        </nav>
        <main>
            <h2 id="home">Home</h2>
            <p>We understand that <span><a href="#realme">Mobile Offers</a></span> you may have questions about the Microsoft Services Agreement. We have an FAQ page (https://www.microsoft.com/en-us/servicesagreement/upcoming-faq.aspx) that provides more information, including what Microsoft products and services it covers. Whenever we make changes, we provide a summary of the most notable changes to the current Microsoft Services Agreement. We will also continue to provide a summary of the changes to the previous version, and a link to the previous version, of the Microsoft Services Agreement on the Summary of Changes (https://www.microsoft.com/en-us/servicesagreement/upcoming-updates.aspx) page.</p>
            
            <h2 id="women">Women's Fashion</h2>
            <img src="public/images/women-fashion.jpg" width="200" height="300">
            <div>
                <a href="#home">Back to Top</a>
            </div>
            <p>We understand that you may have questions about the Microsoft Services Agreement. We have an FAQ page (https://www.microsoft.com/en-us/servicesagreement/upcoming-faq.aspx) that provides more information, including what Microsoft products and services it covers. Whenever we make changes, we provide a summary of the most notable changes to the current Microsoft Services Agreement. We will also continue to provide a summary of the changes to the previous version, and a link to the previous version, of the Microsoft Services Agreement on the Summary of Changes (https://www.microsoft.com/en-us/servicesagreement/upcoming-updates.aspx) page.</p>
     
            <h2 id="men">Men's Fashion</h2>
            <img src="public/images/men-fashion.jpeg" width="200" height="300">
            <div>
                <a href="#home">Back to Top</a>
            </div>
            <p>We understand that you may have questions about the Microsoft Services Agreement. We have an FAQ page (https://www.microsoft.com/en-us/servicesagreement/upcoming-faq.aspx) that provides more information, including what Microsoft products and services it covers. Whenever we make changes, we provide a summary of the most notable changes to the current Microsoft Services Agreement. We will also continue to provide a summary of the changes to the previous version, and a link to the previous version, of the Microsoft Services Agreement on the Summary of Changes (https://www.microsoft.com/en-us/servicesagreement/upcoming-updates.aspx) page.</p>
         
            <figure id="realme">
                <img src="public/images/realme-black.jpg" width="300" height="300">
                <figcaption>Realme-Black 50% OFF</figcaption>
            </figure>
            <p>We understand that you may have questions about the Microsoft Services Agreement. We have an FAQ page (https://www.microsoft.com/en-us/servicesagreement/upcoming-faq.aspx) that provides more information, including what Microsoft products and services it covers. Whenever we make changes, we provide a summary of the most notable changes to the current Microsoft Services Agreement. We will also continue to provide a summary of the changes to the previous version, and a link to the previous version, of the Microsoft Services Agreement on the Summary of Changes (https://www.microsoft.com/en-us/servicesagreement/upcoming-updates.aspx) page.</p>
            <p>We understand that you may have questions about the Microsoft Services Agreement. We have an FAQ page (https://www.microsoft.com/en-us/servicesagreement/upcoming-faq.aspx) that provides more information, including what Microsoft products and services it covers. Whenever we make changes, we provide a summary of the most notable changes to the current Microsoft Services Agreement. We will also continue to provide a summary of the changes to the previous version, and a link to the previous version, of the Microsoft Services Agreement on the Summary of Changes (https://www.microsoft.com/en-us/servicesagreement/upcoming-updates.aspx) page.</p>
            <p>We understand that you may have questions about the Microsoft Services Agreement. We have an FAQ page (https://www.microsoft.com/en-us/servicesagreement/upcoming-faq.aspx) that provides more information, including what Microsoft products and services it covers. Whenever we make changes, we provide a summary of the most notable changes to the current Microsoft Services Agreement. We will also continue to provide a summary of the changes to the previous version, and a link to the previous version, of the Microsoft Services Agreement on the Summary of Changes (https://www.microsoft.com/en-us/servicesagreement/upcoming-updates.aspx) page.</p>
            <h2 id="kid">Kid's Fashion</h2>
            <img src="public/images/kids-fashion.jpg" width="200" height="200">
            <div>
                <a href="#home">Back to Top</a>
            </div>
            <p>We understand that you may have questions about the Microsoft Services Agreement. We have an FAQ page (https://www.microsoft.com/en-us/servicesagreement/upcoming-faq.aspx) that provides more information, including what Microsoft products and services it covers. Whenever we make changes, we provide a summary of the most notable changes to the current Microsoft Services Agreement. We will also continue to provide a summary of the changes to the previous version, and a link to the previous version, of the Microsoft Services Agreement on the Summary of Changes (https://www.microsoft.com/en-us/servicesagreement/upcoming-updates.aspx) page.</p>
            <p>We understand that you may have questions about the Microsoft Services Agreement. We have an FAQ page (https://www.microsoft.com/en-us/servicesagreement/upcoming-faq.aspx) that provides more information, including what Microsoft products and services it covers. Whenever we make changes, we provide a summary of the most notable changes to the current Microsoft Services Agreement. We will also continue to provide a summary of the changes to the previous version, and a link to the previous version, of the Microsoft Services Agreement on the Summary of Changes (https://www.microsoft.com/en-us/servicesagreement/upcoming-updates.aspx) page.</p>
            <p>We understand that you may have questions about the Microsoft Services Agreement. We have an FAQ page (https://www.microsoft.com/en-us/servicesagreement/upcoming-faq.aspx) that provides more information, including what Microsoft products and services it covers. Whenever we make changes, we provide a summary of the most notable changes to the current Microsoft Services Agreement. We will also continue to provide a summary of the changes to the previous version, and a link to the previous version, of the Microsoft Services Agreement on the Summary of Changes (https://www.microsoft.com/en-us/servicesagreement/upcoming-updates.aspx) page.</p>
            <p>We understand that you may have questions about the Microsoft Services Agreement. We have an FAQ page (https://www.microsoft.com/en-us/servicesagreement/upcoming-faq.aspx) that provides more information, including what Microsoft products and services it covers. Whenever we make changes, we provide a summary of the most notable changes to the current Microsoft Services Agreement. We will also continue to provide a summary of the changes to the previous version, and a link to the previous version, of the Microsoft Services Agreement on the Summary of Changes (https://www.microsoft.com/en-us/servicesagreement/upcoming-updates.aspx) page.</p>
            <p>We understand that you may have questions about the Microsoft Services Agreement. We have an FAQ page (https://www.microsoft.com/en-us/servicesagreement/upcoming-faq.aspx) that provides more information, including what Microsoft products and services it covers. Whenever we make changes, we provide a summary of the most notable changes to the current Microsoft Services Agreement. We will also continue to provide a summary of the changes to the previous version, and a link to the previous version, of the Microsoft Services Agreement on the Summary of Changes (https://www.microsoft.com/en-us/servicesagreement/upcoming-updates.aspx) page.</p>
            <p>We understand that you may have questions about the Microsoft Services Agreement. We have an FAQ page (https://www.microsoft.com/en-us/servicesagreement/upcoming-faq.aspx) that provides more information, including what Microsoft products and services it covers. Whenever we make changes, we provide a summary of the most notable changes to the current Microsoft Services Agreement. We will also continue to provide a summary of the changes to the previous version, and a link to the previous version, of the Microsoft Services Agreement on the Summary of Changes (https://www.microsoft.com/en-us/servicesagreement/upcoming-updates.aspx) page.</p>
            <p>We understand that you may have questions about the Microsoft Services Agreement. We have an FAQ page (https://www.microsoft.com/en-us/servicesagreement/upcoming-faq.aspx) that provides more information, including what Microsoft products and services it covers. Whenever we make changes, we provide a summary of the most notable changes to the current Microsoft Services Agreement. We will also continue to provide a summary of the changes to the previous version, and a link to the previous version, of the Microsoft Services Agreement on the Summary of Changes (https://www.microsoft.com/en-us/servicesagreement/upcoming-updates.aspx) page.</p>

        </main>
    </section>
</body>
</html>











Note: CSS provides a ":target" class that identifies the target container and sets effects dynamically.

Ex:
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        .card {
            width: 200px;
            height: 100px;
            padding: 50px;
            border:1px solid black;
            box-shadow: 2px 2px 2px gray;
            margin: 20px;
        }
        .card:target {
            background-color: black;
            color:white;
        }
        section {
            display: flex;
        }
        nav span {
            margin-right: 100px;
        }
        nav {
            text-align: center;
        }
    </style>
</head>
<body>
    <nav>
        <span><a href="#html">HTML</a></span>
        <span><a href="#css">CSS</a></span>
        <span><a href="#js">JavaScript</a></span>
    </nav>
   <section>
    <div class="card" id="html">
        <h2>HTML</h2>
        <p>It is a markup language</p>
    </div>
    <div class="card" id="css">
        <h2>CSS</h2>
        <p>It defines styles</p>
    </div>
    <div class="card" id="js">
        <h2>JavaScript</h2>
        <p>It manipulates DOM</p>
    </div>
   </section>
</body>
</html>

		********Inter Document Links**********


- An inter document link can handle following
    1. It can link to any "file".
    2. It can link to any remote "url".
    3. It can invoke any "application".
    4. It can invoke any script "function".

Link to File:
- You can create a hyper link that navigates the user to any specified document in project.
- You can link any type of document, image, html, word docs, spread sheets, ppts, text documents, audio, video etc..
- Every linked document can't open in browser.
- Browser need special extentions [plugin's] to open special type of files.
- If file related plugin is not available in browser then file will download.

Syntax:
    <a href="./public/images/kids.jpg"> Kids Fashion </a>        can open in browser
    <a href="./shopper-template.html"> Shopper </a>        can open in browser
    <a href="./public/docs/js.pdf"> JavaScript </a>            can open in browser
    <a href="./public/docs/resume.docx"> Resume </a>        will download

- HTML 5 provides "download" attribute for hyperlink, which download the linked document always.

Syntax:
    <a href="./public/images/kids.jpg"  download>   Kids </a>
    <a href="./public/images/kids.jpg"  download="kids-fashion">

Link to URL:
- You can link any website URL or any specific resource on server.
- When you link URL make sure that is configured with proper "protocol" and "domain name".
           
Syntax:
    <a href="https://www.amazon.in"&gt; Shop on Amazon </a>
    <a href="https://www.youtube.com/nareshit"&gt;  Naresh IT </a>
    <a href="https://api.nasa.gov..../photos/pic.jpg"&gt; Nasa Photo </a>

Link to Applications:
- You can create a hyperlink that can invoke application, which is running in your device.
- You have to make sure that the relative application is already installed in your device.
- Most commonly linked applications with anchor element are:
        mail, skype, telephone, others with web address

Syntax:
    <a href="name@gmail.com">  Email </a>
    <a href="skype:name@outlook.com"> Skype </a>
    <a href="tel:+919988774342"> Call </a>
    <a href="https://api.whatsapp.com/&gt; Whatsapp </a>    link to url

Link JavaScript function:
- You can link JavaScript functions using hyperlink
- A function contains code snippet [code block] that executes and performs specified functionality.

Syntax:
  <a href="javascript:window.print()">  Print Page </a>
  <a href="javascript:functionName()">   Execute </a>


                        YouTube

Ex:
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="node_modules/bootstrap-icons/font/bootstrap-icons.css">
</head>
<body>
    <h2>Favorites</h2>
    <ol>
        <li><a href="javascript:window.print()"> <span class="bi bi-printer-fill"></span> Print </a></li>
        <li>More more details you can mail <a href="hr@nareshit.com">hr@nareshit.in</a></li>
        <li>You can <a href="skype:nareshit@outlook.com">skype</a> us.</li>
        <li>You can call <a href="tel:9994848382">9994848432</a></li>
        <li>Whatsup <a href="https://api.whatsapp.com">99983845573</a&gt; </li>
        <li><a href="./shopper-template.html">Shopper Template</a></li>
        <li><a href="./public/images/kids-fashion.jpg">Kids Fashion Banner</a></li>
        <li><a href="./public/images/women-fashion.jpg" download="IMG001WF">Women Fashion</a></li>
        <li><a href="./public/docs/JavaScript.pdf">JavaScript Tutorial</a></li>
        <li><a href="./public/docs/Angular-14.doc">Angular Word Document</a></li>
        <li><a href="https://www.youtube.com/nareshit">NareshIT Youtube Channel</a></li>
        <li>
            <a href="http://mars.jpl.nasa.gov/msl-raw-images/msss/01000/mcam/1000ML0044631210305218E01_DXXX.jpg"&gt;
                <img src="http://mars.jpl.nasa.gov/msl-raw-images/msss/01000/mcam/1000ML0044631210305218E01_DXXX.jpg&quot; width="100" height="100">
            </a>
        </li>
    </ol>
</body>
</html>

Inter Document Links
- To File
- To Url
- To Application
- To JavaScript functions


FAQ's:
1. How to remove underline for Hyperlink?
A. By using CSS "text-decoration:none"

Syntax:
    a{
      text-decoration:none;
    }

2. How to set colours for active & visited links?
A. By using <body> attributes "alink" & "vlink"
    By using CSS classes  ":visited"  & ":active"

3. How to download linked document always?
A. By using "download" attribute for <a> element.

4. How to open linked document in new tab?
A. By using "target" attribute for <a> set to "_blank".

     <a  href="public/images/fashion.jpg"  target="_blank"> Fashion </a>
 
5. How to open linked document in new window?
A. By using JavaScript function "window.open()".

      <a href="javascript:window.open('path', 'title', 'features')">  Text | Image </a>

Ex:
 <a href="javascript:window.open('public/images/fashion.jpg', 'Fashion', 'width=300 height=400')">   Fashion </a>


6. How to open linked document in the same window along with other contents in page?
A. You can embed any external document into page by using an <iframe>.
     Iframe allows you to access and browse other page contents from current page.
     Iframe can embed any type of document supported by browser plugin's.
    [image, html, pdf, text etc..]
     You can set link target that refers to iframe name.
     
Syntax:
    <iframe  src="you can load any url or file by default"   name="ref">

        </iframe>
   
     <a href="some_path"  target="iframe_ref_name">  Text </a>

Ex:
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        body {
            display: grid;
            grid-template-columns: 3fr 9fr;
        }
        iframe {
            width: 100%;
            height: 100vh;
            border:none;
        }
    </style>
</head>
<body>
   <nav>
    <div>
        <a href="public/images/women-fashion.jpg" target="_blank">Women Fashion</a>
    </div>
    <div>
        <a href="javascript:window.open('public/images/men-fashion.jpeg','Men','width=300 height=400')">Men Fashion</a>
    </div>
    <div>
        <a target="main-frame" href="public/images/kids-fashion.jpg">Kids Fashion</a>
    </div>
    <div>
        <a href="public/docs/JavaScript.pdf" target="main-frame">JavaScript Tutorial</a>
    </div>
    <div>
        <a href="http://www.amazon.in&quot; target="_blank">Amazon</a>
    </div>
    <div>
        <a href="https://www.youtube.com/embed/DeEszXEewHs&quot; target="main-frame">Web UI Fullstack Video</a>
    </div>
    <div>
        <a href="https://www.youtube.com/embed/tm7kVn8abSg&quot; target="main-frame">React JS</a>
    </div>
   </nav>
   <main>
        <iframe name="main-frame"></iframe>
   </main>
</body>
</html>


Ex:
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <h2>Web Technology</h2>
    <iframe src="https://www.youtube.com/embed/DeEszXEewHs"></iframe&gt;
    <iframe src="https://www.youtube.com/embed/tm7kVn8abSg"></iframe&gt;
    <iframe width="300" height="300" src="https://www.slideshare.net/slideshow/embed_code/key/x0szDrukZzOTEY?startSlide=1&quot; width="597" height="486" frameborder="0" marginwidth="0" marginheight="0" scrolling="no" style="border:1px solid #CCC; border-width:1px; margin-bottom:5px;max-width: 100%;" allowfullscreen></iframe><div style="margin-bottom:5px"><strong><a href="https://www.slideshare.net/lexinamer/html-css-57982559&quot; title="HTML & CSS" target="_blank">HTML & CSS</a></strong> from <strong><a href="https://www.slideshare.net/lexinamer&quot; target="_blank">lexinamer</a></strong></div>

</body>
</html>


YouTube Design

Ex: YouTube

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>YouTube-NareshIT</title>
    <link rel="stylesheet" href="node_modules/bootstrap-icons/font/bootstrap-icons.css">
    <style>
        header {
            font-size: 25px;
            display: flex;
            justify-content: space-between;
            padding-left: 20px;
            padding-right: 20px;
        }
        .search-bar {
            color:gray;
            font-size: 20px;
            border:1px solid gray;
            padding-left: 10px;
            padding-right: 10px;
            padding-top: 5px;
            width: 400px;
            border-radius: 30px;
            display: flex;
            justify-content: space-between;
        }
        .profile-pic {
            border-radius: 30px;
            border:1px solid black;
        }
        .shortcut-buttons span {
            margin-right: 20px;
        }
        .search-area {
            display: flex;
        }
        .bi-mic-fill {
            margin-left: 20px;
        }
        section {
            display: grid;
            grid-template-columns: 1fr 11fr;
            margin-top: 20px;
        }
        .nav-item {
            font-size: 25px;
            margin-bottom: 40px;
            margin-top: 20px;
            text-align: center;
        }
        .nav-item span {
            font-size: 15px;
        }
        article {
            margin-top: 20px;
            font-family: Arial;
            display: grid;
            grid-template-columns: 10fr 2fr;
        }
        .title {
            font-size: 25px;
            margin-bottom: 20px;
            margin-top: 5px;
        }
        .sub-title {
            font-size: 15px;
            margin-bottom: 20px;
        }
        .subscribe {
            padding: 5px;
            background-color: black;
            width: 120px;
            border-radius: 10px;
            color:white;
        }
        .text {
            margin-bottom: 10px;
        }
        a {
            text-decoration: none;
        }
        .categories {
            padding: 20px;
            font-family: Arial;
            font-size: 17px;
            font-weight: bold;
            display: flex;
            justify-content: space-between;
            color:gray;
            text-transform: uppercase;
        }
        .videos {
            padding: 20px;
            font-family: Arial;
            font-size: 20px;
        }
        .thumbnails {
            display: grid;
            grid-template-columns: 2fr 2fr 2fr 2fr 2fr;
        }
        iframe {
            width: 220px;
            height: 130px;
        }
    </style>
</head>
<body>
    <header>
        <div>
            <span class="bi bi-justify"></span>
            <img src="public/images/youtube-logo.jpg" width="100">
        </div>
        <div class="search-area">
            <div class="search-bar">
                <span>Search</span>
                <span class="bi bi-search"></span>
            </div>
            <span class="bi bi-mic-fill"></span>
        </div>
        <div class="shortcut-buttons">
            <span class="bi bi-camera-video"></span>
            <span class="bi bi-bell-fill"></span>
            <img class="profile-pic" src="public/images/men-fashion.jpeg" width="30" height="30">
        </div>
    </header>
    <section>
        <nav>
          <div class="nav-item">
            <div class="bi bi-house-door"></div>
            <span>Home</span>
          </div>
          <div class="nav-item">
            <div class="bi bi-film"></div>
            <span>Shorts</span>
          </div>
          <div class="nav-item">
            <div class="bi bi-collection-play"></div>
            <span>Subscribe</span>
          </div>
          <div class="nav-item">
            <div class="bi bi-camera-video"></div>
            <span>Library</span>
          </div>
        </nav>
        <main>
            <div>
                <img src="public/images/channel-banner.jpg" width="100%">
            </div>
            <article>
                <div>
                    <img src="public/images/nit-logo.jpg" align="left" width="140">
                    <div class="title">Naresh i Technologies</div>
                    <div class="sub-title">@NareshIT1.19M subscribers2.8K videos</div>
                    <div class="text">We are one of the India's largest software training organization and an..</div>
                    <div><a href="instagram.com/nareshitech">instagram.com/nareshitech</a>
                        and 7 more links</div>
                </div>
                <div>
                    <div class="subscribe">
                       <span class="bi bi-bell-fill"></span> <span>Subscribe</span>
                       <span class="bi bi-chevron-down"></span>
                    </div>
                </div>
            </article>
            <div class="categories">
                <span>Home</span>
                <span>Videos</span>
                <span>Shorts</span>
                <span>Live</span>
                <span>Playlists</span>
                <span>Community</span>
                <span>Channels</span>
                <span>About</span>
            </div>
            <div class="videos">
                <span>Videos</span>
                <span class="bi bi-play-fill"></span>
                <span>Play All</span>
            </div>
            <div class="thumbnails">
                <div>
                    <iframe src="https://www.youtube.com/embed/Ft-v5aLDWqc"></iframe&gt;
                </div>
                <div>
                    <iframe src="https://www.youtube.com/embed/DeEszXEewHs"></iframe&gt;
                </div>
                <div>
                    <iframe src="https://www.youtube.com/embed/DeEszXEewHs"></iframe&gt;
                </div>
                <div>
                    <iframe src="https://www.youtube.com/embed/DeEszXEewHs"></iframe&gt;
                </div>
                <div>
                    <iframe src="https://www.youtube.com/embed/DeEszXEewHs"></iframe&gt;
                </div>
            </div>
        </main>
    </section>
</body>
</html>
ALTER TABLE [dbo].[rateplan]
ADD IsBulkBuy INT NULL;


		##### Table Attributes and Examples #####

Table Elements
<table>
<caption>
<colgroup>
<thead>
<tbody>
<tfoot>
<tr>
<th>
<td>

Table Attributes
1. Frame, Rules and Border
2. Cellspacing & Cellpadding
3. BgColor & Background

    bgcolor            : It sets background color for table, group, row or cell.
    background        : It sets background image for table, group, row or cell.

Note: You can't manipulate columns in HTML table.



4. align & valign

    align            : It aligns the cell content left, center, right or justify horizontally.
    valign        : It aligns the cell content top, center, bottom vertically.

5. height & width    

    height        : It defines height for table, group, row, cell.
    width        : It defines with for table or cell.

Note: You can change width of cell which effects all cells in the column.
      You can manipulate width of column.
      Always define height for <tr> and width for <th> or <td>.

Syntax:
        <tr height="50">
        <th width="100">
        <td width="100>
        <table width="100%">

Ex:
 <!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Asia Cup Table</title>
    <style>
        table {
            font-family: Arial;
        }
        table img {
            width: 30px;
        }
        .w {
            background-color: green;
            color:white;
            padding: 3px;
            border-radius: 5px;
        }
        .l {
            background-color: red;
            color:white;
            padding: 3px;
            border-radius: 5px;
        }
        .a {
            background-color: gray;
            color:white;
            padding: 3px;
            border-radius: 5px;
        }
        table span {
            display: inline-block;
            width: 20px;
            text-align: center;
        }
        caption {
            margin-bottom: 30px;
        }
    </style>
</head>
<body>
    <table width="100%"  border="1" frame="void" cellspacing="5" cellpadding="5" >
        <caption>Asia Cup Point Table 2023 - Group A</caption>
        <colgroup span="10"></colgroup>
        <thead >
            <tr height="50" valign="center">
                <th>Pos</th>
                <th colspan="2">Teams</th>
                <th>Matches</th>
                <th>Won</th>
                <th>Lost</th>
                <th>Tied</th>
                <th>NR</th>
                <th>Points</th>
                <th>NRR</th>
                <th colspan="2">Series Form</th>
            </tr>
        </thead>
        <tbody>
            <tr align="center">
                <td>1</td>
                <td><img src="public/images/pak.jpg"></td>
                <td align="left" width="150">Pakistan</td>
                <td>2</td>
                <td>1</td>
                <td>0</td>
                <td>0</td>
                <td>1</td>
                <td>3</td>
                <td>+4.760</td>
                <td><span class="w">W</span></td>
                <td><span class="a">A</span></td>
            </tr>
            <tr align="center">
                <td>2</td>
                <td><img src="public/images/india.jpg"></td>
                <td align="left">India</td>
                <td>2</td>
                <td>1</td>
                <td>0</td>
                <td>0</td>
                <td>1</td>
                <td>3</td>
                <td>+1.028</td>
                <td><span class="a">A</span></td>
                <td><span class="w">W</span></td>
            </tr>
            <tr align="center">
                <td>3</td>
                <td><img src="public/images/nepal.jpg"></td>
                <td align="left">Nepal</td>
                <td>2</td>
                <td>0</td>
                <td>2</td>
                <td>0</td>
                <td>0</td>
                <td>0</td>
                <td>-3.572</td>
                <td><span class="l">L</span></td>
                <td><span class="l">L</span></td>
            </tr>
        </tbody>
        <tfoot>
            <tr>
                <td colspan="12">
                    Pos: Position, Pld: Played, Pts: Points, NRR: Net Run Rate
                </td>
            </tr>
        </tfoot>
    </table>
</body>
</html>

6. colspan and rowspan

    colspan        : It can merge multiple cells into one column.
    rowspan        : It can merge multiple cells into one row.

Note: You can define rowspan and colspan only for <td> or <th>.

    <td colspan="4">
    <td rowspan="3">
    <th colspan="5">

Ex:
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <table width="100%" border="1">
        <thead>
            <tr>
                <th colspan="2">Name</th>
                <th colspan="3">Address</th>
            </tr>
            <tr>
                <th>First Name</th>
                <th>Last Name</th>
                <th>City</th>
                <th>State</th>
                <th>Postal Code</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>&nbsp;</td>
                <td>&nbsp;</td>
                <td rowspan="6" align="center">
                    D <br>
                    E <br>
                    L <br>
                    H <br>
                    I
                </td>
                <td>&nbsp;</td>
                <td>&nbsp;</td>
            </tr>
            <tr>
                <td>&nbsp;</td>
                <td>&nbsp;</td>
                <td>&nbsp;</td>
                <td>&nbsp;</td>
            </tr>
            <tr>
                <td>&nbsp;</td>
                <td>&nbsp;</td>
                <td>&nbsp;</td>
                <td>&nbsp;</td>
            </tr>
            <tr>
                <td>&nbsp;</td>
                <td>&nbsp;</td>
                <td>&nbsp;</td>
                <td>&nbsp;</td>
            </tr>
            <tr>
                <td>&nbsp;</td>
                <td>&nbsp;</td>
                <td>&nbsp;</td>
                <td>&nbsp;</td>
            </tr>
            <tr>
                <td>&nbsp;</td>
                <td>&nbsp;</td>
                <td>&nbsp;</td>
                <td>&nbsp;</td>
            </tr>
        </tbody>
        <tfoot>
            <tr>
                <td colspan="5" align="center">&copy; copyright 2023</td>
            </tr>
        </tfoot>
    </table>
</body>
</html>





Summary
1. frame
2. border
3. rules
4. cellspacing
5. cellpadding
6. align
7. valign
8. bgcolor
9. background
10. width
11. height
12. rowspan
13. colspan

Note: You can use table for designing a layout.

Ex:
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <table width="100%" border="1" frame="void" cellspacing="5" cellpadding="5">
        <tr>
            <td colspan="3">Header</td>
        </tr>
        <tr height="400">
            <td width="100">Nav</td>
            <td>Main</td>
            <td width="100">Aside</td>
        </tr>
        <tr>
            <td colspan="3">Footer</td>
        </tr>
    </table>
</body>
</html>

Ex:
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        td img {
            width: 150px;
        }
        table {
            font-family: Arial;
        }
    </style>
</head>
<body bgcolor="gray">
    <table border="1"  cellspacing="10" frame="void" cellpadding="5" width="100%">
        <tr height="400" bgcolor="white">
            <td width="300">
                <table>
                    <tr>
                        <td colspan="2">
                            <h2>Up to 60% off | Styles for men</h2>
                        </td>
                    </tr>
                    <tr>
                        <td>
                            <img src="public/images/a1.jpg">
                            <p>Clothing</p>
                        </td>
                        <td>
                            <img src="public/images/a2.jpg">
                            <p>Footwear</p>
                        </td>
                    </tr>
                    <tr>
                        <td>
                            <img src="public/images/a3.jpg">
                            <p>Watches</p>
                        </td>
                        <td>
                            <img src="public/images/a4.jpg">
                            <p>Bags</p>
                        </td>
                    </tr>
                    <tr>
                        <td colspan="2">
                            <a href="#">see more</a>
                        </td>
                    </tr>
                </table>
            </td>
            <td>

            </td>
            <td>

            </td>
            <td>

            </td>
        </tr>
        <tr height="200" bgcolor="white">
            <td colspan="4" background="public/images/asi.jpg">
               
            </td>
        </tr>
    </table>
</body>
</html>



	======  Forms and Task Design Example  =====

<!DOCTYPE html>

<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Weather</title>
    <style>
        .parent-table {
            border-radius: 10px;
            background-image: url("public/images/weather.jpg");
            background-size: cover;
        }
        .loc-title {
            font-size: 20px;
            color:white;
            text-shadow: 1px 1px 1px black;
            font-family: Arial;
        }
        .loc-title p {
            font-size: 15px;
            text-shadow: 1px 1px 1px black;
        }
        .icons {
            font-size: 20px;
            color:white;
        }
        .unit, .bi-water {
            font-size: 80px;
            font-weight: bold;
            font-family: Arial;
            color:yellow;
            text-shadow: 1px 1px 1px black;
        }
        .cf {
            font-size: 25px;
            font-family: Arial;
            color:white;
        }
        .cf-w {
            font-size: 18px;
            font-family: Arial;
            color:white;
        }
        .parent-table table {
            font-family: Arial;
            color:white;
        }
        .slider {
            width: 100%;
        }
       
    </style>
	
    <link rel="stylesheet" href="node_modules/bootstrap-icons/font/bootstrap-icons.css">
</head>
<body>
    <table class="parent-table" width="50%" height="400" cellpadding="20">
      <tr>
        <td class="loc-title" colspan="3" valign="top">
            Ameerpet, TG
            <p>Updated few sec ago</p>
        </td>
        <td class="icons" colspan="2" align="right" valign="top">
            <span class="bi bi-share-fill"></span>
            <span class="bi bi-three-dots"></span>
        </td>
      </tr>
      <tr>
        <td width="10">
            <span class="bi bi-water"></span>
        </td>
        <td class="unit" width="10">
            28
        </td>
        <td align="center" class="cf" width="10">
            &deg;C <br>
            <hr color="black" width="10">
            F
        </td>
        <td class="cf">
            30&deg;<br><br>
            23&deg;
        </td>
        <td class="cf-w" valign="top">
             Percipitation: 2% <br><br>
             Wind: 8 KMPH <br><br>
             Humidity: 61%
        </td>
      </tr>
      <tr>
        <td colspan="5" class="cf-w">
            Haze - Tue 8, 11:43 am
        </td>
      </tr>
      <tr>
        <td colspan="5">
            <table width="100%">
                <tr align="center">
                    <td align="left">12 PM</td>
                    <td>3 PM</td>
                    <td>6 PM</td>
                    <td>9 PM</td>
                    <td>12 AM</td>
                    <td>3 AM</td>
                    <td>6 AM</td>
                    <td align="right">9 AM</td>
                </tr>
                <tr>
                    <td colspan="8">
                        <input type="range" value="1" class="slider">
                    </td>
                </tr>
            </table>
        </td>
      </tr>
      <tr>
        <td colspan="5">
            <table width="100%" cellpadding="5" border="0" frame="void" cellspacing="5">
                <tr height="160" bgcolor="gray">
                    <td class="details" align="center">
                        Tue 8 <br>
                        <span class="bi bi-water"></span> <br>
                        30&deg;<br>
                        23&deg;
                    </td>
                    <td>
                        Tue 8 <br>
                        <span class="bi bi-water"></span> <br>
                        30&deg;<br>
                        23&deg;
                    </td>
                    <td>
                        Tue 8 <br>
                        <span class="bi bi-water"></span> <br>
                        30&deg;<br>
                        23&deg;
                    </td>
                    <td>
                        Tue 8 <br>
                        <span class="bi bi-water"></span> <br>
                        30&deg;<br>
                        23&deg;
                    </td>
                    <td>
                        Tue 8 <br>
                        <span class="bi bi-water"></span> <br>
                        30&deg;<br>
                        23&deg;
                    </td>
                    <td>
                        Tue 8 <br>
                        <span class="bi bi-water"></span> <br>
                        30&deg;<br>
                        23&deg;
                    </td>
                    <td>
                        Tue 8 <br>
                        <span class="bi bi-water"></span> <br>
                        30&deg;<br>
                        23&deg;
                    </td>
                    <td>
                        Tue 8 <br>
                        <span class="bi bi-water"></span> <br>
                        30&deg;<br>
                        23&deg;
                    </td>
                </tr>
            </table>
        </td>
      </tr>
      <tr>
        <td></td>
      </tr>
    </table>
</body>
</html>




                            Forms in HTML
- A form provides UI from where user can interact with data.
- It allows to handle CRUD operations.

            C        - Create [Register, Insert]
            R        - Read
            U        - Update
            D        - Delete

- Form provides an interface with various set of elements like button, textbox, checkbox, radio, listbox, dropdown etc..

- Form is a generic container, which have default functionality.
- A form can submit and reset its data without configuring any explicity functionality.
- A form is created by using <form> element.

Syntax:
        <form>
            ... your form elements...
        </form>

- Form comprises of following attributes

1. Id                : It is a unique reference given for form in order to access in CSS
                  or in JavaScript.

2. Name            : It defines a reference name for form.


3. Class            : It defines a css class to configure styles.

Syntax:
        <form  id="frmLogin"  name="LoginForm"  class="form-container">

        </form>

4. Method        : It defines the form behaviour, every form in HTML have 2 methods
                    a) GET
                    b) POST

                  GET is used to fetch data from server.
                  POST is used to submit data to server.

Syntax:
        <form  id="frmRegister"   method="post | get">

        </form>

FAQ: What is the default method?
Ans : GET

FAQ: Can we submit data to server on GET method?
Ans:  Yes. But it is not recommended always.


GET
- It is used mostly for fetching data from server.
- You can submit data to server on GET.
- Data is appended into URL as "Query String".
- Every user can view your data.
- It is not safe.
- It is easy to hack your data.
- You can't submit complex data, like binary data.
- You can submit max 2048 chars.
- It stored in browser logs: history.
- It can be bookmarked.
- Data can be cached, which saves round trips.

POST
- It is used mostly for submitting data to server.
- It stores the data in "Form Body".
- It is not visible to users directly.
- It is safe when compared to GET.
- It is not stored in browser logs.
- It can't be bookmarked.
- It is hard to hack.
- You can submit any amount of data, there is no limit for data.
- You can submit complex data, i.e binary data.
- Data is not cached.


		=====  Form Attributes and Textbox =====

Form Attributes

1. id
2. name
3. class
4. method
5. action        :  It refers to the target path where form data is submitted.
                [can be client side or server side page]

Syntax:
    <form method="get"  action="results.html | results.jsp..">
    </form>


6. novalidate    : It can disable the default validations provided by HTML.
              If you are writing custom validations then you can by-pass the default
              validations.

Syntax:
    <form method="get"  actions="results.html"  novalidate>
        </form>

                          Form Elements
- HTML provides various form elements to handle interactions
    <input>
    <select>
    <option>
    <optgroup>
    <datalist>
    <meter>
    <progress>
    <textarea>  etc..

                            Input Element
- HTML <input> is responsible for configuring an input that allows any type of data.
- HTML 5 provided various input types to manage different types of data like number, string, date, email, phone number etc.

Syntax:
        Name    : <input>
        Age        : <input>
        Email    : <input>
        DOB    : <input>

                            TextBox
- A textbox allows user to input a string.
- It provides various attributes for managing and restricting string.
   [ string is a group alpha, numeric and special characters]
- Textbox is designed by using
      <input type=text">

Attributes:
1. id
2. name
3. class

Note: Every form element must have a "name".
          If name is not defined for any element, then form can't submit its value.

     <input type="text"  name="txtCity">
     <input type="text"  name="txtName">

4. value        : It defines the default value to display in textbox.

5. readonly    : It will not allow to modify the default value in textbox. But it allows to
              submit the value.

6. disabled    : It will not allow to modify and submit the value.

Syntax:
    <input type="text"  value="Delhi"  name="txtCity"  readonly>
    <input type="text"   value="Delhi" name="txtCity"  disabled>

7. placeholder    :  It defines the watermark text to display in textbox when value is not
               defined.

Syntax:
    <input type="text" placeholder="Search Amazon.in">

8. size        : It defines the width for textbox, the default is "20".
              It is not restricting textbox, it is only width for textbox.

9. maxlength    : It restricts the maximum number of chars in textbox.

Syntax:
    <input type="text" name="txtOTP"  size="4"  maxlength="4">

10. minlength    : It validates the minimum number of chars in textbox.

Syntax:
    <input type="text"  name="txtOTP  size="4"  minlength="4" maxlength="4">

11. required    : It will not allow to submit empty. It defines that value is mandatory.

Syntax:
    <input type="text"  name="txtOTP" required>


12. autofocus    : It sets focus to textbox automatically on page load.

Syntax:
     <input type="text"  name="txtName"  autofocus>

13. list        : It configures a data list to textbox, which is displayed as autocomplete
              text.        
              Form data list is defined using the elements.
                    <datalist>
                    <option>

Ex:
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="node_modules/bootstrap-icons/font/bootstrap-icons.css">
    <style>
       
    </style>
</head>
<body>
    <form align="center">
       <h1>Google</h1>
       <input type="text" name="txtSearch" size="40" list="topics">
       <datalist id="topics">
          <option>HTML Examples</option>
          <option>CSS Projects</option>
          <option>CSS Examples</option>
          <option>JavaScript Projects</option>
          <option>HTML Projects</option>
       </datalist>
       <p>
        <button>Search</button>
       </p>
       
    </form>
</body>
</html>


				---------------  Regular Expression  ---------------

14. Pattern        : It is used to validate the format of input value.
                  Pattern uses a regular expression for verifying the format of value.
                  A regular expression is built by using meta characters & quantifiers

 Meta Character            Description
----------------------------------------------------------------------------------------------------
 ?                        Zero or one occurance of any character.

                        Syntax:
                         pattern="colou?r"       => color, colour

 *                        Zero or more occurances of any character.

                        Syntax:
                        pattern="colou*r"    => color, colour, colouur, colouuur...

+                        One or more occurances of any character.

                        Syntax:
                        pattern="colou+r"    => colour, colouur, colouuur...

. (dot)                    Any single character [A-Za-z0-9!@#$%^&]
                       
                        Syntax:
                        pattern=".o."    => wow, dos, you, toy, 1o4, $o3, 1oA..
                        pattern=".o.?"    =>  wow, dos, to
                        pattern=".at"    =>  cat, mat, bat, rat, 1at, $at
                        pattern=".?at"    =>  cat, mat, at

\                        It is an escape sequence character, that can transform
                        meta character into normal char and vice versa.

                        Syntax:
                        pattern="gmail.com"    => gmail3com, gmail#com
                        pattern="gmail\.com"    => gmail.com

 | [pipe]                    It refers to logical "OR" [any one of specified]

                        Syntax:
                        pattern="red|blue|green"   => red, blue, green

^                        It excludes the specified chars.

                        Syntax:
                        pattern="[a,d,s]"   =>  a , d , s  
                        pattern="[^a,d,s]"  =>  all are allowed excluding a,d,s.

[ ]                        It defines the range of chars.

                        Syntax:
                        pattern="[a,d,s]"        => a, d, s
                        pattern="[a-z]"            => a to z
                        pattern="[0-9]"            => 0 to 9 all numbers
                        pattern="[a-d,4-9]        => a to d and 4 to 9
                        pattern="[a-zA-Z0-9]    => alpha numeric
                        pattern="[A-Z]"        => only uppercase letters
                        pattern="[^A-Z]"        => excluding upper case all                                                          others allowed.
\^                        Start with

$                        Ends with

                        Syntax:
                        pattern="\^ .... your expression... $"
                        pattern="\^[a-z]\.[0-9]$"


		=====  Meta Chars and Quantifiers  ======

Meta Characters
    ?            zero or one occurance
    *            zero or more
    +            one or more
    |            OR
    .            any single char
    \            escape sequence
    [ ]            range
    ^            exclude
    \^            start with
    $            end with
    ( )            It is union of chars & expression.

    \d            Single digit number  [0-9]

                Syntax:
                pattern="\d\d"        => 12, 46, 37, 25, 99
                pattern="\d\d?"    =>  12, 3,
               
    \D            Non numeric value. [a-z,A-Z,!@#$%^&]

                Syntax:
                pattern="\d\D"        => 3a, 3B, 3@, 3#
               
    \s            Single blank space
   
                Syntax:
                pattern="\d\s\d"    => 3 1,

    \w            It refers to word chars.
                [ a-zA-Z0-9_ ]

                Syntax:
                pattern="\w"        => 3, a, A, _

    \W            It refers to no-word chars. [all special chars]
                [ a - z A - Z 0 - 9 _ ] => not allowed

                Syntax:
                pattern="\w\W"    => 1#, a@, A$            
                pattern="\w[@#$]    => 3@, a#, A$

    \i            Ignore case [capitalization]

                Syntax:
                pattern="Colour\i"       => colour, Colour, COLOUR

Quantifier            Description
------------------------------------------------------------------------
 {n}                    exactly n-number of chars
                   
                    Syntax:
                    pattern="\d{3}"

 {n,m}                minimum-n and maximum-m  chars

                    Syntax:
                    pattern="\w{4,15}"

 {n, }                    minimum-n  and maximum-any

                    Syntax:
                    pattern="\w{4, }"

Regular expressions [pre-defined]:

    (?=.*[A-Z])            At least one upper case letter at any place.
    (?=.*[a-z])            at least one lower case letter.
    (?=.*[0-9])            at least one numeric
    (?=.*[!@#$%])            at least one special character

Ex:
1. Write a pattern to validate mobile number starting with +91 and 10 digits.

            pattern="\+91\d{10}"

2. Write a pattern to validate US mobile format

            +(1)(425) 555-0100

            pattern="\+\(1\)\(\d{3}\)\s\d{3}-\d{4}"

3. Write pattern for UK mobile format
           
            +(44)(20) 1234 5678

            pattern="\+\(44\)\(\d{2}\)\s\d{4}\s\d{4}"

4.  Write a pattern to validate IFSC codes
   
            SBIN0070264

            pattern="SBIN00\d{5}"

5.  Write a pattern for user name 4 to 15 chars alpha numeric. Special chars not allowed.
   
            pattern="[A-Za-z0-9]{4,15}"        => special chars not allowed
            pattern="\w{4,15}"                => underscore allowed

6. Write a pattern for user name 4 to 15 upper letters only. number & special chars not allowed.
            pattern="[A-Z]{4,15}"


7. Write a pattern for user name starting with uppercase letter and can be 4 to 15 chars.
    [number and special chars not allowed]


            pattern="[A-Z]{1}[a-zA-Z]{3,14}"

8. Write a pattern for user name 4 to 15 chars with atleast one uppercase letter.
    [alpha numeric with underscore allowed]

            pattern="(?=.*[A-Z])\w{4,15}"

9. Write a pattern for user name 4 to 15 chars with atleast one uppercase letter, number and special char.
Form Inputs: Number, Range, Color, URL, Date..
Sudhakar Sharma
•
8:42 AM
Password
- It is similar to textbox but can mask the characters with "*".
- All attributes are similar to textbox.

<input type="password" name=""  id=""  class=""  minlength="" maxlength="" pattern="">

                            Number

- It is used to input only numeric values.
- Attributes
        min
        max
        step

Syntax:
    <input type="number"  name="age"  min="15"  max="35" value="22" step="5">    <input type="number"  name="rate"  min="10.45"  max="18.45" step="0.01">

                            Range
- It is used for number input.
- User can select a range of values using slider.
- All attributes are same like number.

Syntax:
<input type="range"  name="price"  min="100" max="150000"  value="100">

                            Email
- It validates email address.

Syntax:
    <input type="email" placeholder="your email address"  required>


                            URL
- It validates URL format.
- URL format must contain "protocol" and "domain"

Syntax:
    <input type="url"   placeholder="your website address" name="" required>

            www.amazon.in        => invalid
            http://www.amazon.in    => valid
            https://www.youtube.com => valid

                            Color
- It show a color picker.
- User can select a color.
- The color value must be 6 chars hexa decimal only.
        #ff00ff

Syntax:
 <input type="color" name="color"  value="#ff0000">

                        Date and Time
- HTML 5 provides various date and time types.
        - date
        - datetime-local
        - time
        - month
        - year
        - week

Syntax:
<input type="date">
<input type="time">
<input type="datetime-local">
<input type="month">
<input type="year">
<input type="week">

FAQ: How to restrict date selection?
Ans: By using "min" and "max" attributes.

Note: Always the date input format must be "year-month-day"

<input type="date" min="2023-09-20"  max="2023-10-12">

Note: You can't select range of date values using HTML element.

                            File
- It allows the user to select a file so that it can be upload to server using javascript.
- It is just a file browser.

Syntax:
<input type="file">

FAQ: How to restrict the file type in HTML?
Ans : You can't restrict the file type but you can set filter.
          You can set filter by using "accept" attribute.

Syntax:
    <input type="file"  accept=".jpg">
    <input type="file"  accept=".jpg, .png, .gif">

- You can allow user to select multiple file by using "multiple" attribute.

    <input type="file"  multiple>

Summary
- password
- number
- range
- color
- url
- email
- file
- date
Summary
- Texbox
- Password
- Number
- Color
- Email
- Url
- File
- Range
- Date & Time

                            Radio Buttons

- You can display a list of options, and user can select any one or multiple.
- Radio once checked, it can't be unchecked.

Syntax:
    <input type="radio"> <label> Text </label>

- Radio's are always used with "Mutex" mechanism.
  [Mutual Exclusion]

- All radios in a category must have same name. So that they can exhibit Mutex.

Syntax:
    <input type="radio"  name="gender">  <label> Male </label>
    <input type="radio"  name="gender">  <label> Female </label>

- You can make any one radio default selected by using "checked" attribute.

Syntax:
    <input type="radio" name="gender" checked> <label> Male </label>

FAQ: When to use Radio button?
Ans: When selection of any one option is mandatory and without selecting an option if user moves to next, default one option is selected.

- Radios by default submit  "ON" as value.
- You have to define a "name" attribute and "value" for every radio.

Syntax:
 <input type="radio"  name="gender"  value="Male"> <label> Male </label>

                         CheckBox

- Checkbox is similar to radio button.
- Checkbox allows to check or uncheck any option.

Syntax:
 <input type="checkbox" name="course"  value="Java"> <label> Java </label>
 
- You can choose one or multiple.
- In checkbox selection is not mandatory.

Syntax:
 <input type="checkbox"  name="course" value="Java" checked>  <label> Java </label>

FAQ: How to create a checkbox list?
Ans: HTML doesn't provide any checkbox list, you have to design using CSS overflow.

Ex:
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="node_modules/bootstrap-icons/font/bootstrap-icons.css">
    <style>
       ul {
         list-style: none;
         border:1px solid gray;
         width: 150px;
         height: 60px;
         overflow: auto;
       }
    </style>
</head>
<body>
    <form>
        <ul>
            <li><input type="checkbox"> HTML </li>
            <li><input type="checkbox"> CSS </li>
            <li><input type="checkbox"> Bootstrap </li>
            <li><input type="checkbox"> JavaScript </li>
            <li><input type="checkbox"> jQuery </li>
            <li><input type="checkbox"> React </li>
        </ul>
    </form>
</body>
</html>

                            Dropdown List
- It enables the user to select any option from a group of choices.
- HTML dropdown is designed by using

    <select>
    <optgroup>
    <option>

Syntax:
    <select name="product">
     <option> Select Product </option>
     <optgroup label="categoryName">
       <option> Item-1 </option>
       <option> Item-2 </option>
    </optgroup>
    </select>

- Every option comprises 3 attributes

    a) value            It defines the value to submit
    b) selected        It makes option default selected on page load
    c) disabled        It will not allow to select any option

Ex:
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="node_modules/bootstrap-icons/font/bootstrap-icons.css">
    <style>
    </style>
</head>
<body>
    <form>
        <fieldset>
            <legend>Select Product</legend>
            <select name="product">
                <option>Select Product</option>
                <optgroup label="Electronics">
                    <option>Televisions</option>
                    <option disabled>Mobiles</option>
                    <option value="WTH01">Watches</option>
                </optgroup>
                <optgroup label="Fashion">
                    <option selected>Kids</option>
                    <option>Men's</option>
                    <option>Women's</option>
                </optgroup>
            </select>
            <button>Submit</button>
        </fieldset>
    </form>
</body>
</html>

                            List Box
- It is similar to dropdown but allows to select multiple.
- You can convert a dropdown into list box just by using the attributes
    a) size
    b) multiple

Syntax:
    <select size="4" multiple>
    </select>
Form Elements
- Radio Button (Mutex)
- CheckBox
- Dropdown
- ListBox [Size & Multiple]

Note: The options in dropdown or listbox are RC data type. They allow only plain text, number and special chars. You can't add symbols or images into dropdown options.
      HTML will not allow to create nested dropdowns.

                            Textarea
- It is used for multiline text.
- It is RC data type.
- You can use only for plain text.
- It will not allow formats for text.

Syntax:
    <textarea> </textarea>
    <textarea> your text.. </textarea>

Attributes:
- rows        : It defines height in rows.
- cols        : It defines width in columns.
- readonly    : It will not allow to modify text.
- disabled    : It will not allow to modify and submit.

Syntax:
    <textarea  rows="5"  cols="40"> </textarea>

Ex:
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="node_modules/bootstrap-icons/font/bootstrap-icons.css">
    <style>
    </style>
</head>
<body>
    <form>
        <fieldset>
             <legend>Your Comments</legend>
             <textarea cols="40" rows="5"></textarea>
             <br><br>
             <textarea disabled rows="5" cols="40">Terms of Service..</textarea>
             <br><br>
             <input type="checkbox"> <label>I Accept</label>
             <br><br>
             <button>Post Comment</button>
        </fieldset>
    </form>
</body>
</html>

                                    Meter
- It is used to display a grade meter.
- It is controlled dynamically by using "JavaScript".

Syntax:
    <meter> </meter>

Attributes:
    min        : It defines the lowerbound value.
    max        : It defines the upperbound value
    value    : It defines the default value.
    low        : It is a value above min and below high.
    high        : It is a value below max and above low.

Note: If low & high difference is less     => red color
      If low & high difference is more     => yellow
      If low & high are zero            => green

Syntax:
    <meter min="1" max="100" value="100" low="40" high="80"> </meter>

Ex:
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="node_modules/bootstrap-icons/font/bootstrap-icons.css">
    <style>
        ul {
            list-style: none;
        }
        ul span {
            margin-left: 10px;
        }
        li {
            margin-bottom: 10px;
        }
        meter {
            width: 150px;
            border-radius: 100px;
        }
    </style>
</head>
<body>
    <form>
        <fieldset>
             <legend>Ratings & Reviews</legend>
             <ul>
                <li>
                    <span>5</span><span class="bi bi-star-fill"></span>
                    <meter min="1" value="5" max="5"></meter>
                    <span>8,123</span>
                </li>
                <li>
                    <span>4</span><span class="bi bi-star-fill"></span>
                    <meter min="1" max="5" value="3"></meter>
                    <span>5,923</span>
                </li>
                <li>
                    <span>3</span><span class="bi bi-star-fill"></span>
                    <meter min="1" max="5" value="2"></meter>
                    <span>3,123</span>
                </li>
                <li>
                    <span>2</span><span class="bi bi-star-fill"></span>
                    <meter min="1" max="100" low="40" high="80" value="100"></meter>
                    <span>123</span>
                </li>
                <li>
                    <span>1</span><span class="bi bi-star-fill"></span>
                    <meter min="1" max="100" low="60" high="80" value="100"></meter>
                    <span>23</span>
                </li>
             </ul>
        </fieldset>
    </form>
</body>
</html>

                              Progress
- It is used to show the status of any task performed in page, such as downloading, installing, copying, etc..

Syntax:
    <progress> </progress>

Attributes:
    min
    max
    value

Syntax:
    <progress min="1" max="100"  value="30"> </progress>

Ex:
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="node_modules/bootstrap-icons/font/bootstrap-icons.css">
    <style>
        ul {
            list-style: none;
        }
        ul span {
            margin-left: 10px;
        }
        li {
            margin-bottom: 10px;
        }
        meter {
            width: 150px;
            border-radius: 100px;
        }
    </style>
</head>
<body>
    <form>
        <dl>
            <dt>Perparing for Download</dt>
            <dd>
                <progress></progress>
            </dd>
            <dt>40% Completed</dt>
            <dd>
                <progress min="1" max="100" value="40"></progress>
            </dd>
            <dt>Download Complete</dt>
            <dd>
                <progress min="1" max="100" value="100"></progress>
            </dd>
        </dl>
    </form>
</body>
</html>

                            Label
- It is used to display titles and captions for fields in a form.
- It can bind with fields.
- To bind with any field it used "for" attribute.
- Binding is required to manipulate the field dynamically.

Syntax:
    <label for="UserName"> User Name </label>
    <div>
      <input type="text" name="UserName">
    </div>

Ex:
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="node_modules/bootstrap-icons/font/bootstrap-icons.css">
    <style>
        form {
            padding: 20px;
            border:1px solid gray;
            width: 200px;
        }
        .form-group {
            margin-bottom: 20px;
        }
        label {
            font-weight: bold;
        }
        .error-field {
            color:red;
            font-size: 12px;
        }
    </style>
</head>
<body>
    <form>
        <h2><span class="bi bi-person-fill"></span> User Login</h2>
        <div class="form-group">
            <label for="UserName">User Name</label>
            <div>
                <input type="text" name="UserName">
                <div class="error-field">
                    <span>User Name Required</span>
                </div>
            </div>
        </div>
        <div class="form-group">
            <label for="Password">Password</label>
            <div>
                <input type="password" name="Password">
                <div class="error-field">
                    <span>4 to 15 chars</span>
                </div>
            </div>
        </div>
    </form>
</body>
</html>


                            Buttons
- A button is used for confirming user actions.
- HTML provides 2 types of buttons
    a) Generic Buttons
    b) Non-Generic Buttons
- Generic buttons have default functionality
    a) Submit
    b) Reset

    <input type="submit">            HTML 4  [RC Data Type]
    <input type="reset">            HTML 4

    <button type="submit">Text | Image </button>    HTML 5
    <button type="reset"> Text | Image </button>    HTML 5

Ex:
<div class="form-group">
            <input type="submit" value="Register">
            <input type="reset" value="Cancel">
</div>

<div class="form-group">
           <button type="submit"> <span class="bi bi-person-fill"></span> Register </button>
           <button type="reset"> <img src="public/images/bullet.jpg"> Cancel </button>
</div>

- Non Generic button are static without any default functionality.
       
    <input type="button" value="print">        HTML 4
    <button type="button"> Text | Img </button>    HTML 5

                    Bootstrap Form Classes
Bootstrap Classes for Forms
                        [ bootstrap 5x ]

1. Install Bootstrap

    >npm install bootstrap --save

2. Link Bootstrap css to your page

<link rel="stylesheet"  href="node_modules/bootstrap/dist/css/bootstrap.css">
<link rel="stylesheet"  href="node_modules/bootstrap-icons/font/bootstrap-icons.css">


1. Bootstrap Container Classes

    .container            : small screen [smartwatch]
    .container-sm            : mobiles
    .container-md            : tab
    .container-lg            : pc
    .container-xl            : laptop
    .container-xxl            : laptop wide screen
    .container-fluid        : responsive

    <body class="container-fluid">
    </body>

2. Margins

    .m-{size}            margin all directions
    .ms-{size}        left margin [s=start]
    .me-{size}        right margin [e=end]
    .mt-{size}            top margin
    .mb-{size}        bottom margin

    size = 1 to 5

    <form  class="mt-5  ms-5">
    <form  class="m-5">

3. Padding

    .p-{size}            all sides    
    .ps-{size}            left
    .pe-{size}            right
    .pt-{size}            top
    .pb-{size}            bottom

    <form class="m-5 p-5">


4. Borders

    .border
    .border-{size} [ 1 to 3 ]
    .border-{contextual}  primary, secondary, danger, success, warning, info, dark..
    .rounded
    .rounded-{size} [1 to 3]
    .rounded-circle
    .rounded-pill [requires more width]

<img  src="public/images/fashion.jpg"  class="border border-3 rounded rounded-circle">
<div class="border border-2 border-primary"> </div>

5. Width and Height

    .w-{size}        25, 50, 100
    .h-{size}        25, 50, 100

    <div  class="w-25">
    <img class="w-100">

6. Background & Text Colors

    bg-{contextual}
    text-{contextual}

    <h2 class="text-danger">
    <form  class="bg-success text-white">

7. Display

    .d-none
    .d-block
    .d-inline
    .d-flex
    .flex-wrap
    .flex-nowrap
    .justify-content-center
    .justify-content-between
    .justify-space-between
    .align-items-center
    .align-items-top
    .align-items-end
    .align-items-start
    .align-items-baseline

Syntax:
    <body  class="d-flex justify-content-center  align-items-center">
        <div>
            your content..
        </div>
    </body>

Ex:
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="node_modules/bootstrap/dist/css/bootstrap.css">
    <style>
        body {
            height: 100vh;
        }
    </style>
</head>
<body class="container-fluid d-flex justify-content-center align-items-center">
   
    <form class=" ms-5 mt-5 border border-3 border-dark p-4 rounded w-25">
        <h3>Register User</h3>
        <dl>
            <dt>User Name</dt>
            <dd><input type="text"></dd>
            <dd class="text-danger">Name Required</dd>
            <dt>Password</dt>
            <dd><input type="password"></dd>
        </dl>
        <button>Register</button>
    </form>

</body>
</html>

Ex:
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="node_modules/bootstrap/dist/css/bootstrap.css">
    <link rel="stylesheet" href="node_modules/bootstrap-icons/font/bootstrap-icons.css">
    <style>
        body {
            height: 100vh;
        }
    </style>
</head>
<body class="container-fluid">
   <header class="bg-danger text-white p-2 m-2 d-flex justify-content-between">
      <div><span class="fw-bold">Shopper.</span></div>
      <div>
        <span class="me-3">Home</span>
        <span class="me-3">Shop</span>
        <span class="me-3">Pages</span>
        <span class="me-3">Blog</span>
        <span class="me-3">Docs</span>
      </div>
      <div>
        <span class="bi bi-search me-3"></span>
        <span class="bi bi-heart me-3"></span>
        <span class="bi bi-cart"></span>
      </div>
   </header>
</body>
</html>

8. Grid Display

    .row
    .col            responsive
    .col-{size}    1 to 12

Syntax:
    <section class="row">
       <nav class="col-2"> </nav>
       <main class="col"> </main>
       <aside class="col-2"> </aside>
    </section>

Ex:
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="node_modules/bootstrap/dist/css/bootstrap.css">
    <link rel="stylesheet" href="node_modules/bootstrap-icons/font/bootstrap-icons.css">
    <style>
        section {
            height: 100vh;
        }
    </style>
</head>
<body class="container-fluid">
    <section class="row border border-primary border-2 p-4 m-2">
        <nav class="border border-dark border-2 m-2 p-2 col-2">Nav</nav>
        <main class="border border-dark border-2 m-2 p-2 col">Main</main>
        <aside class="border border-dark border-2 m-2 p-2 col-2">Aside</aside>
    </section>
</body>
</html>
Bootstrap Forms
Sudhakar Sharma
•
11:28 AM
9. Form Classes

    .form-control            text, number, email, url, date, password, textarea
    .form-range            range
    .form-control-color        color
    .form-control-file        file
    .form-select            dropdown, listbox
    .form-check-input        radio, checkbox
    .form-label            label
    .form-check-label        label for radio & checkbox
    .form-switch            radio & checkbox container

Syntax: switch type for checkbox or radio

   <div class="form-switch">
    <input type="checkbox"  class="form-check-input">
        <label class="form-check-label"> Yes </label>
  </div>

Ex:
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="node_modules/bootstrap/dist/css/bootstrap.css">
    <link rel="stylesheet" href="node_modules/bootstrap-icons/font/bootstrap-icons.css">
    <style>
       
    </style>
</head>
<body class="container-fluid">
    <h2>Register User</h2>
    <dl class="w-25 border border-2 border-primary rounded p-4">
        <dt>User Name</dt>
        <dd><input type="text" class="form-control"></dd>
        <dt>Password</dt>
        <dd><input type="password" class="form-control"></dd>
        <dt>Select City</dt>
        <dd>
            <select class="form-select">
                <option>Choose City</option>
                <option>Delhi</option>
            </select>
        </dd>
        <dt>Price Range</dt>
        <dd>
            <input type="range" class="form-range">
        </dd>
        <dt>Subscribe</dt>
        <dd class="form-switch">
            <input type="checkbox" class="form-check-input"> <label class="form-check-label">Yes</label>
        </dd>
    </dl>
</body>
</html>

10. Button Classes
   
    .btn
    .btn-{contextual}
    .btn-outline-{contextual}
    .btn-sm
    .btn-lg
    .btn-group
    .btn-group-vertical
    .btn-close
    .btn-link
    .btn-toolbar

Syntax:
    <button  class="btn btn-primary"> Text </button>

    btn => It is base class and required for all button styles.

Ex:
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="node_modules/bootstrap/dist/css/bootstrap.css">
    <link rel="stylesheet" href="node_modules/bootstrap-icons/font/bootstrap-icons.css">
    <style>
       
    </style>
</head>
<body class="container-fluid">
   <dl>
    <dt>Toolbar</dt>
    <dd class="d-flex justify-content-between btn-toolbar bg-danger">
        <div class="btn-group">
            <button class="btn btn-danger">Home</button>
            <button class="btn btn-danger">Shop</button>
            <button class="btn btn-danger">Contact</button>
            <button class="btn btn-danger">Blog</button>
        </div>
        <div class="btn-group">
            <button class="bi bi-search btn btn-danger"></button>
            <button class="bi bi-heart btn btn-danger"></button>
            <button class="bi bi-person btn btn-danger"></button>
        </div>
    </dd>
    <dt>Ordinary Button</dt>
    <dd>
        <button>Login</button>
    </dd>
    <dt>Button Base</dt>
    <dd>
        <button class="btn">Login</button>
    </dd>
    <dt>Contextual</dt>
    <dd>
        <button class="btn btn-success">Insert</button>
        <button class="btn btn-warning btn-sm">Update</button>
        <button class="btn btn-danger btn-lg">Delete</button>
    </dd>
    <dt>Outline Contextual</dt>
    <dd>
        <button class="btn btn-outline-success">Insert</button>
        <button class="btn btn-outline-warning">Update</button>
        <button class="btn btn-outline-danger">Delete</button>
    </dd>
    <dt>Special</dt>
    <dd>
        <button class="btn btn-close"></button>
        <button class="btn btn-link">Signout</button>
    </dd>
    <dt>Group</dt>
    <dd class="btn-group-vertical">
        <button class="btn btn-primary bi-facebook"></button>
        <button class="btn btn-info bi-twitter"></button>
        <button class="btn btn-danger bi-instagram"></button>
    </dd>
   </dl>
</body>
</html>


11. Input Group Classes

    .input-group
    .input-group-text

Syntax:
    <div class="input-group">
       <span class="input-group-text"> &#8377; </span>
       <input type="text" class="form-control">
       <span class="input-group-text"> .00 </span>
    </div>

Ex:
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="node_modules/bootstrap/dist/css/bootstrap.css">
    <link rel="stylesheet" href="node_modules/bootstrap-icons/font/bootstrap-icons.css">
    <style>
       
    </style>
</head>
<body class="container-fluid">
   <h4>Amazon Search Bar</h4>
   <div class="w-50 input-group">
      <select class="input-group-text">
        <option>All</option>
        <option>Mobiles</option>
        <option>Watches</option>
      </select>
      <input type="text" placeholder="Search Amazon.in" class="form-control">
      <button class="bi bi-search btn btn-warning"></button>
   </div>
   <h4>Netflix Register</h4>
   <div class="w-50 input-group input-group-lg p-4 bg-dark">
     <input type="email" class="form-control" placeholder="Your email address">
     <button class="btn btn-danger">
        Get Started <span class="bi bi-chevron-right"></span>
     </button>
   </div>
   <h4>Password</h4>
   <div class="w-25 input-group">
      <span class="bi bi-key-fill input-group-text"></span>
      <input type="password" class="form-control">
      <span class="bi bi-check-square input-group-text bg-success text-white"></span>
   </div>
   <h4>Price</h4>
   <div class="w-25 input-group">
      <span class="input-group-text bg-dark text-white">&#8377;</span>
      <input type="text" class="form-control">
      <span class="input-group-text bg-dark text-white">.00</span>
   </div>
</body>
</html>

12. Text Align

    .text-start
    .text-center
    .text-justify
    .text-end

13. Text Formats
    .fw-bold
    .fst-italic
   
Ex:
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="node_modules/bootstrap/dist/css/bootstrap.css">
    <link rel="stylesheet" href="node_modules/bootstrap-icons/font/bootstrap-icons.css">
    <style>
       
    </style>
</head>
<body class="container-fluid">
    <h4>Register User</h4>
    <dl class="row">
        <dt class="col-2">Name</dt>
        <dd class="col-10"><input type="text"></dd>
        <dt class="col-2">Password</dt>
        <dd class="col-10"><input type="password"></dd>
        <dt class="col-2">Age</dt>
        <dd class="col-10"><input type="number"></dd>
        <dt class="col-2">City</dt>
        <dd class="col-10">
            <select>
                <option>Select City</option>
                <option>Delhi</option>
            </select>
        </dd>
    </dl>
</body>
</html>

Ex: EMI Calculator

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="node_modules/bootstrap/dist/css/bootstrap.css">
    <link rel="stylesheet" href="node_modules/bootstrap-icons/font/bootstrap-icons.css">
    <style>
       
    </style>
</head>
<body class="container-fluid bg-secondary">
    <div class="bg-light m-4 p-4 rounded">
        <div class="h4">Personal Loan EMI Calculator</div>
        <div class="row mt-3 mb-3">
            <div class="col">
                Amount you need &#8377; <input type="text" value="50000" size="15">
            </div>
            <div class="col">
                for <input type="text" size="4" value="5"> years
            </div>
            <div class="col">
                Interest rate <input type="text" size="4" value="10.45"> %
            </div>
        </div>
        <div class="row mt-3 mb-3">
            <div class="col">
                <input type="range" class="w-100" min="50000" max="1000000" value="100000">
            </div>
            <div class="col">
                <input type="range" class="w-100" min="1" max="5" value="3">
            </div>
            <div class="col">
                <input type="range" class="w-100" min="10.45" max="16.45" value="11.45">
            </div>
        </div>
        <div class="row mt-3 mb-3">
            <div class="col">
                <span>&#8377; 50,000</span>
                <span class="float-end">&#8377; 10,00,000</span>
            </div>
            <div class="col">
                <span>1</span>
                <span class="float-end">5</span>
            </div>
            <div class="col">
                <span>10.45%</span>
                <span class="float-end">16.45%</span>
            </div>
        </div>
        <div class="row mt-4 mb-3">
            <div class="col">
                <button class="btn btn-primary float-end">Calculate</button>
            </div>
        </div>
    </div>
</body>
</html>

Ex: Amazon Login

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="node_modules/bootstrap/dist/css/bootstrap.css">
    <link rel="stylesheet" href="node_modules/bootstrap-icons/font/bootstrap-icons.css">
    <style>
       a {
        text-decoration: none;
       }
    </style>
</head>
<body class="container-fluid">
    <div>
        <form class="w-25">
            <div class="h3">Signin</div>
            <div class="mb-4">
                <label class="form-label fw-bold">Email or mobile phone number</label>
                <div>
                    <input type="email" class="form-control">
                </div>
            </div>
            <div class="mt-4">
                <button class="btn btn-warning w-100">Continue</button>
            </div>
            <div class="mt-4">
                By continuing, you agree to Amazon's <a href="#"> Conditions </a> of Use and Privacy Notice.
            </div>
            <div class="mt-4">
                <details>
                    <summary><a href="#">Help?</a></summary>
                    <dl class="ms-3 mt-3">
                        <dd><a href="#">Change Password</a></dd>
                        <dd><a href="#">Forgot Password</a></dd>
                    </dl>
                </details>
            </div>
        </form>
    </div>
</body>
</html>
CSS Form Attributes
- CSS provides attributes and classes to handle form appearence and validation.


    :required            It configures effects when field is defined with required.
    :optional            It defines effects when field is not defined with required.
    :valid            It defines effects when all validation attributes are satisfied.
    :invalid            It defines effects when the field validation returns error.
    :read-only        It defines effects for element when field is set with readonly.
    :disabled            It defines effects when element is set with disabled.
    :checked            It defines effects when element is set with checked attribute.
                    [It can be for radio or checkbox]
    :focus            It defines effects when element is in focus.

    ::placeholder        It defines effects for elements placeholder.


Ex: required & optional

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        input:required+span {
            display: inline;
            color:red;
        }
        input:optional+span {
            display: none;
        }
        input:required {
            border:1px solid red;
        }
        input:optional {
            border:1px solid black;
        }
    </style>
</head>
<body>
    <form>
        <dl>
            <dt>User Name</dt>
            <dd><input type="text" required><span>*</span></dd>
            <dt>Password</dt>
            <dd><input type="password" required><span>*</span></dd>
            <dt>Age</dt>
            <dd><input type="number"><span>*</span></dd>
        </dl>
    </form>
</body>
</html>

Ex: Valid & Invalid

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        input:required+span {
            display: inline;
            color:red;
        }
        input:optional+span {
            display: none;
        }
        input:required {
            border:1px solid red;
        }
        input:optional {
            border:1px solid black;
        }
        input:valid {
            border:1px solid black;
        }
        input:valid+span {
            display: none;
        }
        input:valid~div {
            display: none;
        }
        input:invalid~div {
            display: block;
            color:red;
        }
    </style>
</head>
<body>
    <form>
        <dl>
            <dt>User Name</dt>
            <dd>
                <input type="text" required><span>*</span>
                <div>Name Required</div>
            </dd>
            <dt>Password</dt>
            <dd>
                <input type="password" required><span>*</span>
                <div>Password Required</div>
            </dd>
            <dt>Age</dt>
            <dd>
                <input type="number" required><span>*</span>
                <div>Age Required</div>
            </dd>
            <dt>Mobile</dt>
            <dd>
                <input type="text" pattern="\+91\d{10}">
                <div>Invalid Mobile: +91 - 10 digits</div>
            </dd>
        </dl>
    </form>
</body>
</html>

Ex: Readonly & Disabled

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        textarea:disabled {
            cursor: not-allowed;
        }
    </style>
</head>
<body>
    <form>
        <dl>
            <dt>Terms of Service</dt>
            <dd>
                <textarea rows="4" disabled cols="40">Our Terms of Service..</textarea>
            </dd>
        </dl>
    </form>
</body>
</html>


Ex: Checked

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        textarea:disabled {
            cursor: not-allowed;
        }
        .terms:checked+span {
            color:green;
        }
        .terms+span {
            color:red;
        }
        .terms~button {
            display: none;
        }
        .terms:checked~button {
            display: block;
        }
    </style>
</head>
<body>
    <form>
        <dl>
            <dt>Terms of Service</dt>
            <dd>
                <textarea rows="4" disabled cols="40">Our Terms of Service..</textarea>
            </dd>
            <dd>
                <input type="checkbox" class="terms"> <span>I Accept</span>
                <br><br>
                <button>Submit</button>
            </dd>
        </dl>
    </form>
</body>
</html>


Ex: Focus

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="node_modules/bootstrap-icons/font/bootstrap-icons.css">
    <style>
       input+div {
         display: none;
       }
       input:focus+div {
        display: block;
        color:goldenrod;
       }
    </style>
</head>
<body>
    <form>
        <dl>
           <dt>User Name</dt>
           <dd>
              <input type="text">
              <div> <span class="bi bi-info-circle"></span> Name in Block Letters</div>
           </dd>
        </dl>
    </form>
</body>
</html>


Ex:
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="node_modules/bootstrap-icons/font/bootstrap-icons.css">
    <style>
       input{
          border-left: none;
          border-right: none;
          border-top: none;
       }
       input::placeholder {
         color:green;
       }
    </style>
</head>
<body>
    <form>
        <div>
            <input type="text" placeholder="UserName">
        </div>
    </form>
</body>
</html>




			===========	Multimedia and Styles =============

- Multimedia comprises of animations, audio and video content.
- HTML multi media comprises of
    <marquee>
    <video>
    <audio>
    <embed>     Embed any plugin into page, like applets, video, audio etc.

Marquee:
- It can display scrolling and sliding content in page.

Syntax:
    <marquee>
        ...your content...
    </marquee>

Attributes:
1. scrollamount    : It sets marquee scrolling speed from 1 to 100.
2. direction        : It sets marequee scrolling direction left, right, up & down.
3. behavior        : It changes from scrolling to sliding, you can set "alternate".
4. loop            : It defines the number of times to display after page load.
5. width/height        : It defines marquee area.
6. bgcolor        : It sets background color for marquee area.

Syntax:
<marquee  scrollamount="20" direction="right" loop="3"  width="500" bgcolor="yellow">

    ... your content ...

</marquee>

Ex:
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <marquee scrollamount="20" width="300" bgcolor="yellow">
        <img src="public/images/a2.jpg" width="50" height="50"> Big Billion Sale <img src="public/images/a1.jpg" width="50" height="50"> starts on Amazon and Flipkart from 8-Oct-2023 <img src="public/images/a3.jpg" width="50" height="50">
    </marquee>
    <marquee scrollamount="20" width="300" direction="right" bgcolor="lime">
        <img src="public/images/a2.jpg" width="50" height="50"> Big Billion Sale <img src="public/images/a1.jpg" width="50" height="50"> starts on Amazon and Flipkart from 8-Oct-2023 <img src="public/images/a3.jpg" width="50" height="50">
    </marquee>
</body>
</html>

Video & Audio:
- HTML allows to embed video files into page, which can be the type
        .mp4, .avi, .mkv, .mov, .ogg  etc..
- HTML allows to embed audio files of type
        .mp3, .wav, .midi etc..
- HTM elements

        <video>
        <audio>

Syntax:
    <video  src="path"  poster="thumbnail.jpg"  controls> </video>
    <audio  src="path"  poster="pic.jpg" controls> </audio>


                            Styles
- Styles are attributes defined for HTML elements to make them more interactive and responsive.
- Styles are defined in a webpage using 3 techniques

    1. Inline Style
    2. Embedded Style
    3. External Style Sheet

Inline Styles:
- The style attributes are defined for every element individually by using "style" attribute.
- These styles are faster in rendering.
- However you can't reuse the styles.


Syntax:
    <h2 style="attribute:value; attribute:value">  Text </h2>
   
Ex:
    <h2 style="background-color:red; color:white">  Text </h2>

Embedded Style:
- Styles are defined in page by using <style> container.
- You can reuse the styles with in page.
- It is slower when compared to inline.
- You can't access styles from another page.

Syntax:
   <style>
    selector {
        attribute: value;
        attribute: value;
    }
   </style>

FAQ's:
1. Where to embed the style container?
A. You can embed <style> container in <head> or <body>.




=============CSS Embed and External Files===================


1. Inline            "style"
2. Embedded        <style>

FAQ: Where to embed?
Ans:  <head> & <body>

FAQ: What is the MIME type for Styles?
Ans:  MIME is "Multi purpose Internet Mail Extention".
         MIME defines file & content type.
     Styles MIME type is "text/css".

Syntax:
    <style  type="text/css">

    </style>

FAQ: What is Media type for styles?
Ans:  It configures your styles for various devices and viewports.
     You can set styles for screen, print and speech.
     
Syntax:
    <style  type="text/css"  media="all | screen | print | speech">

    </style>

FAQ: What is the issue with embedded technique?
Ans:
 - It is slower when compared to inline.
 - You can't access across pages.
 - Styles can be used only with in the page.

3. Styles in External File
- You can write styles in a separate style sheet.
- Style sheet have extention ".css"
- Style sheet can Cascade over HTML page.
   [Cascade Style Sheet]
- You can access across pages.
- However if you are using external files, then number of requests will increase for page, which will increase the page load time.

Syntax:
1. Go to "src" folder and add sub-folder  "styles"

2. Add a new file
        "ticket.css"
     .... your css.. style...

3. Link to web page

    <link rel="stylesheet"  href="src/styles/ticket.css">


Ex:
 ticket.css

.container {
    padding: 20px;
    background-color: lightyellow;
    border:3px solid black;
}
dl {
    display: grid;
    grid-template-columns: 6fr 6fr;
}
dt{
    font-weight: bold;
}

 home.html

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="src/styles/ticket.css">
</head>
<body>
    <div class="container">
        <img src="public/images/a1.jpg" width="100" height="100">
        <h1>Ticket</h1>
        <dl>
            <dt>Departure Date</dt>
            <dd>30-Sep-2023</dd>
            <dt>Time</dt>
            <dd>12:45 PM</dd>
        </dl>
        <button>Print Ticket</button>
    </div>
</body>
</html>

FAQ: What is Minification?
Ans:  It is a coding technique followed by developers to compress the CSS file and
     reduce the size.
   
Ex:
1. Copy your actual CSS code

2. Visit the website

    https://www.toptal.com/developers/cssminifier

3. Paste your actual CSS code

4. Click Minify button

5. Now copy the minified code

6. Go to your project  "src/styles" folder

7. Add a new file  "ticket.min.css" and paste the minified code.

8. Link the minified file to your page.

Note: Always use Uncompressed files for "Development" [Design]
      and Minified [Compressed] files for  "Production" [Go Live]

    <link rel="stylesheet" href="src/styles/ticket.min.css">

FAQ: What is CDN?
Ans:  Content Delivery Network
     You can keep all your files in separate respository server and access remotely      
     from any project.



		================  CSS Selectors & Rules  ========================

CSS Rules - FAQ's

1. If styles are defined for any element using inline, embedded and external techniques, which set of effects will apply?
A. If different attributes are defined then all will apply.
     If same attributes are defined then it uses priority
        1st    Inline
        2nd    Embedded
        3rd    External File
 
2. If style container is defined with same attribute in both head & body, then which set of effects will apply?
A. Priority is defined for the <style> in body.

3. If style container is defined with same attribute multiple times in body, then which set will apply?
A. The latest container effects will apply.


                      Selecting HTML elements
                      -----------------------------------
- Styles are defined using inline technique, where selecting element is not required.
- If styles are defined embedded or in external file, then you need a selector to select HTML elements.

Syntax:
        selector
        {
          attribute1: value;            => CSSOM [CSS Object Model]
          attribute2: value;
        }

        {
         key:value;                => Object
        }

- CSS Selectors are classified into various groups

    1. Primary Selectors
    2. Rational Selectors
    3. Dynamic Pseudo classes
    4. Structural Pseudo Classes
    5. Element State Pseudo Classes
    6. Validation State Pseudo Classes
    7. Attribute Selectors
    8. Universal Selector
    9. Root Selector
    10. Behavioural Selector

Primary Selectors:

1. Type Selector

 - It refers to element token name.
    p, h1, h4, table, td, dd, img..
 - It will apply effects to every occurance of element in page.
 - You can't ignore effects for any specific occurance.

Syntax:
      h1 {
         color:red;
      }

2. ID Selector

- It is defined by using "#" and reference name.
- It is assigned to any element by using "id" attribute.
- You apply only to specific element.
- Every element can have only one ID reference.
- Hence multiple sets of styles can't be applied to one element.

Syntax:
    #text-style {
        color:red;
        text-align:center;
    }

    <h1  id="text-style">  HTML </h1>

3. Class Selector

- It is defined by using "." and reference name.
- You can access and apply to any element using "class" attribute.
- Every element can implement multiple classes.
- All class names a separated with "blank space".

Syntax:
    .text-style {
        color:red;
    }
    .border-style{
        border:1px solid red;
    }

    <h1 class="text-style  border-style">  HTML </h1>

Ex:
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        .border-style {
            border: 2px solid red;
            padding: 5px;
        }
        .text-style {
            text-align: center;
            color:red;
            font-family: Arial;
        }
        .bg-style {
            background-color: yellow;
        }
    </style>
</head>
<body>
    <h1 class="text-style border-style bg-style" >Web Technologies</h1>
</body>
</html>

CSS Rules FAQ's:

1. If we define styles for any element using all 3 primary selectors, which one will apply?
A. If different styles are defined then all will apply.
    If same styles are defined then it uses priority:

        1st         Id selector
        2nd        class selector
        3rd         type selector

2. If same attributes are defined using  ID selector in embedded and external file, which set will apply?
A.  Embedded


Note: You can group the selectors using "," delimeter. You can group any type of
      selector for same set of effects.

Syntax:
        p, h1, img {
           border:1px solid red;
        }

        img, .container {
          box-shadow: 2px 2px 2px black;
        }

        #head, .container, p {
          font-family : Arial;
        }

Ex:
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        #head, p {
            font-family: Brush Script MT;
        }
    </style>
</head>
<body>
    <h1 id="head">Web Technologies</h1>
    <p>We build applications for web.</p>
    <h1>HTML</h1>
    <p>It is a markup language.</p>
</body>
</html>

Rational Selectors:
- You can select element using parent and child hierarchy.
- You can also select by refering to siblings.

        parent   child            =>  all child elements in specific parent.

        parent > child            =>  only direct child elements in specific parent.

        ElementA+ElementB    =>  Adjacent selector [Sibling]
       
        ElementA~ElementB    =>  General Sibling


Ex:
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        .container > p {
            color:red;
        }
    </style>
</head>
<body>
     <div class="container">
        <p>Para-1</p>
        <p>Para-2</p>
        <span><p>Para-3</p></span>
        <p>Para-4</p>
     </div>
     <p>Para Outside Container</p>
</body>
</html>


Ex:
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
       h2~p {
         color:red;
       }
    </style>
</head>
<body>
        <h2>Welcome</h2>
        <p>Para-1</p>
        <p>Para-2</p>
        <p>Para-3</p>
        <p>Para-4</p>
 

</body>
</html>
