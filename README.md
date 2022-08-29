# 🏗️ Implementing CSS Variables in Style Sheet

- As a developer, I want to manage CSS values that are used in multiple CSS rules in a more efficient manner.

---


## Acceptance Criteria

- It's done when any repeated color values are defined once as a CSS variable.

- It's done when any repeated border radius values are defined once as a CSS variable.

---


## 💡 Hints

- Declare CSS variables, also known as CSS custom properties, on the `:root` pseudo-class.


```
/* Create CSS variables at the root of the document to be used throughout the style sheet */
:root {
  --white: #fff;
  --dark-blue: #13293d;
  --tan: #d8a47f;
  /* You can use it with any value that is repeated throughout the sheet */
  --border-radius: 50px;
  ```

- Use those custom property values instead of using values that are repeated throughout the style sheet such as `#fff`.


```
header {
  padding: 40px;
  text-align: center;
  /* Refer to CSS values by the name of the custom property we assigned it */
  background: var(--dark-blue);
  color: var(--white);
}
```

```
.card > header {
  /* This is the same as `border-radius: 50px 50px 0 0 */
  border-radius: var(--border-radius) var(--border-radius) 0 0;
  padding: 20px;
}
```


