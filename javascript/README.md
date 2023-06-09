# AI Function

Generate realtime AI Functions!

## Installation

To install AI Function for node.js, run:

```bash
npm install aifunction
```

## Usage

```
aiFunction(name <string>, description <string>, installPackages <bool>)
```

- name: The name of the function. Ex: "time", "current_president"
- description: A description of the function. Ex: "Returns the current time", "Returns the date in the format YYYY-MM-DD"
- installPackages: Whether or not to install the required packages for the function. Ex: "time" requires the "datetime" package, so it will be installed if this is set to true.

To use AIFunction, you must have an OpenAI API key.

Firstly, add a .env file to your project, and add the following:

```
OPENAI_API_KEY="key_here"
```

Then, import the aiFunction function:

```javascript
const aiFunction = require("aifunction");
```

Now, you can use the aiFunction function to generate AI Functions!

```javascript
(async () => {
  console.log(await aiFunction("time", "Return the current time"));
})();
// --> 12:00:00
```

## What is an AI Function?

Let's say you want to write a function to get the current time in javascript. All you have to do is:

```javascript
(async () => {
  console.log(await aiFunction("time", "Return the current time"));
})();
// --> 12:00:00
```

## How does it work?

AI function uses OpenAI's GPT model to generate the code for the function. It then runs the code and returns the output. If specified, it will also install the required packages for the code.

## Security

AI Functions are not very secure, as they run code without any user testing, and can be used to run malicious code.
