[Back to Portfolio](./)

Online Bookstore Final Project
===============

-   **Class:** *CSCI 275 CPT Senior Project* 
-   **Grade:** *A* 
-   **Language(s):** *HTML, PHP, JavaScript, JQuery, CSS* 
-   **Authors:** *David Slama, Ray Hill, Danial Greer, Roderick Oliver*
-   **Project Leader:** *Roderick Oliver*

## Project description

The purpose of he is project was to create a functionall online bookstore with the capabilities for students to veiw courses and books for upcoming semesters. The site is an interface for for instructors, directors, and department heads, to be able to view, place orders, edit orders, as well approve orders based on role granted to use the site. The site also allows for the bookstore employees to be able to process the books that are ordered through the site. The site also allows for the site admin to add and update user accounts. 

## How to run the program:

Code Design Structure (will to setup on webserver) and to run the project.

```bash
<!DOCTYPE html>
<html lang="en-us">
<head>
</head>
<body></body>
</html>
<meta http-equiv="Content-Type" content="text/html; charset=utf-8">
<title>Bookstore Order System Home</title>
<meta name="viewport" content="device-width, intial-scale=1"/>
<link href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css" rel="stylesheet" /><script src="https://ajax.googleapis.com/ajax/libs/jquery/3.2.1/jquery.min.js"></script><script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/js/bootstrap.min.js"></script>
<link href="main.css" rel="stylesheet" type="text/css" />
<link href="index.css" rel="stylesheet" type="text/css" />
<style type="text/css">body {
        background: url(images/bookstack3.jpg) no-repeat center center fixed;
        -webkit-background-size: cover;
        -moz-background-size: cover;
        -o-background-size: cover;
        background-size: cover;
      }

  /*Float causes the button to stick to the side. Issues with using percentages on header - results in it "sticking" at a certain minimized point.*/
  /*Button set to 1000+px.*/
      #home-login {
        float: right;
      }

      #book-carousel {
        height: 30em;
        background: rgba(189, 206, 173, 0.5);
        margin-bottom: 15px;
        text-align: center;
		min-height: 460px;
      }

      #course-search {
        background-color: white;
        background: rgba(189, 206, 173, 0.5);
      }

      #search-button {
        margin: 1%;
      }

      .carousel-caption {
        position: relative;
        left: auto;
        right: auto;
      }

    #select-div {
        position: absolute;
        left: 50%;
        top: 90%;
        transform: translate(-50%, -50%);
    }

</style>
<header class="container">
<h1 id="bos-logo">Bookstore Order System</h1>

<h2>Powered by R2D2 Technologies</h2>
<a href="login.php" class="btn btn-primary" id="home-login" type="submit">Login</a>
</header>
<!--Begins Carousel for books--><!--!! Carousel is to take a small number of current books from the database and display their images + course code + course title-->

<div class="carousel slide" data-ride="carousel" id="book-carousel"><!--Carousel Indicators-->
<ol class="carousel-indicators">
	<li class="active" data-target="#book-carousel" data-to-slide="0"></li>
	<li data-target="#book-carousel" data-to-slide="1"></li>
	<li data-target="#book-carousel" data-to-slide="2"></li>
	<li data-target="#book-carousel" data-to-slide="3"></li>
</ol>
<!--Carousel Wrapper-->

<div class="carousel-inner">
<div class="item active"><img id="carousel0" width="10%" alt="" class="img-responsive center-block" src="" />
<div class="carousel-caption">
<h4 id="c0-title"></h4>
<p id="c0-course"></p>
<p hidden id="c0"></p>

<p></p>
</div>
</div>

<div class="item"><img id="carousel1" alt="" width="10%" class="img-responsive center-block" src="" />
<div class="carousel-caption">
<h4 id="c1-title"></h4>
<p id="c1-course"></p>
<p hidden id="c1"></p>

<p></p>
</div>
</div>

<div class="item"><img id="carousel2" alt="" width="10%" class="img-responsive center-block" src="" />
<div class="carousel-caption">
<h4 id="c2-title"></h4>
<p id="c2-course"></p>
<p hidden id="c2"></p>

<p></p>
</div>
</div>

<div class="item"><img id="carousel3" alt="" width="10%" class="img-responsive center-block" src="" />
<div class="carousel-caption">
<h4 id="c3-title">Psychology 101</h4>
<p id="c3-course"></p>
<p hidden id="c3"></p>

<p></p>
</div>
</div>
</div>
<!--Carousel L&R Controls--><a class="left carousel-control" data-slide="prev" href="#book-carousel"><span class="sr-only">Previous</span> </a> <a class="right carousel-control" data-slide="next" href="#book-carousel"> <span class="sr-only">Next</span> </a></div>
<div class="text-center" id="course-search">
    <!--Options left in as placeholders -->
    <div id="select-div" class="col-sm-3">
        <select class="form-control col-sm-3" id="viewClass" name="department">
            <option> -Select Department- </option>
        </select>
    </div>
</div>
       
<!-- <footer>
<p>Background images are courtesy of financialplan.byu.edu/buying-textbooks and feelgrafix.com/752369-black-background-images.html</p>
</footer> -->
<script>

       
        $("#viewClass").change(function () {
            if ($(this).val()) window.location = $(this).val();
        });

  
function populateForm() {

//    
// generates a list of available departments in the database
// and then populates the lower drop down list with it.
//
	$.ajax({
        url: 'action.php',
        type: 'POST',
        data: {action:"get_departments"},      
        success: function(result) {
			for(i = 0; i < result.data.length; i++){						
				deptCode  = result.data[i].DeptCode;
				name = result.data[i].Name;
				if (deptCode != 'GTC') {
					newOption = "<option value=\"departments.php?DeptCode=" + deptCode + "&Name=" + name + "\">" + name + "</option>";				
					document.getElementById("viewClass").insertAdjacentHTML('beforeend', newOption);
					}
				}
		}
	});

	//
	// populates the carousel
	//
    $.ajax({
        url: 'action.php',
        type: 'POST',
        data: {action:'search_all_books'},
        success: function(result){
            for (var i = 0; i < 4; i++) {
				repeat = false;
				var rand = (Math.floor(Math.random() * result.data.length));					
				
				//
				// checks for a repeated textbook
				//
				for(var j = i - 1; j >= 0; j--){					
					prevBook = $('#c' + j).html();
					if(prevBook == rand)
					{
						i--;
						repeat = true;
						break;
					}
				}
				
				//
				// adds the textbook to the carousel
				//
				if (repeat == false) {				
					var xThumbnail = result.data[rand].Thumbnail;
					var xTitle = result.data[rand].Title;
					var xClassCode = result.data[rand].ClassCode;
					$('#carousel' + i).attr({src:xThumbnail,width:"220px"});
					$('#c' + i + '-title').text(xTitle).css({color:"black"});
					$('#c'+ i + '-course').text(xClassCode).css({color:"black"});					
					$('#c' + i).text(rand);
				}      
			}
        }
    });
}


$(document).ready(function(){
    populateForm();
});	

</script>
```


## UI Design

The UI provides for a user whether they are the site admin, an instructor, department head, or a bookstore employee, can login and see the neccessary functions needed to process the book orders. The site use model form created using Bootstrap for the design. And API for retrieving book information based on the ISBN number is used for creating the book orders to be submiotted for approval and is stored in the database. As the books go through the process of being ordered, approved, and processed by the bookstore, it sends email notifications to each party registered.

The first screensh displays an admin page after login **(see Fig 1 - 4)**, the model used for the forms, and a list of drop-down options that can used in managing the user's account access and the course they will be responsible for. The next set of screenshot provides the functions administered by an instructor. The instructiors are able to see the book orders they have made and status of those orders, as well as the ability to place additional orders **(see Fig 5 - 8)**. The remainging images provide example of the director and department head's view of the site which grants the abliltiy approve or reject orders placed by instructors before sending it on to the bookstore for processing. And lastly, the books store employees's view allows for the processing of the orders received and for view orders that have already been placed. **(see Fig 9 - 11)**.

![screenshot](images/Bookstore_Instructor's_Admin_Page.png)  
Fig 1. The Admin Page

![screenshot](images/Bookstore_Instructor's_Admin_Edit_User.png)  
Fig 2. Example of User Account editing.

![screenshot](images/Bookstore_Admin_Page-Department_selection.png)  
Fig 3. Example of Editing the user's department.

![screenshot](images/Bookstore_Admin_Page-Role_selection.png)  
Fig 4. Example of Editing the user's role.

![screenshot](images/Bookstore_Instructor's_View_Page.png)  
Fig 5. Example of Instructor's view pending orders.

![screenshot](images/Bookstore_Instructor's_View_Page-2.png)  
Fig 6. Example of Instructor's view of previous orders.

![screenshot](images/Bookstore_Instructor's_View_Page-3.png)  
Fig 7. Example of Instructor's order form for books for course.

![screenshot](images/Bookstore_Instructor's_View_Page-Campus_selection.png)  
Fig 8. Example of Instructor's campus selection drop-down list.

![screenshot](images/Bookstore_DepartmentHead_Order_Approval_Page.png)  
Fig 9. Example of the Department Head's approval portal.

![screenshot](images/Bookstore_Staff_Page.png)  
Fig 10. Example of Bookstore Staff portal.

![screenshot](images/Bookstore_Staff_Page_Update_Orders-2.png)  
Fig 10. Example of Bookstore Staff order processing.

![screenshot](images/Bookstore_Staff_Page_Update_Orders-3.png)  
Fig 11. Example of Bookstore processed orders.

### [User Interface Mockups with Functionality Descriptions](pdf/TeamProjectMockUps.pdf)

## 3. Additional Considerations

During the process of developing this application there werem deliverables that we had to provide. The deliverables inccluding a ***Mission Statement, Project Charter, Functional Specifications, a Testing Plan, a Testing Report, a Finalized System Design, and a User Guide***, which can a be found below

For more details see [Final Project Supporting Documents](additional_resources).

[Back to Portfolio](./)
