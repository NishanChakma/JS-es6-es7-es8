# for in
    var obj = {a:1, b:2, c:3};  
    for (var prop in obj) { 
        console.log(obj[prop]); 
    }
    output: 
    1 
    2 
    3
# for of
    for (let val of[12 , 13 , 123]) {   
        console.log(val) 
    } 
    output:
    12 
    13 
    123
# do while
    var n = 10;   
    do { 
        console.log(n); 
        n--; 
    } 
    while(n>=0); 
    output:
    10 
    9 
    8 
    7 
    6 
    5 
    4 
    3 
    2 
    1 
    0
# while 
    var num = 5; 
    var factorial = 1; 
    while(num >= 1) { 
        factorial = factorial * num; 
        num--; 
    } 
    console.log("The factorial  is "+factorial); 
    output:
    The factorial is 120
# for loop: Label with Break
    outerloop: // This is the label name  
    for (var i = 0; i < 5; i++) {  
        console.log("Outerloop: " + i);  
        innerloop:  
        for (var j = 0; j<5; j++) {  
            if (j>3 ) break; 
            
            // Quit the innermost loop  
            if (i == 2) break innerloop; 
            
            // Do the same thing  
            if (i == 4) break outerloop; // Quit the outer loop  
            console.log("Innerloop: " + j);  
        }  
    }
    output:
    Outerloop: 0 
    Innerloop: 0 
    Innerloop: 1 
    Innerloop: 2 
    Innerloop: 3 
    Outerloop: 1 
    Innerloop: 0 
    Innerloop: 1 
    Innerloop: 2 
    Innerloop: 3 
    Outerloop: 2 
    Outerloop: 3 
    Innerloop: 0 
    Innerloop: 1 
    Innerloop: 2 
    Innerloop: 3 
    Outerloop: 4
# outerloop: // This is the label name  
    for (var i = 0; i < 3; i++) {  
    console.log("Outerloop: " + i);      
        for (var j = 0; j < 5; j++) {  
            if (j == 3){  
                continue outerloop;  
            }  
            console.log("Innerloop: " + j );  
        }  
    } 
    output:
    Outerloop: 0 
    Innerloop: 0 
    Innerloop: 1 
    Innerloop: 2 
    Outerloop: 1 
    Innerloop: 0 
    Innerloop: 1 
    Innerloop: 2 
    Outerloop: 2 
    Innerloop: 0 
    Innerloop: 1 
    Innerloop: 2 
# forEach
    var array1 = ['a', 'b', 'c'];
    array1.forEach(function(element) {
    console.log(element);
    });
    // expected output: "a"
    // expected output: "b"
    // expected output: "c"
