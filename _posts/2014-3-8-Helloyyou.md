---
layout: post
title: Number 8
---

#### Observer example

Before we dive into our real world example, let's give a basic one.

As we've setup our Observable function, we can now invoke our observer, passing in `1` as a value and subscribe to it:

```js
const one$ = new Observable((observer) => {
  observer.next(1);
  observer.complete();
});

one$.subscribe({
  next: (value) => console.log(value) // 1
});
```

We subscribe to the Observable instance, and pass our observer (object literal) into the constructor (which is then assigned to `this.subscribe`).