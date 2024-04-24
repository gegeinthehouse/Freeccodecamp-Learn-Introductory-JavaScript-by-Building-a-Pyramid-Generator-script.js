# Freeccodecamp-Learn-Introductory-JavaScript-by-Building-a-Pyramid-Generator-script.js
Freeccodecamp Learn Introductory JavaScript by Building a Pyramid Generator script.js
This is just the final answer. I jst want to say this project is very easy and you can do it. Time taken: 1hr, 42 min
Im neww to github so please correct me if i did something wrong

const character = "!";
const count = 10;
const rows = [];
let inverted = false;

function padRow(rowNumber, rowCount) {
  return " ".repeat(rowCount - rowNumber) + character.repeat(2 * rowNumber - 1) + " ".repeat(rowCount - rowNumber);
}

for (let i = 1; i <= count; i++) {
  if (inverted) {
    rows.unshift(padRow(i, count));
  } else {
    rows.push(padRow(i, count));
  }
}

let result = ""

for (const row of rows) {
  result = result + "\n" + row;
}

console.log(result);

