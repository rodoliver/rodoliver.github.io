[Back to Portfolio](./)

Website Design Final Project
===============

-   **Class:** *CSCI 226 Internet Programming* 
-   **Grade:** *A* 
-   **Language(s):** *HTML & CSS* 


## Project description

This project was to build a litely functional webite which showcases student abilities to create a finish UI that incorpoated HTML, CSS, and some JavaScript in the design. The is comprised of several of the assignments and task created over the course of the semester. 

## How to run the program

How to run the project.

```bash
To view the site got to: http://rodoliver.atwebpages.com/finalproject/ROWebDesigns.htm

<!DOCTYPE html>
<html lang="en-us">
<head>
    
<script src="modernizr-2.js"></script>
<title>R.O. Web Gallery</title>    
    <!--
           Author: Roderick Oliver
           Assignment: Final Exam Project
    Problem 
           Date: 11/21/2016
       -->
   <meta charset="utf-8" />
    <style>
  

    #container {
        max-width: 95%;
        min-width: 60%;
        margin: 0 auto;
        padding:0;
        border: 4px solid black;
        border-radius: 22px;
     }
 
    header {
            padding-top: 1em;
            background-image: url(images/paisley.png);
            border-radius: 10px;
        }

    
    h1.headfontstyleh1 {
         margin: 0 auto;
         padding: 0;
         font-size: 65px;
         font-family: Copperplate / Copperplate Gothic Light, sans-serif;
         color: #356094;
         text-shadow: 0 1px 0 #999999, 0 2px 0 #888888,
             0 3px 0 #777777, 0 4px 0 #666666,
             0 5px 0 #555555, 0 6px 0 #444444,
             0 7px 0 #333333, 0 8px 7px rgba(0, 0, 0, 0.4),
             0 9px 10px rgba(0, 0, 0, 0.2);      
    }
       
    h5.headfontstylesp {
        margin: 0 auto;
        padding: 0 0 2em 10em;
        font-size: 18px;       
        font-style: oblique;
        color: #191970;
        text-shadow: 0 0 5px #356094, 0 0 5px #0094ff,
             0 0 10px #A5F1FF, 0 0 15px #A5F1FF,
             0 0 20px #A5F1FF;
       }   

    header p {
        margin: 0 auto;
        padding-bottom: 2em;
        font-weight: bold;
    }   
    
    img {
        vertical-align: top;
    }

    img.header {
            margin: 0 5em 0 1em;
            box-shadow: 6px 6px 5px 0 #888888;
            border-radius: 15px;
            float: left;
        }

    span.thumbnail {
         float:right;
         margin: 5px;
         padding-top: 10px;
        }      

    body {
        background-attachment: fixed;
        background-image: url(images/dark_wood.png);
        }

 
    #sec1 {
        padding: 0 12px 0 12px;
    }

    #sec3 {
         padding: 0 12px 0 12px;
    }

    nav ul {
                text-align: center;
    }

    nav li {
            padding-right: 12px;
        }

    nav ul li  {
            display: inline;
            text-align: center;
        }

    a {
        height: 50px;
        line-height: 50px; 
    }

    .button-link {
            padding: 10px 15px;
            background: #4479BA;
            color: white;
            text-decoration: none;
            -webkit-border-radius: 4px;
            -moz-border-radius: 4px;
            border-radius: 4px;
            border: solid 1px #20538D;
            text-shadow: 0 -1px 0 rgba(0, 0, 0, 0.4);
            -webkit-box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.4), 0 1px 1px rgba(0, 0, 0, 0.2);
            -moz-box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.4), 0 1px 1px rgba(0, 0, 0, 0.2);
            box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.4), 0 1px 1px rgba(0, 0, 0, 0.2);
            -webkit-transition-duration: 0.2s;
            -moz-transition-duration: 0.2s;
            transition-duration: 0.2s;
    }
      
    .button-link:hover, .button-link:focus {
            background: #356094;
            border: solid 1px #2A4E77;
            text-decoration: none;
    }

    .button-link:active {
            -webkit-box-shadow: inset 0 1px 4px rgba(0, 0, 0, 0.6);
            -moz-box-shadow: inset 0 1px 4px rgba(0, 0, 0, 0.6);
            box-shadow: inset 0 1px 4px rgba(0, 0, 0, 0.6);
            background: #2E5481;
            border: solid 1px #203E5F;
    }

    ul.star {
            list-style-image: url(images/star4.jpg);
            font-size: 1em;
            font-family: Bodoni MT,Didot,Didot LT STD,Hoefler Text,Garamond,Times New Roman,serif;            
            color: navy;
            line-height: 2em;
            
    }
    
    .col1 {
            margin: 0 4em 0 1.5em;
            padding: 0 5px 160px 5px;
            width: 25%;    
            border: solid 2px black;       
            background-image: url(images/paisley.png);
            border-radius: 15px;
            float: left;
    }

    .col2 {
            padding: 0 20px 220px 20px;
            width: 28%;
            border: solid 2px black; 
            background-image: url(images/paisley.png);
            border-radius: 15px;
            float: left;
    }

    .col3 {
            margin: 0 1em 0 4em;
            padding: 0 20px 0 30px;
            width:25%;
            border: solid 2px black; 
            background-image: url(images/paisley.png);
            border-radius: 15px;
            float: left;
    }

    em {
        font-size: 20px;
        color: navy;
    }

    fieldset {
            margin-right: 10px;
            padding-top: 0;
            border: solid 2px black;
            background-color: #99ccff;
            -webkit-border-radius: 4px;
            -moz-border-radius: 4px;
            border-radius: 4px;
            border: solid 1px #20538D;
            -webkit-box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.4), 0 1px 1px rgba(0, 0, 0, 0.2);
            -moz-box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.4), 0 1px 1px rgba(0, 0, 0, 0.2);
            box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.4), 0 1px 1px rgba(0, 0, 0, 0.2);
            -webkit-transition-duration: 0.2s;
            -moz-transition-duration: 0.2s;
            transition-duration: 0.2s;
    }

    legend {
            color:black;
    }

    .labelfloatleft label {
            width: 100px;
            margin-right: 15px;
            color: black;
            float: left;
            text-align: right;
    }
    .labelfloatleft input {
            display: block;
    }

       #shadow1, #shadowbutton1 {
           margin-left: 30px;
            box-shadow: 6px 6px 5px 0 #888888;      
    }

      #shadow2, #shadowbutton2 {
            margin-left: 30px;
            box-shadow: 6px 6px 5px 0 #888888;      
    }


    footer {
            max-width: 35%;
            margin: 0 auto;
            padding: 0.5em 0;
            background-image: url(images/paisley.png);
            border-top: solid 2px black;
            border-radius: 22px;
            clear: both;
            font-weight: bold;
            text-align: center;
    }
    </style>
</head>
<body>    
    <div id="container">
        <header>
            <img class="header" src="images/me_small.jpg" alt="Portfolio Image" title="R.Oliver" />
            <h1 class="headfontstyleh1 ">R.O. Web Designs</h1> 
            <h5 class="headfontstylesp">Where we make all your dreams a reality!</h5>         
                <p>
                    Roderick Oliver - <em>Lead Web Developer</em><br />
                    Address: 300 Terilyn Court Greenville, SC<br />
                    Contact: (205) 864-329-2355
                </p>        
        </header>
    </div>
        <nav>
            <ul>
                <li><a class="button-link" href="brick/bricksolution.htm" title="Brick Solution">Welcome</a></li>
                <li><a class="button-link" href="barker/barker.htm" title="Barker Bread">Barker Bread</a></li>
                <li><a class="button-link" href="contact/gild.htm" title="Gild Shipping">Shipping and Receiving</a></li>
                <li><a class="button-link" href="power/power.htm" title="Sierra Desert">Energy</a></li>
                <li><a class="button-link" href="books/books.htm" title="Woodpendium Books">Books</a></li>
                <li><a class="button-link" href="ziller/ziller.htm" title="Ziller Financial">Finance</a></li>
                <li><a class="button-link" href="lana/lana.htm" title="Lana Bowling Lanes">Recreation</a></li>
                <li><a class="button-link" href="body/body.htm" title="Body By You">Fitness</a></li>
                <li><a class="button-link" href="award/awardballot.htm" title="WKZ Hollywood">Entertainment</a></li>
            </ul>
        </nav>
   
    <div>
      
        <section class="col1" id="sec1">
            <h2>About R.O. Web Designs</h2>
            <p>
                Though R.O. Web Designs is not a real company, this Web page was created for a class project as a skill assessment. The site provided
                was created to consist of all skills learned throughout the course, and is to contain functioning links, thumbnails, and other features in a three column liquid layout.
                So, with that being said; here at R.O. Web Designs we provide our customers with the highest quality in professional web designs. 
                Included in our promise to offer a product that is second to none, we supply our customers with the optoion 
                to choose from several different services and maintenance packages. Our customers can trust that we will develop cutting edge, responsive sites, that are guaranteed to increase their 
                SEO (Seach Engine Optimization) and yield an increase in visits to their sites. Below is a list of some of the previous
                business models we've had the pleasure to work with in the past.             
            </p>

            <ul class="star">
                <li>Shipping and Receiving</li>
                <li>Recreation and Entertainment</li>
                <li>Fitness and Health</li>
                <li>Energy</li>
                <li>And much more...</li>
            </ul><br />            
            </section>
        </div>

    <div>
        <section class="col2">
            <h2>Our Work Speaks for Itself</h2>
            <p>
                Among many of the sites and pages we have designed for our customers, we feel that it is important to let potential customers
                judge for themselves. Though many Web designers showcase their services by providing simple design examples, we take it a step further and give the
                customers the ability to perform live interactions right here in our portfolio site. Customers are able to interact with our site
                by using many of the buttons, links, thumbnails,<span class="thumbnail"><a href="art/art3col.htm" title="Ink Wash Art Gallery"><img src="art/images/bamboo_small.jpg" alt="Ink Wash Art Gallery" /></a></span><br />
                and other features. We encourage you to began navigating the site by starting with clicking the thumb nail to the right; or just by clicking any of the button links
                above. There you will find sites we've created for other customers with a diversity of formats. Here at R.O. Web Designs we truly believe that we can be the Web developers you are looking for,
                and hope that you will consider us for your web site needs.
            </p>
        </section>
   </div>

    <div id="wrapper">
        <section class="col3" id="sec3">
            <h2>If You're Interested in Our Services</h2>
            <p>
                Hopefully you have navigated our site and have discovered that we are the developers of your choice. If you have not looked around our site, we encourage you to
                to do so at this time. But, if you have, and you are interested in setting up a meeting with us and just need more information, please submit your contact information in the form below
                and one of our representives will reach out to you on the next following business day. Once again, thank you for visiting our site and for considering our services. We hope to be doing business with you soon. And remember,
                R.O. Web Designs is,<em>"Where we make all your dreams a reality!"</em>
            </p>

            <div>
                <!-- enter the form code below -->
                <form id="survey" name="survey" method="post" action="javascript:submitform();">
                    <fieldset id="shadow1" class="labelfloatleft">
                        <legend>Contact Information</legend>
                        <label for="firstname">First Name</label>
                        <input class="text" type="text" name="firstname" id="firstname" placeholder="first name" />

                        <label for="lastname">Last Name</label>
                        <input class="text" type="text" name="lastname" id="lastname" placeholder="last name" />

                        <label for="emailaddress">Email Address</label>
                        <input class="text" type="email" name="emailaddress" id="emailaddress" placeholder="name@anywhere.com" />
                    </fieldset><br />

                    <fieldset id="shadow2">
                        <legend>I am interested: (check option below)</legend>
                        <fieldset>
                            <input type="checkbox" name="interested" id="information" value="websites" />
                            <label for="information">I'd like to receive additional information about upcoming events and seminars and would like to schedule an appointment.</label>
                        </fieldset>
                    </fieldset><br />

                    <input id="shadowbutton1" type="submit" value="Send Information" class="button-link" />
                    <input id="shadowbutton2" type="reset" value="Reset" class="button-link" />
                </form>

            </div><br /> <!-- end formcontainer -->
        </section> <!--end main setion -->
   </div>
    <div>
        <footer>
            <p>
                Greenville Technical Community College<br />
                Date Created: November 23, 2016 <br />&bull; Course Number: IST-226 Internet Programming<br />

            </p>
        </footer>
    </div>
</body>
</html>

```

The application doesn't need compiliing but can be run by going tothe webpages link above. To be able to recreate the assignment you would need to go to https://webfreehosting.net/login.php to create an account for a free domain. Fron the domain you will be able to add all the file to the domain to be able display them online. This process is similar to adding the application on a webserver. For instructions please feel free to contact me.

## UI Design

The application is just a simple desgin that allow the user to view basic function on how a website works. This site allows for the user to use buttons, checkboxes, clickable thumbnails, and radio buttons to understand how the website respond to user interaction.

Website landing page on load (see Fig 1), displays the user interface with interactive links for the user to be able to navigate the site, and see how the clickable items and links respond. The Recreation pages just to display code style and design, as well as to showcase the use of a different nav bars style (see Fig 2).The Entertainment page showcases the use of a radio button style form that allows a user to make a selection for movie tickets with the ability to reset the form for the user (see Fig 3). The Fitness site showcases the use of tables and rows within a website. The site also showcases the styling that is used for alternating colors on rows (see Fig 4).

![screenshot](images/RO_WebDesign.png)

Fig 1. The Landing Page

![screenshot](images/RO_WebDesign2.png)

Fig 2. Site load after clicking the Recreation button on the nav bar.

![screenshot](images/RO_WebDesign3.png)

Fig 3. Site load after clicking the Entertainment button on the nav bar.

![screenshot](images/RO_WebDesign4.png)

Fig 4. Site load after clicking the Fitness button on the nav bar.

## 3. Additional Considerations

As a result of what I have learned over the years, I have continued to work towards building my skillset through continual development and training by learning applications such as *Power Query & Power BI, MySQL, etc.*). Below is an example of a example site I started working on in 2017 for an automotive maintenance site based on a class project using PHP. The page is only the login page and the code for the vehicle logs can be shared if requested.


For more details see [Personal Project UI](personal_project).

[Back to Portfolio](./)
