# Web Page for Mathematical Calculations

## AIM:

To design a static website with validation to perform mathematical calculations in client side.

## DESIGN STEPS:

### Step 1:

Requirement collection.

### Step 2:

Creating the layout using HTML and CSS.

### Step 3:

Write javascript to perform the calculations.

### Step 4:

Include regularexpression based input validation.

### Step 5:

Validate the layout in various browsers.

### Step 6:

Validate the HTML code.

### Step 6:

Publish the website in the given URL.

## PROGRAM :
~~~
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Math Website</title>
    <style>
        *{
            box-sizing: border-box;
            font-family: Arial, Helvetica, sans-serif;
        }
        body{
            background-color: black;
            color:black;
        }
        .container{
            width: 1080px;
            margin-left: auto;
            margin-right: auto;
            background-color: black;
            border:#540688;
        }
        .content{
            display: block;
            width: 100%;
            background-color:purple;
            margin-top: 40px;
            min-height: 400px;
        }
        .text{
            text-align: center;
            padding-top: 50px;
            text-decoration: underline;
        }
        .formelement{
            text-align: center;
            font-family: Georgia, 'Times New Roman', Times, serif;
            font-size: 25px;
            margin-top: 5px;
            margin-bottom: 5px;

        }
        .content2{
            display: block;
            width: 100%;
            background-color:red;
            margin-top: px;
            min-height: 400px;
        }
        .by{
            text-align: center;
            color: rgb(245, 240, 240);
        }
    </style>

</head>


<body>
    <div class="container">
        <div class="content">
            <h1 class="text"><B>Area of Rectangle:</B></h1>
            <form>
                <div class="formelement"><label for="aEdit">Length:</label>
                    <input type="number" id="aEdit" value="0"/>
                    <lable for="aedit">Meters</lable>
                </div><br>
                
                <div class="formelement">
                    <label for="bEdit">Breadth:</label>
                    <input type="number" id="bEdit" value="0"/>
                    <lable for="aedit">Meters</lable>
                </div>
                <div class="formelement">
                    <input type="button" value="Calculate" id="AddButton"/>
                </div>
                
                <div class="formelement">
                    <label for="cEdit">Area:</label>
                    <input type="text" id="cEdit" value="0" readonly />
                    <lable for="aedit">Meter<sup>2</sup></lable>
                </div><br>
                <div class=formelement>
                    Formula : Area = Length*Breadth
                </div>
            </form>

        </div>
        <div class="content2">
            <h1 class="text">Volume of the Cylinder</h1>
            <form>
                <div class="formelement"><label for="hEdit">Radius:</label>
                    <input type="number" id="hEdit" value="0"/>
                    <lable for="aedit">Meters</lable>
                </div><br>
                
                <div class="formelement">
                    <label for="rEdit">Height:</label>
                    <input type="number" id="rEdit" value="0"/>
                    <lable for="aedit">Meters</lable>
                </div>
                <div class="formelement">
                    <input type="button" value="Calculate" id="AddButton1"/>
                </div>
                
                <div class="formelement">
                    <label for="vEdit">Volume:</label>
                    <input type="number" id="vEdit" value="0" readonly />
                    <lable for="aedit">Meter<sup>3</sup></lable>
                </div><br>
                <div class="formelement">
                    Formula : Volume=π*Radius<sup>2</sup>*Height
                    </div><br>
                   
            </form>

        </div>
    </div>
    <script>
        function validate(){
            var user1=document.getElementById("aedit").value;
            var user2=document.getElementById("bedit").value;
            var user3=document.getElementById("redit").value;
            var user4=document.getElementById("hedit").value;
            var re = /^[0-9]+$/;
            if (re.test(user1)){
                return true;
      }
            else if (re.test(user2)){
                return true;
         }
         else if (re.test(user3)){
                return true;
         }
         else if (re.test(user4)){
                return true;
         }
            else {
                alert('Please input numeric characters only');
                return false;
        }
       
        }
    </script>
    <script type="text/javascript">
        var button,button1;
        button = document.querySelector("#AddButton");
        
        button.addEventListener("click",function(){
            var aText,bText,cText;
            var aVal,bVal,cVal;
            aText=document.querySelector("#aEdit");
            bText=document.querySelector("#bEdit");
            cText=document.querySelector("#cEdit");

            aVal = parseInt(aText.value);
            bVal = parseInt(bText.value);
            cVal = aVal*bVal;
            cText.value = ""+cVal;
        });
        button1 = document.querySelector("#AddButton1");
        button1.addEventListener("click",function(){
            var aText,bText,cText;
            var aVal,bVal,cVal;
            hText=document.querySelector("#hEdit");
            rText=document.querySelector("#rEdit");
            vText=document.querySelector("#vEdit");

            hVal = parseInt(hText.value);
            rVal = parseInt(rText.value);
            vVal = (22/7*rVal*rVal)*(hVal);
            vText.value = ""+vVal;
        });

    </script>
    <footer> <p class="by"><B>Developed by :A.KATHIRVEL</B></p></footer>
</body>
</html>
~~~
## OUTPUT:
![output](mathweb.png)
## Result:

Thus a website is designed to perform mathematical calculations in the client side.
