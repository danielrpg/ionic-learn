**IONICv2 FRAMEWORK**

This is to reference for to lear more about IONICv2 Framework and mobile developement.

**TypeScript**

Firstly we need to learn something of TypeScript

*Comments*

```
// this is a single line comment 
/* this is a multi line comment.Multiline comments starts with slash-star and ends with star-slash */

```

*Declaration*

```
let name = "TypeScript";
name = "nodejs";
const pi = 3.141;
```

*Basic Types*

Boolean

```
let isDone: boolean = false;
```

Number

```
let loc: number = 600;
```

String 

```
let name = "typescript";
name = "java";
```
- Multiline String
```
let subject: string = `TypeScript is awesome.
Google adapting a language developed at Microsoft, shows how awesome it is.`
```
- Template Strings with embededd expressions

```
let customerName: string = `Harry`;
let invoiceAmount: number = 1500;
let email: string = `Dear ${customerName},
Invoice for ${invoiceAmount} is enclosed.
Thank you.`
```

Any

```
let userInput: any;
userInput = "any user input"
userInput = 45.3;
userInput = false;
```

Void

```
function showWarning(): void {
 alert("This is a warning")
}
```

Type Assertions

- Angle brackets

```
let name: any ="Bruce Wills";
let nameLen: number = (<string>name).length;
```

- Other form

```
let name : any = 'Bruce Wills';
let nameLen: number = (name as string).length;
```

*Collections*

- Array
```
 let cities: string[] = ['delhi','chennai','munbai'];
 let cities: Array<string> = ['delhi','chennai','munbai'];
```

- Tuple
```
let yearBorn: [string, number];
yearBorn = ['julia roberts', 1967];
```
- Enum

```
enum Day {Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday};
let firstDay: Day = Day.Sunday;
enum Direction {North = 2, South = 4, East = 6, West = 8};
enum Direction {North = 2, South = 4, East, West}; // East = 5; West = 6
```

- Union
```
let path: string[] | string;
path = ['/home', '/home/dropbox'];
path = '/home';
```

*Operators*

- Arithmetic

```
let a = 5;
let b = 4;
let c = 0;
c = a + b; //c = 9
c = a - b; //c = 1
c = a * b; //c = 20
c = a / b; //c = 1.25
c = a % b; //c = 1
c = a++; //c = 6
c = b--; //c = 3let a = 5;
let b = 4;
let c = 0;
c = a + b; //c = 9
c = a - b; //c = 1
c = a * b; //c = 20
c = a / b; //c = 1.25
c = a % b; //c = 1
c = a++; //c = 6
c = b--; //c = 3
```

- Comparision

```
let a = 5;
let b = 4;
let c = false;
let d = 5;
c = a == b; //c = false
c = a === d; //c = true
c = a != b; //c = true
c = a > b; //c = true
c = a < b; //c = false
c = a >= b; //c = true
c = a <= b; //c = false 
```

- Logical

```
&& is a logical AND operator. If both operands are true, then the condition becomes true.
|| is a logical OR operator. If one of the two operands is true, then the condition becomes true.
! is a logical NOT operator. It reverses the state of the operand.
```

*Control flow*

- if..else

```
if (boolean-expression) {
 statement1
}
else {
 statement2
}
```
- Ternary
```
boolean-expression ? statement1 : statement2
let speed = 80;
let isFast = speed > 55 ? true : false
```

- for loop

```
var sum = 0;
for (var i = 0; i <= 1000; i++){
 if (i % 3 == 0 || i % 5 == 0){
 sum = sum + i;
 }
}
console.log(sum);
```
- for-of loop

```
let cities: string[] = ['delhi', 'chennai', 'mumbai'];
for (let city of cities) {
 alert(city);
}
```

- switch

```
let animal = 'dog';
switch (animal){
    case 'dog':
        alert('dog');
    break;
    case 'cat':
        alert('cat');
    break;
    default:
        alert('none?')
}
```
- while

```
let sum = 0;
while (sum <= 5) {
 sum = sum + 1;
}
```
- do...while

```
let sum = 0;
do {
 sum = sum + 1;
} while (sum <= 4)
```

*Functions*

```
function squareOf(i: number): number {
 return i * i;
};
```
or

```
let sqr1 = function sqr (i: number) : number {
 return i * i;
}
```

```
// anonymous function
let sqr2 = function (i: number) : number {
 return i * i;
}
// alternate syntax for anonymous function using =>
let sqr3 = (i: number) : number => { return i * i;}
// return type can be inferred
let sqr4 = (i: number) => { return i * i;}
// return is optional in one line 
let sqr5 = (i: number) => i * i
```
- Optional and Default Values

```
function getFullName(firstName: string, lastName?: string) : string {
 if (lastName) {
 return firstName + " " + lastName;
 } else {
 return firstName
 }
}
```
Also mention default values for parameters

```
function getFullName(firstName: string, lastName: string = "") : string {
 return (firstName + " " + lastName).trim();
}
```

*Classes*

```
class Book {
 name: string;
 purchasedYear: number;
 constructor (name: string, purchasedYear: number){
 this.name = name;
 this.purchasedYear = purchasedYear;
 }
}
let Book1 = new Book('7 habits', 2005)
```

*Inheritance*

```
class Asset {
 name: string;
 purchasedYear: number;
 constructor (name: string, purchasedYear: number){
 this.name = name;
 this.purchasedYear = purchasedYear;
 }
}
class Book extends Asset {
 constructor (name: string, purchasedYear: number) {
 super(name, purchasedYear)
 }
}
let book1 = new Book('7-habits', 2013);
```
*Interfaces*

```
interface iAsset {
 name: string;
 purchasedYear: number;
 age: () => number;
}
class Book implements iAsset{
    name: string;
    purchasedYear: number;
    constructor (name: string, purchasedYear: number){
    this.name = name;
    this.purchasedYear = purchasedYear;
    }
    age() {
        return (2016 - this.purchasedYear);
    }
}
let Book1 = new Book('7 habits', 2005)
alert(Book1.age)
```