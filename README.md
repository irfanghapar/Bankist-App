# Bankist App Tutorial: Interactive Banking Application

Welcome to the Bankist App Tutorial! 🎉 In this tutorial, you'll learn how to interact with the Bankist application, a simulated banking application built with JavaScript. Let's dive into understanding the user flow, requirements, and how you can clone and run this application.

## User Flow

1. **Login**: Users will start by logging into the application using their username and PIN.
2. **View Account**: Once logged in, users can view their account details, including balance and transaction history.
3. **Transfer Money**: Users can transfer money to other accounts.
4. **Request Loan**: Users can request a loan if eligible.
5. **Close Account**: Users can close their account.

## Requirements

To interact with the Bankist application, you'll need:

- A web browser such as Google Chrome, Mozilla Firefox, or Safari.
- Basic knowledge of HTML, CSS, and JavaScript.
- A code editor like Visual Studio Code, Sublime Text, or Atom.

## Cloning the Application

To clone the Bankist application repository, follow these steps:

1. Open your terminal or command prompt.
2. Navigate to the directory where you want to clone the repository.
3. Run the following command:

```bash
git clone https://github.com/yourusername/bankist-app.git
```

Replace `yourusername` with your GitHub username.

4. Once the cloning process is complete, navigate into the `bankist-app` directory:

```bash
cd bankist-app
```

5. Open the project in your code editor to explore the files and make modifications.

## Exploring the Code

Let's take a closer look at some key parts of the Bankist application code:

### 1. Login Functionality

The login functionality allows users to log into the application using their username and PIN.

```javascript
btnLogin.addEventListener("click", function (e) {
  // Handle login functionality
});
```

### 2. Displaying Account Details

Once logged in, the application displays the user's account details, including balance and transaction history.

```javascript
const updateUI = function (acc) {
  // Display movements
  displayMovements(acc);

  // Display balance
  calcDisplayBalance(acc);

  // Display summary
  calcDisplaySummary(acc);
};
```

### 3. Transferring Money

Users can transfer money to other accounts by entering the recipient's username and the amount to transfer.

```javascript
btnTransfer.addEventListener("click", function (e) {
  // Handle money transfer functionality
});
```

### 4. Requesting Loan

Users can request a loan if they meet the eligibility criteria and enter the desired loan amount.

```javascript
btnLoan.addEventListener("click", function (e) {
  // Handle loan request functionality
});
```

### 5. Closing Account

Users have the option to close their account by entering their username and PIN.

```javascript
btnClose.addEventListener("click", function (e) {
  // Handle account closure functionality
});
```

## Running the Application

To run the Bankist application locally, follow these steps:

1. Open the `index.html` file in your web browser.
2. Interact with the application by logging in, viewing your account details, transferring money, requesting a loan, and closing your account.


## Features and Techniques Used

### 1. Map, Filter, and Reduce

- **Map**: Used to transform each element of an array to another value, for example, formatting movement dates.
- **Filter**: Used to filter elements of an array based on certain criteria, for example, filtering deposits and withdrawals.
- **Reduce**: Used to accumulate values of an array into a single value, for example, calculating account balance and summary.

```javascript
const incomes = acc.movements
  .filter((mov) => mov > 0)
  .reduce((acc, mov) => acc + mov, 0);
```

### 2. Chaining Methods

Multiple array methods like `filter`, `map`, and `reduce` are often chained together to perform complex operations on arrays in a concise and readable manner.

```javascript
const incomes = acc.movements
  .filter((mov) => mov > 0)
  .map((deposit) => deposit * acc.interestRate / 100)
  .reduce((acc, int) => acc + int, 0);
```

### 3. Find Method

The `find` method is used to search for an element in an array based on a condition.

```javascript
currentAccount = accounts.find(
  (acc) => acc.username === inputLoginUsername.value
);
```

### 4. Implementing Login

The application allows users to log in using their username and PIN. Once logged in, the user can access their account functionalities.

```javascript
btnLogin.addEventListener("click", function (e) {
  // Handle login functionality
});
```

### 5. Some and Every Methods

These methods are used to check whether at least one element or all elements of an array satisfy a given condition.

```javascript
const isEven = n => n % 2 === 0;
console.log(isEven(8)); // true
console.log(isEven(23)); // false
```

### 6. Flat and FlatMap

These methods are used to flatten nested arrays into a single-level array.

### 7. Sorting Arrays

The `sort` method is used to sort arrays based on certain criteria.

```javascript
movs.sort((a, b) => a - b); // Sort movements in ascending order
```

### 8. Creating Dates

JavaScript's `Date` object is used to work with dates, including creating, formatting, and manipulating dates.

### 9. Internationalizing Dates

The `Intl.DateTimeFormat` object is used to format dates according to the user's locale preferences.

```javascript
const formattedDate = new Intl.DateTimeFormat(locale).format(date);
```

### 10. setTimeout

The `setTimeout` function is used to execute a function after a specified delay.

```javascript
const pizzaTimer = setTimeout(
  (ing1, ing2) => console.log(`Here is your pizza with ${ing1} and ${ing2} 🍕`),
  3000,
  ...ingredients
);
```

## Conclusion

The Bankist App demonstrates the usage of various JavaScript features and techniques to create a functional banking application. By understanding and implementing these concepts, you can build robust and interactive web applications. Happy coding! 🚀