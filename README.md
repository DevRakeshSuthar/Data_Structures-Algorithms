# Data Structures  -  Algorithms

# Data Structures

- Data structures are collections of values, the relationships among them, and the functions or operations that can be applied to the data.

- Different data structures excel at different things.  Some are highly specialized, while others (like arrays) are more generally used.

- Working with
map/location data?
Use a graph!

- Need an ordered list with fast inserts/removals at the beginning and end?
Use a linked list!

- Web scraping nested HTML?
Use a tree!

- Need to write a scheduler?
Use a binary heap!


# ES2015
CLASS link : https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes

- What is a class?
A blueprint for creating objects with pre-defined properties and methods.

- Why do we need to learn this?
We're going to implement data structures as classes!

- Class Keyword 

SYNTAX:
  
    class Student {  
           constructor(firstName, lastName){
                   this.firstName = firstName;
                   this.lastName = lastName;
            }
     }
     
 The method to create new objects must be called constructor.
 The class keyword creates a constant, so you can not redefine it.
 Watch out for the syntax as well!
 
 - Creating objects from classes

          class Student {
            constructor(firstName, lastName){
                this.firstName = firstName;
                this.lastName = lastName;
            }
        }

        let firstStudent = new Student("Colt", "Steele");
        let secondStudent = new Student("Blue", "Steele");
        

 - Instance Methods

        class Student {
            constructor(firstName, lastName){
                this.firstName = firstName;
                this.lastName = lastName;
            }
            fullName(){
                return `Your full name is ${this.firstName} ${this.lastName}`;
            }
        }

        let firstStudent = new Student("Colt", "Steele");

        firstStudent.fullName() // "Colt Steele"
