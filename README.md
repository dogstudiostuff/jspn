# JSPN Documentation
**Welcome to the JSPN Documentation, this will teach you everything you need to know about JSPN**
##### "JSON" is for storage, "JSPN" is for writing programs in the same format of JSON.
##### If you wanted to know, "JSPN" stands for Javascript Programming Notation.

# Learning JSON Basics
First, JSPN is Powered by JSON.
If you are already familliar with JSON, [Skip this section.](#jspns-basics)\
If you are NOT fammiliar with JSON, here are the basics:
in this section you will learn:
- JSON Basics
- yup thats it\
<br>
You can store keys (like variables) in JSON using a format like this:
```json
{"name":"jimmy"}
```
This will set the key **name** to the value **jimmy**.\
But what if you want to make multiple JSON keys?\
You can easily store multiple keys by adding a second group like this:
```json
{"name":"jimmy", "age":27000}
```
#### (Remember to add a comma inbetween keys.)
You can add a nearly **infinite** amount of keys in json:
```json
{"name":"jimmy", "age":27000, "coolness amount":"super cool", "is god":true, "do you need to give jimmy cookies":true}
```
#### (There is no limit on json keys, i just didnt add so many in that example.)
You can also add JSON **inside of** JSON! (objects)
```json
{
    "shoppinglist":{
        "apples":"1",
        "bananas":"4",
        "oranges":"100"
    },
    "money":{
        "100 dollar bills":26,
        "20 dollar bills":30,
        "pennies":5
    }
}
```
Arrays are also supported in json (even though they dont technically count as json)
```json
    {"jimmy's friends":["bob", "billy", "joe"]}
```
If you understood this, you are now ready to start using JSPN.\
If you dont understand, look it up or something idk.

# JSPN'S basics
## Creating a program Key
Your main code will need to be in a special key, called the ```program``` key.\
First, create a json object:
```json
{}
```
Then, create an object inside with the name ```program```:#
```json
{
    "program":{
        // your code goes here
    }
}
```
If your file looks like the code above, you are ready to start coding with JSPN!
## Simple Programs
Programs are made up of keys. (functions/code in jspn)\
In this section you will learn:
- Basic Functions
- How to run the code\
<br>
First, lets learn basic functions and how to use them.
### Say
Say is the main way for users to see outputed text

You Can use say like this:
```json
{
    "program":{
        "say":"hello world"
    }
}
```
JSPN was meant to run in [Penguinmod](https://penguinmod.com), using say you can make sprites have speech bubbles with text in them.

You can also set how long you want the speech bubble to display using arrays (in seconds). (note: this will also pause the program until the speech bubble dissapears.)
```json
{
    "program":{
        "say":["hello world", 3]
    }
}
```
### An important note
JSPN functions cannot be used twice in a program with the same name.
```json
{
    "program":{
        "say":["i am jimmy", 2], // will be skipped due to them both being the same key 
        "say":["i am bob", 2]
    }
}
```
To fix this, add a number to the end of the second "say", and all says after that.\
This rule applies to all functions.
```json
{
    "program":{
        "say":["i am jimmy", 2], // will work normally
        "say2":["i am bob", 2]
    }
}
```
### Wait
Wait pauses for the specified amount of time.
```json
{
    "program":{
        "say":["Jimmy: lets wait for billy", 2],
        "wait":20, // will wait for 20 seconds before running the next line
        "say2":["Billy: i have arrived", 2]
    }
}
```
### Log
The JSPN version of
```python
print("text")
```
or
```js
console.log("text")
```
You can use it like
```json
{
    "program":{
        "say":["Jimmy: lets wait for billy", 2],
        "log":"waiting for billy...", // will not show for the user if the list JSPN logs is hidden
        "wait":20,
        "log2":"billy has arrived",
        "say2":["Billy: i have arrived", 2],
        "say3":["Billy: wheres joe?", 2],
        "wait2":1,
        "log3":["Joe: HELP, IM STUCK IN THE LOGS"]
    }
}
```
## Functions, Variables, And Loops
### Variables
If you want to store data, use variables!\
Variables can easily store information using the following code
```json
{
    "program":{
        "var":["cool", "1234"],
        "say":{"getvar":"cool"}
    }
}
```




If you need to do a specific task, things might start getting repetitive
```json
{
    "program":{
        "say":"hello",
        "log":"hello said"
    }
}
```