# S.O.L.I.D. Clean-Code Principles

The SOLID Principles are thoroughly explained by Martin C. Fowler in his book Clean Architecture. Take a look at the original summary used for this markdown [here][book-summary], but I much rather like the following medium [post][medium-post]

Possibly created by *Robert G. Martin* (?)

## Summary

Make more **Readable**, **Maintainable** and **Testable** code.

The solid principles are meant for Object-Oriented Programming languages.

- **Single Responsibility (SRP)**: Every class should have only one responsibility
- **Open-Closed (OCP)**: Entities should be open for extension but closed for modification
- **Liskov Substitution (LSP)**: Subtype objects should be substitutable for supertype objects
- **Interface Segregation (ISP)**: Clients should not depend upon interfaces that they don't use
- **Dependency Inversion (DIP)**: One Entity should depend upon absractions not concretions

## React + Typescript

[![Demo CountPages alpha][react-ts-video-image]][react-ts-video-link]

The Github repository used in the video can be found [here][react-ts-github]

### Single Responsibility

<!-- markdownlint-disable-next-line -->
<img style="display: block; margin: auto; padding: 2rem;" src="https://miro.medium.com/max/700/1*P3oONz9Da3Tc1w97fMV73Q.png" width="400" />

- Separate the classes into smaller classes.
- Use hooks to manage logic
- Prevent the use of inline components with `.map`, it is better to separate it into its own class
- If there is a useState and a useEffect, it is very possible that you need to create a custom hook for it

### Open-Closed

<!-- markdownlint-disable-next-line -->
<img style="display: block; margin: auto; padding: 2rem;" src="https://miro.medium.com/max/700/1*0MtFBmm6L2WVM04qCJOZPQ.png" width="400" />

- Prevent the creation of reusable components that have to be modified constantly
- Passing `React.ReactNode` components instead of trying to cover every scenario inside reusable components is preferred

### Liskov Substitution

<!-- markdownlint-disable-next-line -->
<img style="display: block; margin: auto; padding: 2rem;" src="https://miro.medium.com/max/700/1*yKk2XKJaCLNlDxQMx1r55Q.png" width="400" />

- When a component extends from another, remember to extend its props as well
- A subtype shouldn't remove props or functionality from their extension to the supertype

### Interface Segregation

<!-- markdownlint-disable-next-line -->
<img style="display: block; margin: auto; padding: 2rem;" src="https://miro.medium.com/max/700/1*2hmyR9L43Vm64MYxj4Y89w.png" width="400" />

< renders

- Components should not depend on props that they don't use
- Use destructuring everywhere possible, to prevent pulling an unnecessary nested prop

### Dependency Inversion

<!-- markdownlint-disable-next-line -->
<img style="display: block; margin: auto; padding: 2rem;" src="https://miro.medium.com/max/700/1*Qk8tDmjQlyvwKxNTfXIo0Q.png" width="400" />

- Make all components standalone with the possibility to extend instead of rewriting the whole component

[book-summary]: https://dzone.com/articles/solid-principles-basic-building-blocks-of-a-clean
[medium-post]: https://medium.com/backticks-tildes/the-s-o-l-i-d-principles-in-pictures-b34ce2f1e898
[react-ts-video-image]: https://img.youtube.com/vi/MSq_DCRxOxw/maxresdefault.jpg
[react-ts-video-link]: https://www.youtube.com/watch?v=MSq_DCRxOxw
[react-ts-github]: https://github.com/ipenywis/react-solid
