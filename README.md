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
 
 Anonymous Function:
 
  var a = [5, 9, 63, 29, 35, 6, 55, 23]
var prime = [];

var isPrime=function(item){
    var identifier = item / 2;
      for (var j = 2; j <= identifier; j++) {
       if ((item % j) == 0) { // modulous
        return false;
       } 
     }
     return true;
}
for (var index = 0; index < a.length; index++) {
  if (isPrime(a[index])) {
      prime.push(a[index])
  }
}

console.log(prime);

IIFE:

var a = [5, 9, 63, 29, 35, 6, 55, 23]
var prime = [];

function isPrime(item) {
    var identifier = item / 2;
      for (var j = 2; j <= identifier; j++) {
       if ((item % j) == 0) { // modulous
        return false;
       } 
     }
     return true;
}
for (var index = 0; index < a.length; index++) {
  if (isPrime(a[index])) {
      prime.push(a[index])
  }
}

console.log(prime);

  Arrow function:
  
  var a = [5, 9, 63, 29, 35, 6, 55, 23]
var prime = [];

var isPrime=(item)=> {
    var identifier = item / 2;
      for (var j = 2; j <= identifier; j++) {
       if ((item % j) == 0) { // modulous
        return false;
       } 
     }
     return true;
}
for (var index = 0; index < a.length; index++) {
  if (isPrime(a[index])) {
      prime.push(a[index])
  }
}

console.log(prime);
    
  e.Return all the palindromes in an array
  
  // Anonymous Function:

 var res=function(arr){
    var arr1=[];
    for(var i=0;i<arr.length;i++){
    arr1.push(arr[i].split("").reverse().join(""))
     }
  var palin=[];
for(var j=0;j<arr.length;j++){ 
  if(arr[j]===arr1[j]){
    palin.push(arr[j])} }
 return palin;

 }
  console.log(res(["abc","madam","cool","malayalam","racecar"]));
  
//  IIFE:

(function (arr){
      var arr1=[];
    for(var i=0;i<arr.length;i++){
    arr1.push(arr[i].split("").reverse().join(""))
     }
  var palin=[];
for(var j=0;j<arr.length;j++){ 
  if(arr[j]===arr1[j]){
    palin.push(arr[j])} }
 return palin;})(["abc","madam","cool","malayalam","racecar"]);
 
// Arrow Function:  

var res=(arr)=>{
      var arr1=[];
    for(var i=0;i<arr.length;i++){
    arr1.push(arr[i].split("").reverse().join(""))
     }
  var palin=[];
for(var j=0;j<arr.length;j++){ 
  if(arr[j]===arr1[j]){
    palin.push(arr[j])} }
 return palin;}
  console.log(res(["abc","madam","cool","malayalam","racecar"]));
  
  f.Return median of two sorted arrays of the same size
  
//Anonymous function

 var res=function(a,b){
   for(var i=0;i<b.length;i++){
     var temp=0;
     a.push(b[i])
     }
 for(var j=0;j<a.length;j++){
   var temp=a[j]
   for(var k= j-1;j >= 0 && (a[k] >temp); k--) {
        a[k+1] = a[k];
   }
    a[k+1] = temp;
     }  
     var e=(a.length)/2;
  if(a.length%2===0)
   {return ((a[e]+a[e-1])/2) }
 }
  console.log(res([100,11],[1,30]));
  
  //IIFE
  
  (function(a,b){
   for(var i=0;i<b.length;i++){
     var temp=0;
     a.push(b[i])
     }
 for(var j=0;j<a.length;j++){
   var temp=a[j]
   for(var k= j-1;j >= 0 && (a[k] >temp); k--) {
        a[k+1] = a[k];
   }
    a[k+1] = temp;
     }  
     var e=(a.length)/2;
  if(a.length%2===0)
   {return ((a[e]+a[e-1])/2) }
 })([100,11],[1,30])
 // console.log(res([100,11],[1,30]));
 
 //Arrow Function
 
 var res=(a,b)=>{
   for(var i=0;i<b.length;i++){
     var temp=0;
     a.push(b[i])
     }
 for(var j=0;j<a.length;j++){
   var temp=a[j]
   for(var k= j-1;j >= 0 && (a[k] >temp); k--) {
        a[k+1] = a[k];
   }
    a[k+1] = temp;
     }  
     var e=(a.length)/2;
  if(a.length%2===0)
   {return ((a[e]+a[e-1])/2) }
 }
  console.log(res([100,11],[1,30]));
  
  g.Remove duplicates from an array
  
  //Anonymous function
  
var res=function(arr){
  var a=[];
  for(var i=0;i<arr.length;i++){
 if (a.indexOf(arr[i]) === -1)
            a.push(arr[i]);
    
    }return a;
    }
    console.log(res([1,2,1,2,3,4,3,4]));

//IIFE

(function(arr){
  var a=[];
  for(var i=0;i<arr.length;i++){
 if (a.indexOf(arr[i]) === -1)
            a.push(arr[i]);
    
    }return a;
    })([1,2,1,2,3,4,3,4])
    
//Arrow Function

var res=(arr)=>{
  var a=[];
  for(var i=0;i<arr.length;i++){
 if (a.indexOf(arr[i]) === -1)
            a.push(arr[i]);
    
    }return a;
    }
    console.log(res([1,2,1,2,3,4,3,4]));
  
  h.Rotate an array by k times
  
//Anonymous function

var res=function(arr,n){
  var temp=arr.slice(0,n)
  var temp1=arr.slice(n)
  var arr1=[...temp1,...temp]
  return arr1;
}
console.log(res([1, 2, 3, 4, 5, 6, 7,8],4));

//IIFE

(function(arr,n){
  var temp=arr.slice(0,n)
  var temp1=arr.slice(n)
  var arr1=[...temp1,...temp]
  return arr1;
})([1, 2, 3, 4, 5, 6, 7,8],3)

//Arrow function

var res=(arr,n)=>{
  var temp=arr.slice(0,n)
  var temp1=arr.slice(n)
  var arr1=[...temp1,...temp]
  return arr1;
}
console.log(res([1, 2, 3, 4, 5, 6, 7,8],4));
