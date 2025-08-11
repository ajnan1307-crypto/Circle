<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Animated Circles</title>
  <style>
    *{
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      background: #000;
      overflow:hidden;
      font-family: system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;
    }

    .container {
      position: absolute;
      top: 20%;
      height: 90%;
      display: flex;
      justify-content: center;
      align-items: center;
      width: 100%;
      pointer-events: none; /* so clicks pass through if needed */
      transform-style: preserve-3d;
      perspective: 800px;
    }

    .circle {
      position: absolute;
      background: transparent;
      width: calc(var(--i) * 2.5vmin);
      aspect-ratio: 1;
      border-radius: 50%;
      border: 3px solid rgb(255, 20, 13);
      transform-style: preserve-3d;
      transform: rotateX(70deg) translateZ(50px);
      animation: animate 3s ease-in-out calc(var(--i) * 0.08s) infinite;
      box-shadow: 0 0 15px rgb(124,124,124), inset 0 0 15px rgb(124,124,124);
      left: 50%;
      top: 50%;
      translate: -50% -50%;
      mix-blend-mode: screen;
    }

    @keyframes animate {
      0%, 100% {
        transform: rotateX(70deg) translateZ(50px) translateY(0);
        filter: hue-rotate(0);
      }
      50% {
        transform: rotateX(70deg) translateZ(50px) translateY(-50vmin);
        filter: hue-rotate(360deg);
      }
    }

    /* optional: make the smallest circles more subtle */
    .circle[style*="--i:0"] { width: calc(0 * 2.5vmin); border-color:red; opacity: 0.09; }
  </style>
</head>
<body>
  <div class="container">
    <div class="circle" style="--i:0;"></div>
    <div class="circle" style="--i:1;"></div>
    <div class="circle" style="--i:2;"></div>
    <div class="circle" style="--i:3;"></div>
    <div class="circle" style="--i:4;"></div>
    <div class="circle" style="--i:5;"></div>
    <div class="circle" style="--i:6;"></div>
    <div class="circle" style="--i:7;"></div>
    <div class="circle" style="--i:8;"></div>
    <div class="circle" style="--i:9;"></div>
    <div class="circle" style="--i:10;"></div>
    <div class="circle" style="--i:11;"></div>
    <div class="circle" style="--i:12;"></div>
    <div class="circle" style="--i:13;"></div>
    <div class="circle" style="--i:14;"></div>
    <div class="circle" style="--i:15;"></div>
    <div class="circle" style="--i:16;"></div>
    <div class="circle" style="--i:17;"></div>
    <div class="circle" style="--i:18;"></div>
    <div class="circle" style="--i:19;"></div>
    <div class="circle" style="--i:20;"></div>
    <div class="circle" style="--i:21;"></div>
    <div class="circle" style="--i:22;"></div>
    <div class="circle" style="--i:23;"></div>
    <div class="circle" style="--i:24;"></div>
    <div class="circle" style="--i:25;"></div>
    <div class="circle" style="--i:26;"></div>
    <div class="circle" style="--i:27;"></div>
    <div class="circle" style="--i:28;"></div>
    <div class="circle" style="--i:29;"></div>
    <div class="circle" style="--i:30;"></div>
    <div class="circle" style="--i:31;"></div>
  </div>
</body>
</html>

