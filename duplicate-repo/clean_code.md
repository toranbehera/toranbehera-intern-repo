## Research and summarize the following clean code principles in clean_code.md:

1. **Simplicity** – Keep code as simple as possible.
It is important to avoid any unnecessary complexity in code and keep them concise to improve readability and maintainability. This can be achieved by focusing on the core problem at hand and breaking it down into small manageable components, with each component having a clearly defined distinct purpose, and reusing components/creating more reusable components where appropriate to avoid duplication. This resultantly helps developers in tracing bugs and writing new code faster. 

For example, let's say that we want to build an ecommerce website. Instead of writing all code monolithically in a single code file, we should instead break the codebase down into several components, and write the code for each component in its respective file. For example, a navbar can be a component, the product cards can be another component, the shopping cart is another component, etc. In this way, if we ever run into an bug, instead of having to look through a single large code file, we will instead have several smaller files that we can look through to narrow down the source of the bug.

2. **Readability** – Code should be easy to understand.
This involves using meaningful variable and function names, following a consistent coding style, and writing comments to provide clarity. For examples, instead of  using vague variable names such as 'x' or 'calc', instead use 'price' and 'calculateTotalPrice', such that if another developer joins the team and starts working with your code, they will immediately understand the purpose of each variable and function. Comments explaining the 'why' rather than 'what' of the code should also be employed to achieve readability. In turn, this reduces the likelihood of introducing bugs by mitigating chances of misunderstanding the code, minimizes complexity, and makes the code quicker to debug.

3. **Maintainability** – Future developers (including you!) should be able to work with the code easily.
Maintainability is achieved by documenting the code by including detailed comments and explanations. Achieving simplicity and modularizing the code also improves maintainability. Moreover, the code should be made flexible and modifiable in a manner that when changes are introduced or the code is extended, it is unlikely to introduced any unintended side effects. The act of achieving code maintainability by changing the code without changing its external behavior is known as refactoring. This helps future developers to easily navigate the codebase and understand its intricacies instead of having to spend time figuring it out themselves, as well as easing the task of debugging any bugs.

4. **Consistency** – Follow style guides and project conventions.
Normally, large projects follow a standard for formatting code, including how to name files, structuring directories, formatting comments, type of casing used, architecture/design/implementation decisions established, etc. New developers must make sure to follow these standards to maintain consistency, so that other team members can understand their code faster, spot errors, and debug unexpected behaviors faster, instead of trying to reinvent the wheel by, for example, developing their own design pattern where there already are existing ones in the codebase that fulfil the desired purpose.

5. **Efficiency** – Write performant, optimized code without premature over-engineering.
Writing efficient code means writing code in a way that it uses a reasonable amount of resources in terms of time and space, preferably minimizing both time taken to run and space used. 

## Find an example of messy code online (or write one yourself) and describe why it's difficult to read.


## Rewrite the code in a cleaner, more structured way.


## Commit and push your changes to GitHub.
