                                # Day 2 – CSS Basics 

## 1. What is CSS?

**CSS (Cascading Style Sheets)** is used to style and design HTML elements. It controls the **appearance, layout, colors, spacing, fonts, and overall presentation** of a web page.

### Why is CSS necessary in Full Stack Development?

HTML is mainly used to create the **structure** of a webpage, while CSS is used to make that webpage **visually appealing, readable, responsive, and user-friendly**.

For example:

- HTML → creates a button
- CSS → gives the button color, size, spacing, border, etc.

---

## 2. Ways to Apply CSS

There are three main ways to apply CSS to HTML.

### A. Inline CSS

CSS is written directly inside the `style` attribute of an HTML element.

```html
<p style="color: blue;">Hello World</p>
```

Here, the style is applied only to that particular `<p>` element.

**Use:** Useful for applying a quick style to a specific element, but not preferred for large projects.

---

### B. Internal CSS

CSS is written inside the `<style>` tag in the HTML document, usually inside the `<head>`.

```html
<head>
    <style>
        p {
            color: blue;
        }
    </style>
</head>
```

This CSS can style multiple elements within the same HTML page.

**Use:** Useful when the styling is specific to a single HTML page.

---

### C. External CSS

CSS is written in a separate `.css` file and linked to the HTML file.

**HTML:**

```html
<head>
    <link rel="stylesheet" href="style.css">
</head>
```

**style.css:**

```css
p {
    color: blue;
}
```

### Why is external CSS preferred?

It separates **structure from presentation**, makes the code easier to maintain, and allows the same CSS file to be reused across multiple HTML pages.

---

# 3. How to Link an External CSS File

We use the `<link>` element inside the `<head>` of the HTML document.

```html
<link rel="stylesheet" href="style.css">
```

### Meaning:

- `link` → connects an external resource to the HTML document
- `rel="stylesheet"` → tells the browser that the linked file is a CSS stylesheet
- `href="style.css"` → specifies the location of the CSS file

---

# 4. CSS Color Property

The `color` property is used to change the **text color** of an element.

```css
p {
    color: red;
}
```

It can also use different color formats:

```css
p {
    color: blue;
}
```

```css
p {
    color: #0000ff;
}
```

```css
p {
    color: rgb(0, 0, 255);
}
```

---

# 5. CSS Background-Color Property

The `background-color` property is used to set the **background color** of an element.

```css
div {
    background-color: yellow;
}
```

### Difference:

```css
color: red;
```

→ Changes the **text color**.

```css
background-color: red;
```

→ Changes the **background color**.

---

# 6. What are CSS Selectors?

A **CSS selector** is used to select the HTML element(s) to which CSS styles should be applied.

Example:

```css
p {
    color: blue;
}
```

Here, `p` is the **selector**.

---

# 7. Types of CSS Selectors Learned

## A. Universal Selector

The universal selector is represented by `*`.

It selects **all elements**.

```css
* {
    color: red;
}
```

This applies the style to all elements.

---

## B. Element Selector

An element selector selects HTML elements based on their tag name.

```css
p {
    color: blue;
}
```

This selects all `<p>` elements.

Another example:

```css
h1 {
    color: green;
}
```

This selects all `<h1>` elements.

---

## C. Class Selector

A class selector is represented using `.` followed by the class name.

HTML:

```html
<p class="text">Hello</p>
```

CSS:

```css
.text {
    color: blue;
}
```

A class can be applied to **multiple elements**.

---

## D. ID Selector

An ID selector is represented using `#` followed by the ID name.

HTML:

```html
<p id="heading">Hello</p>
```

CSS:

```css
#heading {
    color: red;
}
```

An ID is generally intended to identify a **unique element** within a page.

---

# 8. What is CSS Specificity?

**CSS specificity determines which CSS rule is applied when multiple rules target the same element and property.**

For the normal selectors learned today, the priority is:

**Inline > ID > Class > Element > Universal**

### Example:

```html
<p id="text" class="para" style="color: red;">
    Hello
</p>
```

```css
#text {
    color: blue;
}

.para {
    color: green;
}

p {
    color: yellow;
}

* {
    color: black;
}
```

The text will be **red** because the inline style has higher priority than these normal selector rules.

### Specificity order:

| Selector | Example | Priority |
|---|---|---|
| Inline | `style="..."` | Highest |
| ID | `#text` | ↓ |
| Class | `.text` | ↓ |
| Element | `p` | ↓ |
| Universal | `*` | Lowest |

**Important:** `!important` can override normal specificity rules, so it should be treated separately rather than simply added to this list.

---

# 9. Key Things I Learned Today

- HTML provides the **structure** of a webpage.
- CSS provides the **style and presentation**.
- CSS can be applied using **inline, internal, or external CSS**.
- External CSS is useful for maintaining reusable and organized styles.
- `color` changes the **text color**.
- `background-color` changes the **background color**.
- CSS selectors determine **which HTML elements are styled**.
- CSS specificity determines **which applicable rule takes precedence** when multiple rules target the same property.