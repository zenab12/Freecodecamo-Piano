# [Live Demo]( https://zenab12.github.io/Freecodecamo-Piano/)

![Screen Shot 2022-07-22 at 20 22 35](https://user-images.githubusercontent.com/78083890/180500688-eab166ec-f973-46b4-88ec-ba92e4278e28.png)


## tips i learned from mahratech :

<aside>
🔑 pseudo elements as `::after ,::before`

[https://css-tricks.com/the-shapes-of-css/](https://css-tricks.com/the-shapes-of-css/)

in ::after ,::before we can use in content attribute counter value as this :

for example Create a counter ("my-sec-counter") and increase it by one for each occurrence of the <h2> selector:

```css
body {
   /* Set "section" to 0 */
  counter-reset: section;
}

h1 {
   /* Set "subsection" to 0 */
  counter-reset: subsection;
}

h1::before {
  /* Increment "section" by 1 */
  counter-increment: section;
  content: "Section " counter(section) ": ";
}

h2::before {
  /* Increment "subsection" by 1 */
  counter-increment: subsection;
  content: counter(section) "." counter(subsection) " ";
}

h2::before {
  /* Decrement "my-sec-counter" by 1 */
  counter-increment: my-sec-counter -1;
  content: "Section " counter(my-sec-counter) ". ";
}
```

or we can use `attr(href as example)` as value for content attribute or `open-quote` or `close-quote` 

