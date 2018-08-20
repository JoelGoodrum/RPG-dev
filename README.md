# RPG-dev
game in dev

// game variables

location["CTA building","Wall Street"]; //game levels

var wallet = 0;
var shares = 1;
var CTAshares = 35;

// CTA level

function cta() {
  console.log('Your in the CTA (Central Tech Agencie) building.');
  console.log('Press "W" to work');
  console.log('Press "M" to go to the Market');
  return "wallet $" + wallet;
}

function work() {
  // every time character works, 20$ is added to wallet
  wallet += 20;
  cta();
}

function market() {
  WallSt();
}


//WallStreet

function WallSt() {
  console.log("Youre at WallStreet.")
  console.log('Press "B" to buy 1 CTA share at' + CTAshares);
  console.log('Press "S" to sell one CTA share at' + CTAshares);
  console.log('Press "C" to return to CTA building');
  return"wallet $" + wallet;
}

function buy() {
  wallet -= CTAshares;
  shares++;
  WallSt();
}

function sell() {
  wallet += CTAshares;
  shares--;
  WallSt();
}

function returnCTA() {
  cta();
}

