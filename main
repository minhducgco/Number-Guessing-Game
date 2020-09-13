var button = document.getElementById("guessButton");
var message = document.getElementById("message");
var past = document.getElementById("past");
var count = 10;
	
button.addEventListener('click', function(){
	var random = Math.floor(Math.random()*10);
    var input = document.getElementById("number");
    if(!input.value){
    	alert("Please enter the number, do not leave it blank!");
    }else{
    	count --;
    	if(count < 0){
    		alert("You have run out of guesses!");
    		button.disabled  = true;
    		setTimeout(function(){
    			location.reload();
			}, 5000);
    	}else{
    		if(random == parseInt(input.value)){
    			message.innerHTML = "Congratulations!! You guessed correctly. <br> You have "+ count +" left to guess";
    			message.style.background = "green";
    			button.disabled  = true;
    			setTimeout(function(){
    				location.reload();
				}, 5000);
    		}else if(random > parseInt(input.value)){
				message.innerHTML = "Sorry your guess is too high. <br> You have "+ count +" left to guess";
				message.style.background = "red";
    		}else{
    			message.innerHTML = "Sorry your guess is too low. <br> You have "+ count +" left to guess";
    			message.style.background = "red";
    		}
    		past.append(input.value+ " ") ;
    	}
    	
    }
    
});