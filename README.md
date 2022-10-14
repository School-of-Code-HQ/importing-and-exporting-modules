# Workshop - Importing and exporting modules

## 🎯 Workshop objectives

- ☑️ Install Node.js and verify the version
- ☑️ Create, import and export modules using CommonJS
- ☑️ Import JSON data using CommonJS

<br>

## 💼 The Brief

Install Node.js and explore importing and exporting modules by completing the tickets below in order!

<br>

## 🎫 Ticket 1 - Install Node.js and verify the version

Head to the [official Node.js website](https://nodejs.org/en/) and download/install version 18 for your operating system.

Once installed, verify you have the correct version by typing `node --version` in the terminal.

The output returned to your terminal should look similar to the example below:

```
v18.1.0
```

💡 The exact version you're running may be slightly different from the one above, but the main aim is to ensure you are running v18.

If you're running v18.x, move on to the next ticket. ✔️

<br>

## 🎫 Ticket 2 - Working with modules and JSON data

<br>

### 🎫 Ticket 2a - Create a list of bootcampers

Create a `bootcampers.json` file in the root of your project.

Inside `bootcampers.json`, create an array which contains all bootcampers currently in your breakout room (you and your partner).

Bootcampers should be represented as objects with the following properties:

- firstName (String)
- lastName (String)
- age (Number)
- hasPets (Boolean)

Here's an example of what the file should look like:

```json
[
  {
    "firstName": "John",
    "lastName": "Doe",
    "age": 32,
    "hasPets": false
  },
  {
    "firstName": "Jane",
    "lastName": "Doe",
    "age": 25,
    "hasPets": true
  }
]
```

💡 Although similar in appearance, JSON (JavaScript Object Notation) and objects in JavaScript are not the same. All property names in JSON must be strings. You can use [this website](https://jsonformatter.org/) to validate and format your JSON data if needed.

If the data is complete with your and your partner's info and you've checked the JSON is valid, commit your work and move on to the next ticket. ✔️

<br>

### 🎫 Ticket 2b - Create introduce functionality for bootcampers

You have a list of bootcampers.

Now you're going to create a helper function that you can export and use/reuse in your Node.js app later.

Create a `bootcamper.js` file in the root of your project.

Inside `bootcampers.js` create a function named `introduce`.

Make sure to export this function, as you'll use it in a different file.

The `introduce` function will take in a bootcamper object and return a string. E.g.

```js
"Hi, my name is John Doe. I'm 32 years old and I have no pets.";
```

Or if the bootcamper has pets:

```js
"Hi, my name is Jane Doe. I'm 25 years old and I'm a pet owner.";
```

💡 Before you move on to the next ticket, you can test your function works (in this file) by calling it and passing a bootcamper object (created on the fly) as an argument. Study the example below.

```js
console.log(
  introduce({
    firstName: "Barney",
    lastName: "Rubble",
    age: 45,
    hasPets: true,
  })
);

// node bootcamper.js -> Hi, my name is Barney Rubble. I'm 45 years old and I'm a pet owner.
```

Change the `hasPets` value from `true` to `false` and make sure the function still works as you'd expect.

Once you've manually tested your `introduce` function, comment out the function call, commit your work and move on to the next ticket. ✔️

<br>

## 🎫 Ticket 3 - Import/use the module and JSON data

You have a data source - the `bootcampers.json` file.

You have `introduce` functionality located in `bootcamper.js`.

Now it's time to import both and start building out our `app.js` file.

Create an `app.js` file in the root of your project.

Inside `app.js`:

- Import the JSON data from the `bootcampers.json` file and store it in a variable named `bootcamperData`.
- Import the `introduce` function from `bootcamper.js`.

Create appropriately named variables to store each bootcamper in `bootcamperData`. E.g.

```js
const john = bootcamperData[0];
const jane = bootcamperData[1];
```

Now invoke the `introduce` function for each bootcamper and log the result to the console. E.g.

```js
console.log(introduce(john));
console.log(introduce(jane));
```

Finally, run `node app.js` and if you see the correct introductions for each bootcamper in the console - congratulations! Commit your work and move on to the bonus tasks. ✔️

<br>

## 🔥 Bonus tasks

1. Create another function in `bootcamper.js` named `pickRandomBootcamper`. This function should take in your `bootcamperData` as an argument and return one randomly chosen Bootcamper. Import this function in `app.js` and log out a randomly chosen bootcamper to the console.

2. Now In your pairs, ask each other the following interview questions:

- What is Node.js?
- What problems does Node.js solve?
- What are some differences between Node.js and the browser?
- What are modules and why are they useful?

Use your `pickRandomBootcamper` function to determine who goes first, and keep practising until you both are satisfied with how you're articulating your answers.
