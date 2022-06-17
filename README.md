# day05
Functions
1.Do the below programs in anonymous function & IIFE
   a.Print odd numbers in an array
   
  Anonymous function:
  var res=function(arr){
  var b=[];
  for(var i=0;i<arr.length;i++){
  if (arr[i] == 1 || arr[i]%2 ==1)
   b.push(arr[i]);
  }
  return b;}
  console.log(res([1,2,3,4,5,6,7,8,9,10]));
  
  IIFE:
  
(function (arr){
  var b=[];
  for(var i=0;i<arr.length;i++){
  if (arr[i] == 1 || arr[i]%2 ==1)
   b.push(arr[i]);
  }
  return b;})([1,2,3,4,5,6,7,8,9,10]);
  
  Arrow Function:
  
  
var res=(arr)=>{
  var b=[];
  for(var i=0;i<arr.length;i++){
  if (arr[i] == 1 || arr[i]%2 ==1)
   b.push(arr[i]);
  }
  return b;}
  console.log(res([1,2,3,4,5,6,7,8,9,10]));
  
b.Convert all the strings to title caps in a string array
Anonymous Function:

var res=function(str){
  var b=[];
  str=str.split(' ')
  for(var i=0;i<str.length;i++){
  str[i]=str[i].charAt(0).toUpperCase()+str[i].substr(1).toLowerCase() }
   b.push(str[i]);
return str;
  }
  console.log(res("how are you"));
  
  IIFE:
  (function(str){
  var b=[];
  str=str.split(' ')
  for(var i=0;i<str.length;i++){
  str[i]=str[i].charAt(0).toUpperCase()+str[i].substr(1).toLowerCase() }
   b.push(str[i]);
return str;
  })("how are you");


Arrow Function:
var res=(str)=>{
  var b=[];
  str=str.split(' ')
  for(var i=0;i<str.length;i++){
  str[i]=str[i].charAt(0).toUpperCase()+str[i].substr(1).toLowerCase() }
   b.push(str[i]);
return str;
  }
  console.log(res("how are you"));
  
 
c.Sum of all numbers in an array

Anonymous Function:

 var res=function(arr){
  var sum=0;
  for(var i=0;i<arr.length;i++){
   sum=sum+arr[i];
    }  return sum; 
  }
  console.log(res([10,20,30,40,50]));

IIFE:
  (function(arr){
  var sum=0;
  for(var i=0;i<arr.length;i++){
   sum=sum+arr[i];
    }  return sum; 
  })([10,20,30,40,50]);
    
Arrow Function:

 var res=(arr)=>{
  var sum=0;
  for(var i=0;i<arr.length;i++){
   sum=sum+arr[i];
    }  return sum; 
    }
  console.log(res([10,20,30,40,50]));
  
 d. Return all the prime numbers in an array

  
    
    
    
  }
  console.log(res([10,20,30,40,50]));
