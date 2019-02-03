# Default Parameters in ES6:
    var calculateArea = function(height = 50, width = 80) {  
        // write logic
        ...
    }
# Multi-line Strings:
    let myData = `this line will be auto multiline!,     
                Do you need some time on your own
                Do you need some time all alone
                Everybody needs some time
                On their own
                Don't you…`
                
# Arrow Functions:
    I.	const multiplyES6 = (x, y) => { return x * y };

    II.	$('.btn').click((event) => {   
        this.doSomething() 
        });

    III.var dateFromTimeStamp = timeStamp => new Date(timeStamp);
        dateFromTimeStamp(1489957823485); //Sun Mar 19 2017 22:10:23 GMT+0100 (WAT)
# Promises: In ES5, we need to use setTimeout():
    var asyncCall =  new Promise((resolve, reject) => {
    // do something async 
    resolve();
    }).then(()=> {   
        console.log('Yay!');
    })
# const and let keywords:
    function f() {
	  var x = 1
	  let y = 2
	  const z = 3
	  {
	    var x = 100
	    let y = 200
	    const z = 300
	    console.log('x in block scope is', x)
	    console.log('y in block scope is', y)
	    console.log('z in block scope is', z)
	  }
	  console.log('x outside of block scope is', x)
	  console.log('y outside of block scope is', y)
	  console.log('z outside of block scope is', z)
	}	
	f();

    output:
    X in block scope is 100
    y in block scope is 200 
    z in block scope is 300 
    x outside of block scope is 100 
    y outside of block scope is 2 
    z outside of block scope is 3 


# Spread
    var defaultColors = ['red', 'blue', 'green']
    var userDefinedColors = ['yellow', 'orange']
    var mergedColors = [...defaultColors, ...userDefinedColors]
    console.log('Merged colors', mergedColors)
    output:
    Merged colors ["red","blue","green","yellow","orange"] 
# Rest
    function printColors(first, second, third, ...others) {
        console.log('Top three colors are ' + first + ', ' + second + ' and ' + third + '. Others are: ' + others)
    }
    printColors('yellow', 'blue', 'orange', 'white', 'black')
    output:
    Top three colors are yellow, blue and orange. Others are: white,black 
# Destructuring
    function printFirstAndSecondElement([first, second]) {
        console.log('First element is ' + first + ', second is ' + second)
    }

    function printSecondAndFourthElement([, second, , fourth]) {
        console.log('Second element is ' + second + ', fourth is ' + fourth)
     }

     var array = [1, 2, 3, 4, 5]

     printFirstAndSecondElement(array)
     output:
     First element is 1, second is 2 
     Second element is 2, fourth is 4 
printSecondAndFourthElement(array)
