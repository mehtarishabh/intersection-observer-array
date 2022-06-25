# react-intersection-observer

React implementation of the
[Intersection Observer API](https://developer.mozilla.org/en-US/docs/Web/API/Intersection_Observer_API)
to tell you when an element enters or leaves the viewport.


## Features

- 🪝 **Hooks or Component API** - With `useElementOnScreen` it's easier than ever to
  monitor elements


## Installation

Install using [Yarn](https://yarnpkg.com):

```sh
yarn add intersection-observer-array
```

or NPM:

```sh
npm install intersection-observer-array --save
```

## Usage

### `useElementOnScreen` hook

```js
// Use object destructing, so you don't need to remember the exact order
  const [containerRefs, isVisibleIndex] = useElementOnScreen({
    root: null,
    rootMargin: "0px",
    threshold: 0.95
  });

//  Add the container refs on various elements to observe as below 
  ref={el => (containerRefs.current = [...containerRefs.current, el])}
