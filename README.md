# js-question-solutions




// question number 1 start

Q1. Make a 'DISCOUNT CALCULATOR' using js?


let amount = Number(prompt('Enter Your Amount '))

if(isNaN(amount) || amount<=0){
    console.log('Please enter a vaild input')
}
else if(5000>=amount){
    console.log('SORRY!!! you got 0% discount at your purchase')
    console.log('Your total payable amount is ',amount,'rs')
}
else if(7000>=amount){
    console.log('Wow you got 5% discount at your purchase')
    let discount_price = Math.floor((amount*5)/100)
    
    console.log('Your payable amount is',amount-discount_price,'rs')
    console.log('Your are saving ', discount_price,'rs')
}
else if(9000>=amount){
    console.log('Wow you got 10% discount at your purchase')
    let discount_price = Math.floor((amount*10)/100)

    
    console.log('Your payable amount is',amount-discount_price,'rs')
    console.log('Your are saving ', discount_price,'rs')
}
else if(amount>=9001){
    console.log('Wow you got 20% discount at your purchase')
    let discount_price = Math.floor((amount*20)/100)
    
    console.log('Your payable amount is',amount-discount_price,'rs')
    console.log('Your are saving ', discount_price,'rs')
}


<------------------- OR --------------------->


let amount = Number(prompt('Enter Your Amount '))
let discount = 0

if(isNaN(amount) || amount<=0){
    console.log('Please enter a vaild input')
}
else if(5000>=amount){
    console.log('SORRY!!! you got 0% discount at your purchase')
    // console.log('Your total payable amount is ',amount,'rs')
    discount = 0
}
else if(7000>=amount){
    console.log('Wow you got 5% discount at your purchase')
    discount = 5
    
}
else if(9000>=amount){
    console.log('Wow you got 10% discount at your purchase')
    discount = 10
    
}
else if(9001<=amount){
    console.log('Wow you got 20% discount at your purchase')
    discount = 20
    
}

console.log('Your payable amount is',amount-Math.floor((amount*discount)/100),'rs')
console.log('Your are saving ', Math.floor((amount*discount)/100),'rs')

// question number 1 end





// question number 2 start

Q2. Write a JavaScript program to calculate the electricity bill based on the following slab system:

For the first 100 units: ₹4 per unit

For the next 100 units (101–200): ₹6 per unit

For the next 200 units (201–400): ₹8 per unit

For units above 400: ₹13 per unit ?




let unit = Number(prompt('enter electricity unit '))
let amount = 0
if (unit>400 ) {
    amount = (unit-400)*13
    unit = 400
}
if (unit>200 && unit<=400) {
    amount += (unit-200)*8
    unit = 200
}
if (unit>100 && unit<=200) {
    amount += (unit-100)*6
    unit = 100
}
amount += unit*4
console.log(amount)



// question number 2 end






// question number 3 start

Q3 Make 'INR denomination' program?



let amount = Number(prompt('enter amount '))

let total_notes = 0
if (amount>=500) {
    let notes = Math.floor(amount/500)
    console.log(notes,'notes of 500')
    amount = amount - (notes*500)
    total_notes += notes
}
if (amount>=200 && amount<500) {
    let notes = Math.floor(amount/200)
    console.log(notes,'notes of 200')
    amount = amount - (notes*200)
    total_notes += notes
}
if (amount>=100 && amount<200) {
    let notes = Math.floor(amount/100)
    console.log(notes,'notes of 100')
    amount = amount - (notes*100)
    total_notes += notes
}
if (amount>=50 && amount<100) {
    let notes = Math.floor(amount/50)
    console.log(notes,'notes of 50')
    amount = amount - (notes*50)
    total_notes += notes
}
if (amount>=20 && amount<50){
    let notes = Math.floor(amount/20)
    console.log(notes,'notes of 20')
    amount = amount - (notes*20)
    total_notes += notes
}
if (amount>=10 && amount<20){
    let notes = Math.floor(amount/10)
    console.log(notes,'notes of 10')
    amount = amount - (notes*10)
    total_notes += notes
}
if (amount>=5 && amount<10){
    let notes = Math.floor(amount/5)
    console.log(notes,'notes of 5')
    amount = amount - (notes*5)
    total_notes += notes
}
if (amount>=2 && amount<5){
    let notes = Math.floor(amount/2)
    console.log(notes,'notes of 2')
    amount = amount - (notes*2)
    total_notes += notes
}
if (amount>=1 && amount<2){
    let notes = Math.floor(amount/1)
    console.log(notes,'notes of 1')
    amount = amount - (notes*1)
    total_notes += notes
}
console.log('total notes :- ',total_notes,'notes')


------------------ OR ---------------------------------------



let amount = Number(prompt('enter amount '))

let total_notes = 0
if (amount>=500) {
    let notes = Math.floor(amount/500)
    console.log(notes,'notes of 500')
    amount = amount % 500
    total_notes += notes
}
if (amount>=200 && amount<500) {
    let notes = Math.floor(amount/200)
    console.log(notes,'notes of 200')
    amount = amount %200
    total_notes += notes
}
if (amount>=100 && amount<200) {
    let notes = Math.floor(amount/100)
    console.log(notes,'notes of 100')
    amount = amount %100
    total_notes += notes
}
if (amount>=50 && amount<100) {
    let notes = Math.floor(amount/50)
    console.log(notes,'notes of 50')
    amount = amount %50
    total_notes += notes
}
if (amount>=20 && amount<50){
    let notes = Math.floor(amount/20)
    console.log(notes,'notes of 20')
    amount = amount %20
    total_notes += notes
}
if (amount>=10 && amount<20){
    let notes = Math.floor(amount/10)
    console.log(notes,'notes of 10')
    amount = amount %10
    total_notes += notes
}
if (amount>=5 && amount<10){
    let notes = Math.floor(amount/5)
    console.log(notes,'notes of 5')
    amount = amount %5
    total_notes += notes
}
if (amount>=2 && amount<5){
    let notes = Math.floor(amount/2)
    console.log(notes,'notes of 2')
    amount = amount %2
    total_notes += notes
}
if (amount>=1 && amount<2){
    let notes = Math.floor(amount/1)
    console.log(notes,'notes of 1')
    amount = amount %1
    total_notes += notes
}
console.log('total notes :- ',total_notes,'notes')

// question number 3 end

// question number 4 start

Q4 write a program to calculate sum of natural number ?


let input = prompt('Provide a no.')

let num = Number(input)
if (input===null) {
  console.log('cancelled')
}
else{
  
if (isNaN(num)) {
  console.log('invalid input')
}else{
  if (num<0) {
    console.log('it is a negative no')
  }
  else if (num===0) {
    console.log('it is zero')
  }
  else{
    let total = 0
    for (let i = 0; i <= num; i++) {
    total += i
    
    }
    console.log('sum of natural no :- ',total)
  }
}
}


// question number 4 end



// question number 5 start

Q5 write a program to calculate factorial of a given number?


let input = prompt('Provide a no.')

let num = Number(input)
if (input===null) {
  console.log('cancelled')
}
else{
  
if (isNaN(num)) {
  console.log('invalid input')
}else{
  if (num<0) {
    console.log('it is a negative no')
  }
  else if (num===0) {
    console.log('it is zero')
  }
  else{
    let fact = 1
    for (let i = 1; i <= num; i++) {
    fact *= i
    
    }
    console.log('factorial of ',num,' :- ',fact)
  }
}
}

// question number 5 end


// question number 6 start 

Q6 write a program to find factors of given number?



let input = prompt('enter a no :- ')
let num = Number(input)

if (input===null) {
  console.log('cancelled')
}
else{
  
  if (isNaN(num)) {
    console.log('invalid input')
  }else{
    if (num<0) {
        console.log('it is a negative no')
      }
      else if (num===0) {
        console.log('it is zero')
      }
    else{
      for (let i = 1; i <= Math.floor(num/2); i++) {
      if (num%i === 0){
        console.log(i)
      } 
    }
    console.log(num)
    }
  }
}


// question number 6 end


//question number 7 start

Q7 write a program to find prime number?

let input = prompt('enter a no :- ')
let num = Number(input)

if (input===null) {
  console.log('cancelled')
}
else{
  
  if (isNaN(num)) {
    console.log('invalid input')
  }else{
    if (num<0) {
        console.log('it is a negative no')
      }
      else if (num===0) {
        console.log('it is zero')
      }
    else{
      console.log(isPrime(num))
    }
  }
}

function isPrime(n) {
  if (n===2) return true
    if (n%2===0) return false
    for (let i = 3; i <= Math.floor(Math.sqrt(n));  i+=2) {
    if (n===1) return false
      if(n%i===0) return false
    }
    return true
  
}

// question number 7 end


// question number 8 start

Q8 write a program to calculate sum of digits?



let input = prompt('enter a no :- ')
let num = Number(input)

if (input===null) {
  console.log('cancelled')
}
else{
  
  if (isNaN(num)) {
    console.log('invalid input')
  }else{
    if (num>0) {
        sum = 0
        while(num>0){
            rem = num%10
            sum += rem
            num = Math.floor(num/10)
        }
        console.log(sum)
      }
    }
  }


// question number 8 end


// question number 9 start

Q9 Make a program to reverse the digit?

let input = prompt("enter the number");
if (input === null) {
  console.log("cancel");
} else {
  let num = Number(input);
  if (isNaN(num)) {
    console.log("invalid input");
  } else {
    if (num > 0) {
      let rev = 0;
      while (num > 0) {
        rem = num % 10;
        rev = rev * 10 + rem;
        num = Math.floor(num / 10);
      }
      console.log(rev);
    } else {
      console.log("number should be positive or greater than 0");
    }
  }
}



// question number 9 end



//question number 10 start

Q10 Make a program to check the given number is strong or not?


let input = prompt("enter the number");
if (input === null) {
  console.log("cancel");
} else {
  let num = Number(input);
  if (isNaN(num)) {
    console.log("invalid input");
  } else {
    if (num > 0) {
      let copy = num;
      let sum = 0;
      while (num > 0) {
        rem = num % 10;
        let fact = 1;
        for (let i = 1; i <= rem; i++) {
          fact *= i;
        }
        sum = sum + fact;
        num = Math.floor(num / 10);
      }
      if (copy === sum) {
        console.log("strong number");
      } else {
        console.log("not strong number");
      }
    } else {
      console.log("number should be positive or greater than 0");
    }
  }
}



// question number 10 end




 
