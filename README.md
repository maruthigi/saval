<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
  

    <link rel="stylesheet" href="besantech.css">
    <title>Document</title>
    <style>
        #img{
            width: 100%;
            box-shadow: 1px 1px ;
            height: 400px;
        }
    </style>
</head>
<body>
    <div id="container" >
<div id="title">
    <h1 id="akka">👤besantechnology</h1>
    <button id="buter">Sing up</button>
</div>
<div class="form"  id="containerb">
    <form action="">
        <div id="admin">
            <span id="spa">✖</span>
            <h3>Admin Login Area</h3>
            <h6>Please Provide your details </h6>

            <input type="text" name="user1" id="user1" placeholder="please enter your Id number" required>
    <br>
   


    <span><input type="text" name="user2" id="user2" placeholder="please enter your Password" required></span>
    <br>
    <input id="submit" value="Login" onclick="besan()"></input> 
    


        </div>
    </form>

</div>
</div>
<div id="second">

<div class="container2">
    <div class="navbar">
        <div class="title2">Besantechnology</div>
        <div><input type="text" name="search" id="search" placeholder="please search ..."></div>
        <div><h3>👤Admin</h3></div>
    </div>
    <div class="header">
        <div class="child"> <br>
            Dash Board
        </div>
        <div class="child"></i><br>
             Branch</div>
        <div class="child">Employee</div>
        <div class="child">Employee Benfits</div>
        <div class="child">Enquiry Soures</div>
        <div class="child">Enquiry Status</div>
        <div class="child"> <br>
            Customers</div>
        <div class="child">Followups</div>
        <div class="child"> Report</div>
    </div>

</div>
<div class="box">
    <div class="title3"><h4>Importantents ShortCuts</h4></div>
    <div class="card">
        <div class="title4">
     <div class="cards" onclick="gab()" > Employee </div>
        <div class="cards">Customer</div>
        <div class="cards">Employees Roles</div>
        <div class="cards">Followup's</div>
        
    </div>
    </div>

</div>
</div>
<div id="maru">
<div class="navbar">
    <div class="title2">Besantechnology</div>
    <div><input type="text" name="search" id="search" placeholder="please search ..."></div>
    <div><h3>👤Admin</h3></div>

<div id="employees">
<table id="employee" >
    <thead>
        <tr>
            <th>s.no</th>
            <th>Eployee Name</th>
            <th>City Name</th>
            <th>Employee Email</th>
            <th>Employee Mobile</th>
            <th>Address</th>
            <th>Branch</th>
            <th>Role</th>
            <th>Edit</th>
        </tr>
    </thead>
        <tbody>

        </tbody>
        <input type="submit" name="submit1" id="submit1" value="Add Employee" onclick="mama()">

</table>

</div>
</div>
<div id="last">

<div class="container">
    <div class="titles">Edit Employee Details</div>
    <form onsubmit="onFormSubmit()">
        <div class="main">
        <div>
        <label class="label">FullName:</label> 
        <input type="text" id="fullName" name="fullName" required class="input">
        
        </div>
        <div>
        <label>Email:</label>
        <input type="email" id="email" name="email" required class="input">
        </div>
        <div>
        <label>City</label>
        <input type="text" id="city" name="city" required class="input">
        </div>
        <div>
        <label>Mobile No:</label>
        <input type="text" id="mobile" name="mobile" required class="input">
        </div>
        <div>
        
        <label >permanent Address:</label>
        <textarea name="address" id="address" cols="30" rows="5" class="input"></textarea>
         
          
        </div>
        <div>

        <label >adhar:</label>
        <input type="text" name="adhar" id="adhar" required class="input">
        </div>
        <div>
        <label >employee Role:</label>
        <input type="text" name="role" id="role" required class="input">
        </div>
        <div>
        <label >employee branch:</label>
        <input type="text" name="branch" id="branch" required class="input">
        </div>
       
       
        <br><br><br>
        <input type="submit" value="SAVE" id="add" onclick="badra()">
       
    </form>
    </div>
</div>
</div>
      
    


    <script>
        
        function besan(){
            let be=document.getElementById("user1").value
             let bd=document.getElementById("user2").value
             if(be.length<5){
                alert("please enter 6 letters")
             }
             else if(bd.length<6){
                alert("please enter above 7 letters")
             }else{
                alert("sucessfully completed")
                besaw()
             }
             

        }
function besaw(){
    window.location.href="besantechpage2.html"
}
        
        let ban=document.getElementById("add")
        function badra(){
            akkr.style.display="block"
            mam.style.display="none"

        }
        let a=document.getElementById("buter")
        let b=document.getElementById("containerb")
        let c=document.getElementById("spa")
        let d=document.getElementById("mar1")
        let e=document.getElementById("mar2")
        b.style.display="none"

        a.addEventListener("click",change)
        function change(){
            b.style.display="block"
        }
        c.addEventListener("click",cancel)
        function cancel(){
            b.style.display="none"
        }

      
let g=document.getElementById("submit")
let f=document.getElementById("second")
let n=document.getElementById("container")
function akka(){
    f.style.display="block"
    n.style.display="none"
   
}
let s=document.getElementById("maru")
function gab(){
    
    s.style.display="block"
    f.style.display="none"
}

let r=document.getElementById("arya")

function ara(){
    
   
    r.style.display="block"
   
   
}
let mam=document.getElementById("last")
let akkr=document.getElementById("employees")
function mama(){
    mam.style.display="block"
    akkr.style.display="none"
}


var selectedRow=null
function onFormSubmit(){
    event.preventDefault()
    var formData=readFormData()
    if(selectedRow === null){
    insertNewRow(formData)
    }
    else{
        updateForm(formData)
    }
    resetForm()
}

        function readFormData(){
            var formData={}
            formData["fullName"]=document.getElementById("fullName").value
            formData["email"]=document.getElementById("email").value
            formData["city"]=document.getElementById("city").value
            formData["mobile"]=document.getElementById("mobile").value
            formData["address"]=document.getElementById("address").value
            formData["adhar"]=document.getElementById("adhar").value
            formData["role"]=document.getElementById("role").value
            formData["branch"]=document.getElementById("branch").value
            


            return formData
        }

        function insertNewRow(data){
            var table=document.getElementsByTagName("tbody")[0]
            var row=table.insertRow(table.length)

            cell1=row.insertCell(0)
            cell1.innerHTML=data.fullName

            cell2=row.insertCell(1)
            cell2.innerHTML=data.email

            cell3=row.insertCell(2)
            cell3.innerHTML=data.city

            cell4=row.insertCell(3)
            cell4.innerHTML=data.mobile
            cell5=row.insertCell(4)
            cell5.innerHTML=data.address
            cell6=row.insertCell(5)
            cell6.innerHTML=data.adhar
            cell7=row.insertCell(6)
            cell7.innerHTML=data.role
            cell8=row.insertCell(7)
            cell8.innerHTML=data.branch
           
              cell9=row.insertCell(8)
              
     cell9.innerHTML=`<button id="mass" onClick="onEdit(this)">Edit</button>  <br> <button id="mass" onClick="onDelete(this)">Delete</button>`
     
        }

        

        function resetForm(){
            document.getElementById("fullName").value=""
            document.getElementById("email").value=""
            document.getElementById("city").value=""
            document.getElementById("mobile").value=""
            document.getElementById("address").value=""
            document.getElementById("adhar").value=""
            document.getElementById("role").value=""
            document.getElementById("branch").value=""
           
        }

        function onEdit(td){
            selectedRow=td.parentElement.parentElement;
            document.getElementById("fullName").value=selectedRow.cells[0].innerHTML
            document.getElementById("email").value=selectedRow.cells[1].innerHTML
            document.getElementById("city").value=selectedRow.cells[2].innerHTML
            document.getElementById("mobile").value=selectedRow.cells[3].innerHTML
            document.getElementById("address").value=selectedRow.cells[4].innerHTML
            document.getElementById("adhar").value=selectedRow.cells[5].innerHTML
            document.getElementById("role").value=selectedRow.cells[6].innerHTML
            document.getElementById("branch").value=selectedRow.cells[7].innerHTML
            
        }

        function updateForm(data){
            selectedRow.cells[0].innerHTML=data.fullName
            selectedRow.cells[1].innerHTML=data.email
            selectedRow.cells[2].innerHTML=data.city
            selectedRow.cells[3].innerHTML=data.mobile
            selectedRow.cells[4].innerHTML=data.address
            selectedRow.cells[5].innerHTML=data.adhar
            selectedRow.cells[6].innerHTML=data.role
            selectedRow.cells[7].innerHTML=data.branch
           
        }


        function onDelete(td){
            selectedRow=td.parentElement.parentElement;
document.getElementById("employee").deleteRow(selectedRow.rowIndex)
        }





    


    </script>
    
</body>
</html>
    </script>
    
</body>
</html>
