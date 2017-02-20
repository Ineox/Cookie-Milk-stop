# Cookie-Milk-stop

var cookieCount = 0
var milkCount = 0

function cookieChocoLate(cookieType) {
    console.log('order of ' + cookieType );
        cookieCount = cookieCount+ 1;
}

function countryMilk(country) {
  console.log('with a order of: ' + country +  ' milk' );
   milkCount = milkCount + 1;
}

function getSubTotal(x, y) {
 
  return   milkCount * 1.50 + cookieCount * 2.50;
}

function getTax () {
 
  return getSubTotal(milkCount + cookieCount) * 0.08;
}

function getTotal () {
  return getSubTotal(milkCount + cookieCount) + getTax();
}

cookieChocoLate('chocolate chip cookie');
countryMilk('german'); 

console.log(getSubTotal(cookieCount, milkCount));
console.log(getTotal());
