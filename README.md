# JS Bakery Orders

This project is a simple web application designed to manage and display orders for a bakery. The challenge involves writing JavaScript to dynamically update order details based on data attributes in the HTML. 

## Table of Contents

- [Overview](#overview)
- [Files](#files)
- [Steps to Complete the Challenge](#steps-to-complete-the-challenge)
  - [Step 1: Fix Variable Naming and Initialization](#step-1-fix-variable-naming-and-initialization)
  - [Step 2: Select Inner Elements](#step-2-select-inner-elements)
  - [Step 3: Assign Values and Status](#step-3-assign-values-and-status)
- [How to Run the Project](#how-to-run-the-project)
- [Technologies Used](#technologies-used)
- [License](#license)

## Overview

The main goal of this challenge is to use JavaScript to update the HTML document with order details dynamically. The HTML file contains order information with data attributes, and the JavaScript file reads these attributes and updates the content accordingly.

## Files

- **index.html**: Contains the structure and data attributes for each order.
- **script.js**: Contains the JavaScript code to dynamically update the order details.

## Steps to Complete the Challenge

### Step 1: Fix Variable Naming and Initialization

Correct the way variables are named and how elements are selected.

**Original Code:**
```javascript
const 1-root = document(order1),
const 1-biscuits: document(biscuits),
const 1-donuts: document(donuts),
const 1-pancakes: document(pancakes),
const 1-status: document(status)
```

**Fixed Code:**
```javascript
const order1Root = document.querySelector('[data-key="order1"]');
const order2Root = document.querySelector('[data-key="order2"]');
const order3Root = document.querySelector('[data-key="order3"]');
```

### Step 2: Select Inner Elements

Select the inner elements where the order details will be displayed.

**Original Code:**
```javascript
const 1-biscuits: document(biscuits),
const 1-donuts: document(donuts),
const 1-pancakes: document(pancakes),
const 1-status: document(status)
```

**Fixed Code:**
```javascript
const order1Biscuits = order1Root.querySelector('.biscuits .count');
const order1Donuts = order1Root.querySelector('.donuts .count');
const order1Pancakes = order1Root.querySelector('.pancakes .count');
const order1Status = order1Root.querySelector('.status dd');

const order2Biscuits = order2Root.querySelector('.biscuits .count');
const order2Donuts = order2Root.querySelector('.donuts .count');
const order2Pancakes = order2Root.querySelector('.pancakes .count');
const order2Status = order2Root.querySelector('.status dd');

const order3Biscuits = order3Root.querySelector('.biscuits .count');
const order3Donuts = order3Root.querySelector('.donuts .count');
const order3Pancakes = order3Root.querySelector('.pancakes .count');
const order3Status = order3Root.querySelector('.status dd');
```

### Step 3: Assign Values and Status

Assign the values from the data attributes to the selected elements and determine the delivery status.

**Original Code:**
```javascript
1-biscuits= 1-root.biscuits,
1-donuts = 1-root.donuts,
1-pancakes = 1-root.pancakes,
1-status = 1-root.status ? Delivered : Pending

2-biscuits= 2-root.biscuits,
2-donuts = 2-root.donuts,
2-pancakes = 2-root.pancakes,
2-status = 2-root.status ? Delivered : Pending

3-biscuits= 3-root.biscuits,
3-donuts = 3-root.donuts,
3-pancakes = 3-root.pancakes,
3-status = 3-root.status ? Delivered : Pending
```

**Fixed Code:**
```javascript
order1Biscuits.textContent = order1Root.dataset.biscuits;
order1Donuts.textContent = order1Root.dataset.donuts;
order1Pancakes.textContent = order1Root.dataset.pancakes;
order1Status.textContent = order1Root.dataset.delivered === 'true' ? 'Delivered' : 'Pending';

order2Biscuits.textContent = order2Root.dataset.biscuits;
order2Donuts.textContent = order2Root.dataset.donuts;
order2Pancakes.textContent = order2Root.dataset.pancakes;
order2Status.textContent = order2Root.dataset.delivered === 'true' ? 'Delivered' : 'Pending';

order3Biscuits.textContent = order3Root.dataset.biscuits;
order3Donuts.textContent = order3Root.dataset.donuts;
order3Pancakes.textContent = order3Root.dataset.pancakes;
order3Status.textContent = order3Root.dataset.delivered === 'true' ? 'Delivered' : 'Pending';
```

## How to Run the Project

1. Clone the repository to your local machine.
2. Open the `index.html` file in your browser.

You should see the order details populated dynamically based on the data attributes.

## Technologies Used

- HTML
- JavaScript

## License

This project is open-source and available under the MIT License.

---

This README provides a comprehensive guide to the project, outlining the purpose, steps taken to complete the challenge, and instructions on how to run the project.
