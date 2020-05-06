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

- Class Methods

      class Student {
          constructor(firstName, lastName){
              this.firstName = firstName;
              this.lastName = lastName;
          }

          fullName(){
              return `Your full name is ${this.firstName} ${this.lastName}`;
          }

          static enrollStudents(...students){
              // maybe send an email here
          }
      }

      let firstStudent = new Student("Colt", "Steele");
      let secondStudent = new Student("Blue", "Steele");

      Student.enrollStudents([firstStudent, secondStudent])
      
 - How we'll be using classes

        class DataStructure(){
            constructor(){
                // what default properties should it have?
            }
            someInstanceMethod(){
                // what should each object created from this class be able to do?
            }
        }
  
    We will be using the constructor and instance methods quite a bit!. 
  We will almost never be using static methods

- One gotcha with `this`

  Inside all of our instance methods and constructor, the keyword `this` refers to the object created from that class (also known as an   instance)


- Classes are blueprints that when created make objects known as instances
- Classes are created with the new keyword
- The constructor function is a special function that gets run when the class is instantiated
- Instance methods can be added to classes similar to methods in objects
- Class methods can be added using the static keyword

# Singly Linked Lists

- What is a linked list?
A data structure that contains a head, tail and length property.

Linked Lists consist of nodes, and each node has a value and a pointer to another node or null.

 - Comparisons with Arrays

                      Lists 

            - Do not have indexes!
            - Connected via nodes with a next pointer
            - Random access is not allowed
            
                      Arrays

            - Indexed in order!
            - Insertion and deletion can be expensive
            - Can quickly be accessed at a specific index
