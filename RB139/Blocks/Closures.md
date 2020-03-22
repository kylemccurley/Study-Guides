# Closures in Ruby
[Link to This Lesson](https://launchschool.com/lessons/c0400a9c/assignments/0a7a9177)
## Guiding Questions:

1. What is a **closure**?
2. What is the **purpose** of a closure?
3. What is a **binding**?
4. What is the **purpose** of a binding?
5. What is the **relationship** between bindings and closures?
6. How is a closure **implemented**?
7. What are the **benefits** of using a closure vs a method?


##### What is a closure?
  - Programming Concept
  - "Closure" because it binds surrounding *artifacts*
  - Build an enclosure around everything so that they can be referenced when the closure is later executed.
  - The combination of code and it's environment ([Lesson Link](https://blog.rebased.pl/2017/11/30/bindings-in-ruby-behind-the-magic-of-blocks.html))
  - Technique of combining methods and variables ([Lesson Link](https://emmanuelhayford.com/ruby-closures-explained/))

##### What is the purpose of a closure?
  - Allow programmers to save a "chunk of code" and execute it at a later time
  - Having an unnamed chunk of code to be passed around can be very handy, especially when passing them into existing methods. 
  - Similar to a method that can be passed around and executed, but doesn't have a name.
     ###### Examples:
       - Blocks
       - Procs
       - Lambdas
  
##### What is a binding?
  > **Ruby Docs Definition:** Encapsulate execution context at some particular place in code; retaining this context for later use.

  - The surrounding artifacts for a 'chunk of code'.
  - Surrounding context/environment.
  
    ###### Example: 
      - __Name Binding:__ Variable Assignment, Binding a name to a memory reference, like a variable name to it's value.

      ```ruby
      name = 'Carl' # Binding 'Carl' to a memory reference: name
      ```

##### What is the purpose of a binding
  - Capture local scope in order to be able to pass it around.
  - Ruby keeps track of it's lexical scope through bindings.
  > ###### Proc Instantiation:
  > Whenever a proc is instantiated, a binding 
  > is created which inherits references
  > to the local variables in the context the block was created. Since
  > the proc inherits the REFERENCES to the local variable, you can perform
  > variable reassignment within the context of the Proc.

##### What is the relationship between bindings and closures?
- Closures must keep track of its _binding_ in order to **execute properly**.
  - Keeping track of its variables, methods, (artifacts)

##### How is a closure implemented:
    - Blocks
    - Procs
    - Lambdas

  - Closures, or chunks of code, can be implemented by passing the 'chunk of code' into a method/object, where the block is executed under the context of that method/object.

##### Benefits of a closure vs a method?
   - Closures are also technically methods. 
   - Closures are unnamed, but the key difference is that closures capture **state** upon their creation.
  
