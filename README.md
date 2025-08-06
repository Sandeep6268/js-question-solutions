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

