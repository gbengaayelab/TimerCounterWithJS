<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/4.4.1/css/bootstrap.min.css">
    <title>Ecommerce Calculator</title>
</head>
<body>
    <div class="row">
        <div class="col-sm-2 m-3 p-3"></div>
        
        <div class="col-sm-6 m-4 p-4">
            
            <div class="jumbotron p-3 m-3 border rounded border-light text-center">
                   <div class="container border rounded border-light text-center"><h3 class="display-3">Timer Counter App With JS</h3></div> 
                 <h1 class="text-primary display-1 mt-3 ml-3 pt-3 timer-h1"> <span class="minute">00</span> : <span class="second">00</span></h1>
                 <button class="btn btn-success text-center rounded p-3 m-3" style="width: 120px;" data-action="start">Start</button>
                 <button class="btn btn-danger text-center rounded p-3 m-3 btn-stop" style="width: 120px;" data-action="stop">Stop</button> <br>
                 <button class="text-secondary btn-link m-3 p-3" data-action="reset">Reset</button>
       
            </div>
        </div></div>
        <div class="col-sm-3 m-3 p-3"></div>
    </div>    
  
    <script>
        // Grab Everything I need
        const grabTimerMins=document.querySelector('.minute');
        const grabTimerSecs=document.querySelector('.second');
        const grabStartButton= document.querySelector('[data-action="start"]');
        const grabStopButton= document.querySelector('[data-action="stop"]');
        const grabResetLink= document.querySelector('[data-action="reset"]');
        
        let intervalCallingFunction;
        
        
         
        // Create all the functions needed
          startCounting = () =>{
            intervalCallingFunction=setInterval(setTimer,1000);
              
          }   

          stopCounting = () =>{
            clearInterval(interValCallingFunction);


          }
         
          resetCounting = () =>{


          }
          
          padMinute = (numbr) =>{
            return (numbr<10) ? '0' +numbr: numbr;
            //   if(numbr<10){
            //       return '0'+numbr;
            //   }
            //   else return numbr;
          }
          let timeCount= 0;
          setTimer = () => {
         timeCount++;

         const numOfMins= Math.floor(timeCount/60);
         const numOfSecs= timeCount%60;

         grabTimerMins.innerText = padMinute(numOfMins);
         grabTimerSecs.innerText = padMinute(numOfSecs); 
        }


          


        // Add event listeners
        grabStartButton.addEventListener('click', startCounting);
        grabStopButton.addEventListener('click', stopCounting);
        grabResetLink.addEventListener('click', resetCounting);
          
       


        //on Run first
       
    </script>
</body>
</html>
