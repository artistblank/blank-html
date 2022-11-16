
emm.....其实我是一个漂亮的旋转立方体，点我一下我就不转喽，点一下空白的地方我又可以转辣
 <html lang="en">
 <head>
     <meta charset="UTF-8">
     <meta http-equiv="X-UA-Compatible" content="IE=edge">
     <meta name="viewport" content="width=device-width, initial-scale=1.0">
     <title>Document</title>
     <style>
         *{
             margin: 0;
             padding: 0;
         }
         .space{
             position: relative;
             width: 800px;
             height: 800px;
             border: 1px solid #000;
             margin: 100px auto;
             perspective: 1000px;
             background: linear-gradient(#a6acfe,#ff9bcc);
         }
         .space:hover section{
             animation-play-state: paused;

         }
         /* section相当于魔方支架 */
         section{
             position: absolute;
             width: 600px;
             height: 600px;  
             border-radius: 500px;   
             border: 10px solid rgb(255, 255, 255);    
             left: 0;
             right: 0;
             top: 0;
             right: 0;
             bottom: 0;
             margin: auto;
             transform-style: preserve-3d;/*设置3d空间*/
             /* transform: rotateX(120deg) rotateY(120deg) rotateZ(120deg); */
             animation: run 3s linear infinite;

         }
         @keyframes run {
             0%{}
             100%{
                 transform: rotateX(360deg) rotateY(360deg) rotateZ(360deg) ;
             }
         }
         .face{
             position: absolute;
             width: 300px;
             height: 300px;
             border-radius: 200px;
             left: 0;
             right: 0;
             top: 0;
             right: 0;
             bottom: 0;
             margin: auto;
             opacity: 0.7;/*设置透明度*/
             font-size: 30px;
             text-align: center;
             line-height: 300px;

         }
         .face:nth-child(1){
             background: linear-gradient(#8dc6fe,#fe8df6);
             transform: translateZ(150px);
         }
         .face:nth-child(2){
             background: linear-gradient(#8ddefe,#ff7df6);
             transform: translateZ(-150px);
         }
         .face:nth-child(3){
             background: linear-gradient(#8dc6fe,#fe8df6);
             transform: translateX(-150px) rotateY(-90deg);
         }
         .face:nth-child(4){
             background: linear-gradient(#8dc6fe,#fe8df6);
             transform: translateX(150px) rotateY(90deg);
         }
         .face:nth-child(5){
             background: #ff97f8;
             background: linear-gradient(#8dc6fe,#fe8df6);
             transform: translateY(-150px) rotateX(90deg);
         }
         .face:nth-child(6){
             background: linear-gradient(#8dc6fe,#fe8df6);
             transform: translateY(150px) rotateX(90deg);
         }
         .circle{
             position: absolute;
             width: 600px;
             height: 600px;
             border-radius: 400px;
             border: 10px solid #fff;
             left: 0;
             right: 0;
             top: 0;
             right: 0;
             bottom: 0;
             margin: auto;
             animation: run 3s linear infinite;
         }
     </style>
 </head>
 <body>
     <div class="space">
         <section>
             <div class="face">

             </div>
             <div class="face">你是最美丽的</div>
             <div class="face">你是最可爱的</div>
             <div class="face">你是最努力的</div>
             <div class="face">你是最聪明的</div>
             <div class="face">你是最优秀的</div>
             <div class="circle"></div>
         </section>
     </div>
 </body>
 </html>
 <!--让三个盒子居中对齐-->
 <!-- 
     位移变换
     transform:translate()
     变换中心-默认在中心点
     transform-origin
  -->
