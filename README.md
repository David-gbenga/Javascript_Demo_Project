# Solving-Problems-with-Javascript
This code was used to help a cashier receive money from customers and give them balance with the specified  currencies
// help the cashier 
var total=prompt("Amount due");
var moneyPaid = prompt("Amount Paid");
total  = parseFloat(total).toFixed(2);
moneyPaid = parseFloat(moneyPaid).toFixed(2);

// calculate the change to be given to customer with a decimal place of 2
var change = (moneyPaid-total).toFixed(2);

//Print the transaction summary 
console.log('Amount due $' + total + '/Amount Paid $' + moneyPaid + '/change $' + change);
/*notes 
50, 20, 10, 5
coins
2, 1,50,20,10,5,2,1p*/
var note_coins = [
    {
        value: 50,
        name: '$50 notes:'
    },
    {
        value: 20,
        name: '$20 notes:'
    },
     {
        value: 10,
        name: '$10 notes:'
    },
     
     {
        value: 5,
        name: '$5 notes:'
    },
     {
        value: 2,
        name: '$2 coins:'
    },
     {
        value:1,
        name: '$1 coins:'
    },
     {
        value: 0.50,
        name: '50p coins:'
    },
     {
        value: 0.20,
        name: '20p coins:'
    },
     {
        value: 0.10,
        name: '10p coins:'
    },
     {
        value: 0.05,
        name: '5p coins:'
    },
     {
        value: 0.02,
        name: '2p coins:'
    },
     {
        value: 0.01,
        name: '1p coins:'
    }

     
];
var i = 0;
while ( change > 0 ){
    note_coins[i].return =
        Math.floor(change/note_coins[i].value);
    change =
        (change%note_coins[i].value).toFixed(2);
    note_coins[i].return > 0?
        console.log(note_coins[i].name +
                   note_coins[i].return): 0;
    i ++
};






