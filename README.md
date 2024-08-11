#HTML CODE

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>css image overlay</title>
    <link rel="stylesheet" href="practice.css">
</head>
<body>
    <h1 class="heading">Image Overlay</h1>
   <div class="main">
       <img src="image.jpg">
       
       <div class="maincontent">
           <h3>Best HP Gaming Laptop</h3>
           <a href="https://www.flipkart.com/hp-victus-intel-core-i5-13th-gen-13420h-16-gb-512-gb-ssd-windows-11-home-6-graphics-nvidia-geforce-rtx-3050-15-fa1327tx-gaming-laptop/p/itmb08f154f265d7?pid=COMHY8KVZ73Y9PPY&lid=LSTCOMHY8KVZ73Y9PPYGBSHGI&marketplace=FLIPKART&q=laptop+gaming&store=4rr%2Ftz1&srno=s_1_7&otracker=search&otracker1=search&fm=Search&iid=b58a2f84-d325-487d-a4fc-0eb5461a05e6.COMHY8KVZ73Y9PPY.SEARCH&ppt=sp&ppn=sp&ssid=oycprlaqio0000001722264687475&qH=6ad778cb0140a100" class="button" target="_blank">Buy now</a>
>
       </div>
   </div>
   
</body>
</html>


#CSS CODE

*,
*::after,
*::before{
    margin:0;
    padding:0;
    box-sizing:border-box;
}
body{
     
    font-family:Cambria, Cochin, Georgia, Times, 'Times New Roman', serif}
.heading{
    text-align:center;
    margin:1rem auto;
}
.main{
    margin:auto;
    max-width:500px;
    position: relative;
}
.main img{
    border:4px solid#225;
    width:100%;
   
}
.button{
    display:inline-block;
    text-decoration: none;
    color:rgb(255, 236, 236);
    background:rgb(119, 112, 112);
    padding:0.5em 1.2em;
    margin-top:1rem;
    transition:all 0.4s ease-in;
}
.button:hover{
    background:rgb(65, 62, 62);
}
.maincontent{
   
    position: absolute;
    top:50%;
    left:20%;
    transform:translate(-50%,-50%);
    color:white;
    text-align:center;
    opacity:0;
    z-index:2;
    transition:all 0.4s ease-in-out;
}
.main:hover .maincontent{
    opacity:1;
    left:50%
}
.main::after{
    content:"";
    
    display:block;
    position:absolute;
    top:0;
    left:0;
    width:100%;
    height:100%;
    background:rgba(0, 0, 0, 0.687);
    opacity: 0;
    z-index:1;
    transition:opacity 0.2s ease-in;

}
.main:hover::after{
    opacity:1;
}

