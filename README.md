#Typescript Moc Interview questions and basic code examples

# <h3># What are some benefits of using TypeScript over JavaScript in a project?</h3>

<p>
    Typescript provide us a strong type controlling system that we can control the type of any variable, the most effective thing is that we can find out the type errors before run the code. where javascript cannot prove this facility, we can not get the type errors before run the program. but in typescript it's so easy to find out
</p>

# <h3># What is the purpose of the optional chaining (?.) and nullish coalescing (??) operators in TypeScript, and how do they work? Provide an example for each</h3>

<p>
    The optional chaining (?.) and nullish coalescing (??) are the two operator operators in TypeScript, both of them are looks little bit same but there are different in how they work, <br><br>
    <b>
        <i>Optional Chaining: </i>
    </b>
    we can say it as the short version of if and else, we mostly use it in object to handle the error of <q>Undefined</q> and <q>null</q>.

</p>

```
interface Object {
    props1: string;
    props2?: {
        props3?: string;
        };
}

const Obj1: Object = {
    props1: "value",
};

```
<p>
    In this example we pass the only props1 value but as we are makes the props2 and props3 and the optional so that at the time of creating the obj1 it doesn't give us any error.
</p>
<p>
<br>
    <b>
        <i>nullish coalescing: </i>
    </b> it's looks like optional chaining, but the task is littlebit different, in nullish coalescing it can be set the default value in any value in optional. 
    for r example: <br>

```
const x=null;
const y="something"

const add = x??y;

```
In this example we set the X=null, and try to assign x to the add variable, but as the x=null and we make the condition with y, so the value of y will be assign to the variable of add

</p>

# <h3># How do you handle asynchronous operations in TypeScript, and what are the advantages of using async/await over callbacks or Promises?.</h3>

<p>
TypeScript provides several ways to handle asynchronous operations but async/await is most updated and most advance method for call any function that could wait for a promise.<br>
 for an example: <br>

```
async function loadData() {
  const res = await fetch('data api');
  const data = await response.json();
  return data;
}

```
here in this code the function will gives a promise and wait for the load of data from the data api,
its also helps us to handle the errors by <b>try catch</b> very easily, and the code of the aysnc and await is very clear and easy to understand
</p>

# <h3># How can you use TypeScript's enums, and what are their advantages?.</h3>

<p>
Emum is a type of typescript that define a set of named constants. it make code more readable and understandable compared to numeric constants. Enums are a useful feature for representing fixed sets of options in a type-safe way.
<br>
 for an example: <br>

```
enum value {
  ONE,
  TWO,
  THREE,
  FOUR
}

enum location {
  present = "khulna",
  permanent = "Dumuria"
}

```


</p>

# <h3># Explain the role of type guards in TypeScript and provide an example of a custom type guard.</h3>

<p>
Type guards allow to narrow down the type of a variable within a conditional block in TypeScript. This helps to secure type safety when dealing with union types or values that can have different types.<br><q> typeof, instanceof , in </q> are the build in type guard,
<br>
 for an example: <br>

```

interface User {
  name: string;
  email: string; 
}

const person1:User = {
    name:"name",
    email:"thoha@gmail.com"
}

```
here user is the custom type i made. and for creating the person1 i am use the type of it as User, so the person1 should have all the property of user.
</p>

# <h3># Can you give an example of how to use "readonly" properties in TypeScript?</h3>

<p>
readonly is the keyword that protect any variable for not to change its default value. 
<br>
 for an example: <br>

```

interface User {
  readonly id: number;
  name: string;
  email: string; 
}

const person1:User = {
    id:0001,
    name:"name",
    email:"thoha@gmail.com"
}

```
here we can change the value of any property except the user.id;
if we are trying to change the value of user.id then its shows the error because of readonly.

</p>

# <h3># Explain what a union type is in TypeScript and provide an example of its usage.</h3>

<p>
A union type in TypeScript represents a value that can be one of several types. It allows you to declare that a type could be one of multiple types.
<br>
 for an example: <br>

```

type number = 'one' | 'two' | 'three';
let count: number;
count = 'two';
count = 'one';
count = 'anything else';

```
here the we define a the number with the static values of union of <q>one | two | three</q> when we create an variable named "count" and the type of it would be "number" so the value of count can be 'one' or 'two' or 'three' , except of those its shows the error
</p>
# Typescripy_Moc_interview
