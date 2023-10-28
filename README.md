# note-taking-app
#index file
!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="./style.css">
    <title>to do list</title>
</head>
<body>
    <div class="container"> 

    <div class="todo-app">
        <h2>To-Do List <img src="img/pencil.jpeg" alt=""></h2>
        <div class="row">
            <input type="text" id="input-box" placeholder="Add Your text">
            <button onclick="addTask()">Add</button>
        </div>
        <ul id="list-container">
           <!-- <li class="checked"></li>
             <li>Task 2</li>
            <li>Task 3</li>  --> 
        </ul>
       </div>
  </div>
<script src="script.js"></script>
</body>
</html>

CSS
* {
    margin: 0;
    padding: 0;
    font-family: 'Poppins', 'sans-serif';
    box-sizing: border-box;
}
.container {
    width: 100%;
    min-height: 100vh;
    background: linear-gradient(135deg, #153677, #4e085f);
    padding: 10px;

}

.todo-app {
    width: 100%;
    max-width: 540px;
    background: #fff;
    margin: 100px auto 20px;
    padding: 40px 30px 70px;
    border-radius: 10px;
}

.todo-app h2 {
    color: #002765;
    display: flex;
    align-items: center;
    margin-bottom: 20px;
}
.todo-app h2 img{
    width: 30px;
    margin-left: 10px;

}
.row{
    display: flex;
    align-items: center;
    justify-content: space-between;
    background: #edeef0;
    border-radius: 30px;
    padding-left: 20px;
    margin-bottom: 25px;
}
input{
    flex: 1;
    border: none;
    outline: none;
    background: transparent;
    padding: 10px;
    font-weight: 14px;
}
button{
    border: none;
    outline: none;
    padding: 16px 50px;
    background: #ff5945;
    color: #fff;
    font-size: 16px;
    cursor: pointer;
    border-radius: 40px;
}
ul li{
    list-style: none;
    font-size: 17px;
    padding: 12px 8px 12px 50px;
    user-select: none;
    cursor: pointer;
    position: relative;
}
ul li::before{
    content: '';
    position: absolute;
    height: 28px;
    width: 28px;
    border-radius: 50%;
    background-image: url(img/circle.jpeg);
    background-size: cover;
    background-position: center;
    top: 12px;
    left: 8px;
}
ul li.checked{
    color: #555;
     text-decoration: line-through;/*  letters ko bich me se cut krne k liye  */
     
}
ul li.checked::before{
    background-image: url(img/checked.jpeg);
}
ul li span{
    position: absolute;
    right: 0;
    top: 5px;
    width: 40px;
    height: 40px;
    font-size: 22px;
    color: #555;
    line-height: 40px;
    text-align:center;

}
ul li span:hover{
    background: #edeef0;
}
