---
id: 587d7dae367417b2b2512b79
title: Extend Constructors to Receive Arguments
challengeType: 1
---

## Description
<section id='description'>
The <code>Bird</code> and <code>Dog</code> constructors from last challenge worked well. However, notice that all <code>Birds</code> that are created with the <code>Bird</code> constructor are automatically named Albert, are blue in color, and have two legs. What if you want birds with different values for name and color? It's possible to change the properties of each bird manually but that would be a lot of work:
<blockquote>let swan = new Bird();<br>swan.name = "Carlos";<br>swan.color = "white";</blockquote>
Suppose you were writing a program to keep track of hundreds or even thousands of different birds in an aviary. It would take a lot of time to create all the birds, then change the properties to different values for every one.
To more easily create different <code>Bird</code> objects, you can design your Bird constructor to accept parameters:
<blockquote>function Bird(name, color) {<br>&nbsp;&nbsp;this.name = name;<br>&nbsp;&nbsp;this.color = color;<br>&nbsp;&nbsp;this.numLegs = 2;<br>}</blockquote>
Then pass in the values as arguments to define each unique bird into the <code>Bird</code> constructor:
<code>let cardinal = new Bird("Bruce", "red");</code>
This gives a new instance of <code>Bird</code> with name and color properties set to Bruce and red, respectively. The <code>numLegs</code> property is still set to 2.
The <code>cardinal</code> has these properties:
<blockquote>cardinal.name // => Bruce<br>cardinal.color // => red<br>cardinal.numLegs // => 2</blockquote>
The constructor is more flexible. It's now possible to define the properties for each <code>Bird</code> at the time it is created, which is one way that JavaScript constructors are so useful. They group objects together based on shared characteristics and behavior and define a blueprint that automates their creation.
</section>

## Instructions
<section id='instructions'>
Create another <code>Dog</code> constructor. This time, set it up to take the parameters <code>name</code> and <code>color</code>, and have the property <code>numLegs</code> fixed at 4. Then create a new <code>Dog</code> saved in a variable <code>terrier</code>. Pass it two strings as arguments for the <code>name</code> and <code>color</code> properties.
</section>

## Tests
<section id='tests'>

```yml
tests:
  - text: <code>Dog</code> should receive an argument for <code>name</code>.
    testString: 'assert((new Dog("Clifford")).name === "Clifford", "<code>Dog</code> should receive an argument for <code>name</code>.");'
  - text: <code>Dog</code> should receive an argument for <code>color</code>.
    testString: 'assert((new Dog("Clifford", "yellow")).color === "yellow", "<code>Dog</code> should receive an argument for <code>color</code>.");'
  - text: <code>Dog</code> should have property <code>numLegs</code> set to 4.
    testString: 'assert((new Dog("Clifford")).numLegs === 4, "<code>Dog</code> should have property <code>numLegs</code> set to 4.");'
  - text: <code>terrier</code> should be created using the <code>Dog</code> constructor.
    testString: 'assert(terrier instanceof Dog, "<code>terrier</code> should be created using the <code>Dog</code> constructor.");'

```

</section>

## Challenge Seed
<section id='challengeSeed'>

<div id='js-seed'>

```js
function Dog() {

}


```

</div>



</section>

## Solution
<section id='solution'>


```js
function Dog (name, color) {
  this.numLegs = 4;
  this.name = name;
  this.color = color;
}

const terrier = new Dog();
```

</section>
