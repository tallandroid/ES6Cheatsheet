# ES6Cheatsheet

CheatSheet creates from [MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide).

===================

### Rest Parameters 
* Remove the boilerplate code:
```
function x(a,b,c){
 var args = Array.prototype.slice.call(arguments);
 
}
```
Consume like this :
```
function x(...thisArgs){
 console.log(...thisArgs instanceof Array); //true
 }
```
*Note: Not implemented in Chrome yet - Lookup browser compatibility*

### Lazy getters
Allows you to execute a custom procedure when the property is accessed. Optimized to **memoize** the value calculated(**Maybe only Gecko**)

```
var obj = {
  get a():{
    console.log("hoodibaba");
  },
  get service():{
    return new function(){
      //not sure how the scope wil work here    
    }
  },
  get [expr]:{
    //properties can be evaluated as an expression too
  }
}
//obj.a = hoodibaba
//obj.service = //no idea
```

=================

### Setters
Not sure if they will find any use. Looking for a possible use cases. 

=================

### Function declaration vs Function expression vs Function constructor
- **Function declaration**
```function foo(){}```
- **Function expression** 
``` var x = function foo(){}```
- function expression creates a closure vs *Function* inherits only global scope
- function declaration and function expression are parsed only once
- function expression gives you a way to create private functions
- declaration and expression can be used interchangeable as apart from hoisting , I dont see any difference. **Need verification**
 
==================

###TBD
- Arrow functions
- Default parameters

