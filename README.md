![image](https://github.com/user-attachments/assets/050d5df4-92cd-4b93-a61e-1226abb82f58)
A fun project using HTML and inner CSS to create a visually appealing wheel with five colors. It rotates continuously on hover for 2 seconds and smoothly returns to its original position when the mouse interaction stops. Enjoy the playful experience! 🎡✨

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Rotating wheel</title>
  <style>
    /*rotating animation*/
    @keyframes rotateAnimation {
      from {
        transform: rotate(0deg);
      }
      to {
        transform: rotate(360deg);
      }
    }

    @keyframes reverseAnimation {
      from {
        transform: rotate(360deg);
      }
      to {
        transform: rotate(0deg);
      }
    }


    .container{
      display: flex;
      justify-content: center;
      align-items: center;
    }

    .wheel {
      position :absolute;
      top:15%;
      left:30%;
      
      
      
      
      width: 500px;
      height: 500px;
      border-radius: 50%;
      background: conic-gradient(rgb(255, 0, 0) 0% 20%,#00f 20% 40%,rgb(0, 204, 255) 40% 60%, rgb(255, 255, 0) 60% 80%, #0f0 80% 100%);
      transition: transform 2s ease-in-out; 
    }

    /*rotate over hovering*/
    .wheel:hover {
      transform: rotate(900deg);

    }


    #center-circle {
            position: relative;
            width: 250px;
            height: 250px;
            top: 25%;
            left: 25%;
            border-radius: 50%;
            background-color: white;
        }

  </style>
</head>
<body>

<div class="container">
  <div class="wheel">
    <div id="center-circle"></div>
  </div>
</div>

</body>
</html>
