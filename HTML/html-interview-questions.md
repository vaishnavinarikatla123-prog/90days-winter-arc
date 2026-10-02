# HTML Interview Questions & Answers

> A practical collection of important HTML interview questions covering fundamentals, semantic HTML, forms, accessibility, SEO, DOM, and advanced concepts.

---

# 🟢 Level 1 — HTML Fundamentals

## 1. What is HTML?

### Answer

HTML stands for **HyperText Markup Language**. It is the standard markup language used to structure content on web pages.

HTML defines elements such as headings, paragraphs, links, images, forms, tables, and other content.

Example:

```html
<h1>My Portfolio</h1>
<p>Welcome to my website.</p>
```

---

## 2. Is HTML a programming language?

### Answer

No. HTML is a **markup language**, not a programming language.

HTML is used to define the structure and meaning of content. It does not provide programming concepts such as loops, conditions, or functions.

For example:

* HTML → Structure
* CSS → Styling
* JavaScript → Logic and behavior

---

## 3. What is HTML5?

### Answer

HTML5 is the modern version of HTML. It introduced many improvements for building modern web applications, including semantic elements, multimedia elements, improved form controls, and various browser APIs.

Examples of HTML5 semantic elements:

```html
<header>
<nav>
<main>
<section>
<article>
<footer>
```

HTML5 also introduced elements such as:

```html
<video>
<audio>
```

---

## 4. What is `<!DOCTYPE html>`?

### Answer

`<!DOCTYPE html>` is a **document type declaration** that tells the browser to use standards mode when interpreting the document.

For modern HTML documents, we normally write:

```html
<!DOCTYPE html>
```

It is not an HTML element.

---

## 5. What is an HTML element?

### Answer

An HTML element consists of an opening tag, content, and usually a closing tag.

Example:

```html
<p>Hello World</p>
```

Here:

* `<p>` → opening tag
* `Hello World` → content
* `</p>` → closing tag

Some elements are **void elements** and do not have closing tags.

Example:

```html
<img src="photo.jpg" alt="Profile photo">
```

---

## 6. What is an HTML attribute?

### Answer

An attribute provides additional information about an HTML element.

Example:

```html
<a href="https://example.com">Visit Website</a>
```

Here, `href` is an attribute of the `<a>` element.

Another example:

```html
<img src="photo.jpg" alt="Profile photo">
```

The attributes are:

* `src`
* `alt`

---

## 7. What is the difference between `id` and `class`?

### Answer

Both are used to identify and target HTML elements, but they serve different purposes.

`id` should identify a particular element, while `class` can be shared by multiple elements.

Example:

```html
<h1 id="main-title">My Website</h1>

<p class="text">First paragraph</p>
<p class="text">Second paragraph</p>
```

CSS:

```css
#main-title {
    color: blue;
}

.text {
    font-size: 18px;
}
```

**Interview point:** An `id` is intended to be unique within a document, while the same class can be applied to many elements.

---

# 🟢 Level 2 — Important HTML Concepts

## 8. What are block-level and inline elements?

### Answer

A **block-level element** normally starts on a new line and takes up the available width of its containing block.

Examples:

```html
<div>
<p>
<h1>
<section>
```

An **inline element** normally occupies only the space required by its content.

Examples:

```html
<span>
<a>
<strong>
<em>
```

Example:

```html
<div>Block element</div>
<span>Inline element</span>
<span>Another inline element</span>
```

---

## 9. What is the difference between `<div>` and `<span>`?

### Answer

`<div>` is a generic **block-level container**, while `<span>` is a generic **inline container**.

Example:

```html
<div>
    <h2>Profile</h2>
    <p>This is my profile.</p>
</div>
```

```html
<p>
    My name is <span>Vaishnavi</span>.
</p>
```

Neither element provides semantic meaning by itself.

---

## 10. What is semantic HTML?

### Answer

Semantic HTML means using HTML elements that clearly describe the meaning and purpose of their content.

Examples:

```html
<header>
<nav>
<main>
<section>
<article>
<aside>
<footer>
```

Instead of:

```html
<div class="header"></div>
<div class="navigation"></div>
```

we can use:

```html
<header></header>
<nav></nav>
```

Semantic HTML improves code readability and maintainability and can improve accessibility and help search engines understand page structure.

---

## 11. What is the difference between `<section>` and `<article>`?

### Answer

`<section>` represents a **thematic grouping of related content**.

`<article>` represents **self-contained content that could potentially stand on its own or be distributed independently**.

Example:

```html
<section>
    <h2>Technology News</h2>

    <article>
        <h3>New JavaScript Feature</h3>
        <p>JavaScript introduced a new feature.</p>
    </article>

    <article>
        <h3>React Update</h3>
        <p>React released a new version.</p>
    </article>
</section>
```

Easy way to remember:

**section → group of related content**

**article → independent piece of content**

---

## 12. What is the difference between `<strong>` and `<b>`?

### Answer

`<b>` is mainly used to draw attention to text without adding special importance.

`<strong>` indicates that the text has strong importance.

Example:

```html
<b>Important heading</b>

<strong>Warning: Password is required.</strong>
```

For meaningful importance, prefer `<strong>`.

---

## 13. What is the difference between `<em>` and `<i>`?

### Answer

`<em>` represents emphasis.

`<i>` is used for text that is conventionally offset from normal prose, such as a technical term, foreign phrase, or other stylistically distinct text.

Example:

```html
<p>You <em>must</em> complete this form.</p>

<p>The term <i>HTML</i> stands for HyperText Markup Language.</p>
```

---

# 🟡 Level 3 — Links, Images and Resources

## 14. What is the difference between `href` and `src`?

### Answer

`href` specifies a **reference or destination**, commonly used with `<a>` and `<link>`.

`src` specifies the **source of a resource that an element needs to load**.

Example:

```html
<a href="about.html">About</a>
```

```html
<img src="profile.jpg" alt="Profile">
```

```html
<script src="app.js"></script>
```

Easy way to remember:

**href → reference/destination**

**src → source/load**

---

## 15. What is the difference between `<a>` and `<link>`?

### Answer

`<a>` creates a hyperlink that users can interact with.

```html
<a href="about.html">About Us</a>
```

`<link>` defines a relationship between the current document and an external resource, commonly a stylesheet.

```html
<link rel="stylesheet" href="style.css">
```

---

## 16. Why is the `alt` attribute important for images?

### Answer

The `alt` attribute provides alternative text for an image.

It is important for **accessibility**, especially for users who use screen readers or when an image cannot be displayed.

Example:

```html
<img src="dog.jpg" alt="Brown dog sitting in a park">
```

The alternative text should describe the meaningful content or purpose of the image.

For a purely decorative image, an empty `alt` can be appropriate:

```html
<img src="decoration.png" alt="">
```

---

## 17. What are absolute and relative URLs?

### Answer

An **absolute URL** contains the complete address of a resource.

```html
<a href="https://example.com/about">About</a>
```

A **relative URL** points to a resource relative to the current document.

```html
<a href="about.html">About</a>
```

Relative paths are commonly used for resources within the same website or project.

---

# 🟡 Level 4 — Forms

## 18. What is an HTML form?

### Answer

An HTML form is used to collect information from users and submit that information for processing.

Example:

```html
<form action="/register" method="POST">

    <label for="name">Name:</label>
    <input type="text" id="name" name="name">

    <button type="submit">Register</button>

</form>
```

---

## 19. What are `action` and `method` in a form?

### Answer

`action` specifies where the form data should be submitted.

`method` specifies the HTTP method used to submit the data.

Example:

```html
<form action="/login" method="POST">
```

Here:

* `action="/login"` → destination
* `method="POST"` → HTTP method

---

## 20. What is the difference between GET and POST?

### Answer

GET is generally used to **retrieve data**, while POST is generally used to **submit data that may change server-side state**.

With GET, form data is commonly included in the URL query string.

With POST, form data is sent in the request body.

Example:

```html
<form method="GET">
```

```html
<form method="POST">
```

Important interview point:

**POST is not automatically secure. HTTPS is needed to protect data during transmission.**

---

## 21. Why is the `name` attribute important in forms?

### Answer

The `name` attribute identifies a form control when its value is submitted as form data.

Example:

```html
<input type="text" name="username">
```

When the form is submitted, the server can receive the value using the field name `username`.

---

## 22. What is the difference between `id` and `name` in a form?

### Answer

`id` uniquely identifies an element in the document and is commonly used with labels, CSS, and JavaScript.

`name` identifies the form field when its value is submitted.

Example:

```html
<label for="email">Email</label>

<input
    id="email"
    name="email"
    type="email"
>
```

Here:

* `id="email"` → identifies the element
* `name="email"` → identifies the submitted form field

---

## 23. Why is the `<label>` element important?

### Answer

`<label>` provides a text label for a form control and improves accessibility.

Example:

```html
<label for="email">Email</label>
<input type="email" id="email">
```

The `for` attribute connects the label to the input's `id`.

Clicking the label can also focus or activate the associated control.

---

## 24. What are common HTML input types?

### Answer

HTML provides many input types for different kinds of data.

Common examples:

```html
<input type="text">
<input type="email">
<input type="password">
<input type="number">
<input type="date">
<input type="file">
<input type="checkbox">
<input type="radio">
<input type="submit">
```

Using the appropriate input type improves validation and user experience.

---

## 25. What is the difference between checkbox and radio button?

### Answer

A **checkbox** allows users to select zero, one, or multiple options.

```html
<input type="checkbox" name="skills" value="html">
<input type="checkbox" name="skills" value="css">
```

A **radio button** is generally used when the user should choose one option from a group.

```html
<input type="radio" name="gender" value="male">
<input type="radio" name="gender" value="female">
```

Radio buttons in the same group normally share the same `name`.

---

## 26. What are HTML form validation attributes?

### Answer

HTML provides built-in attributes for basic client-side validation.

Common examples:

```html
<input required>
<input minlength="8">
<input maxlength="20">
<input type="email">
<input min="1">
<input max="100">
<input pattern="[A-Za-z]+">
```

These allow browsers to perform basic validation before submitting the form.

Server-side validation is still necessary because client-side validation can be bypassed.

---

# 🟡 Level 5 — Accessibility

## 27. What is web accessibility?

### Answer

Web accessibility means designing websites so that people with different abilities can use them effectively.

Examples include:

* Using semantic HTML
* Providing meaningful `alt` text
* Using labels for form controls
* Maintaining logical heading structure
* Making interactive elements keyboard accessible

---

## 28. What is ARIA?

### Answer

ARIA stands for **Accessible Rich Internet Applications**.

It provides additional attributes that can communicate roles, states, and properties to assistive technologies when native HTML semantics are not sufficient.

Example:

```html
<button aria-label="Close menu">
    X
</button>
```

A good principle is to use native HTML elements whenever possible before adding ARIA.

---

## 29. Why should we use a `<button>` instead of a clickable `<div>`?

### Answer

A `<button>` is a semantic interactive element with built-in browser behavior and accessibility support.

Example:

```html
<button type="button">Submit</button>
```

Using:

```html
<div onclick="submitForm()">Submit</div>
```

requires extra work for keyboard interaction and accessibility.

Therefore, when something behaves like a button, use `<button>`.

---

# 🟠 Level 6 — SEO & Meta Tags

## 30. What is SEO?

### Answer

SEO stands for **Search Engine Optimization**.

It is the practice of improving a website so that search engines can better understand its content and users can discover relevant pages through search.

HTML contributes to SEO through elements such as:

```html
<title>My Portfolio</title>

<meta
    name="description"
    content="Portfolio of a full-stack developer."
>
```

Semantic HTML, meaningful headings, descriptive links, and appropriate image alternative text also help communicate page structure and content.

---

## 31. What is the `<title>` element?

### Answer

The `<title>` element defines the title of an HTML document.

It is displayed in places such as the browser tab and is also used by search engines as a source for the page title.

Example:

```html
<head>
    <title>Vaishnavi | Full Stack Developer</title>
</head>
```

---

## 32. What is the `<meta>` tag?

### Answer

`<meta>` provides metadata about the HTML document.

Examples:

```html
<meta charset="UTF-8">
```

Specifies the character encoding.

```html
<meta name="viewport"
      content="width=device-width, initial-scale=1.0">
```

Helps control the viewport on mobile devices.

```html
<meta name="description"
      content="My developer portfolio">
```

Provides a description of the page.

---

## 33. Why is the viewport meta tag important?

### Answer

The viewport meta tag controls how a page is displayed in the viewport, particularly on mobile devices.

Common example:

```html
<meta
    name="viewport"
    content="width=device-width, initial-scale=1.0"
>
```

Without appropriate viewport settings, responsive layouts may not behave as expected on mobile devices.

---

# 🟠 Level 7 — DOM & Browser

## 34. What is the DOM?

### Answer

DOM stands for **Document Object Model**.

When a browser loads an HTML document, it creates an object representation of the document called the DOM.

JavaScript can use the DOM to access and modify HTML elements.

Example:

```javascript
document.querySelector("h1").textContent = "Hello";
```

This changes the text of the selected `<h1>` element.

---

## 35. What is the difference between HTML and DOM?

### Answer

HTML is the markup used to describe the structure of a document.

The DOM is the browser's in-memory object representation of that document.

For example:

```html
<h1>Hello</h1>
```

is HTML.

After the browser parses it, the corresponding element becomes part of the DOM tree, which JavaScript can manipulate.

---

## 36. What are `data-*` attributes?

### Answer

`data-*` attributes allow developers to store custom data on HTML elements.

Example:

```html
<button data-user-id="101">
    View Profile
</button>
```

JavaScript can access it using:

```javascript
const button = document.querySelector("button");

console.log(button.dataset.userId);
```

---

# 🔴 Level 8 — Important Advanced Questions

## 37. What is the difference between `async` and `defer`?

### Answer

Both can be used when loading external JavaScript files.

```html
<script src="app.js" async></script>
```

With `async`, the script downloads while HTML is being parsed and executes as soon as it is ready. Execution order between multiple async scripts is not guaranteed.

```html
<script src="app.js" defer></script>
```

With `defer`, the script downloads while HTML is being parsed but executes after HTML parsing is complete. Deferred classic scripts preserve their order relative to each other.

---

## 38. What are void elements?

### Answer

Void elements are HTML elements that cannot have child content and do not have closing tags.

Examples:

```html
<img>
<input>
<br>
<hr>
<meta>
<link>
```

Example:

```html
<img src="photo.jpg" alt="Profile">
```

We do not write:

```html
</img>
```

---

## 39. Can we put a `<div>` inside a `<p>`?

### Answer

No. A `<p>` element's content model is phrasing content, so a `<div>` cannot be a valid child of `<p>`.

For example, this is invalid:

```html
<p>
    Hello
    <div>World</div>
</p>
```

The browser may automatically close the `<p>` before the `<div>` while parsing the HTML.

---

## 40. Can an `<article>` contain a `<section>`?

### Answer

Yes.

These elements can be nested depending on the content structure.

For example:

```html
<article>

    <h1>My Blog Post</h1>

    <section>
        <h2>Introduction</h2>
        <p>Introduction content...</p>
    </section>

    <section>
        <h2>Conclusion</h2>
        <p>Conclusion content...</p>
    </section>

</article>
```

An article can contain multiple sections when the article itself has meaningful thematic subdivisions.

---

## 41. Is using multiple `<h1>` elements allowed?

### Answer

Modern HTML does not technically prohibit multiple `<h1>` elements.

However, the heading structure should clearly represent the document's hierarchy.

A practical approach is to have a clear main page heading and use `<h2>`, `<h3>`, and so on for subsections where appropriate.

The important point is to use headings based on their semantic hierarchy rather than simply choosing them for visual size.

---

## 42. Why shouldn't we use `<div>` for everything?

### Answer

`<div>` is a generic container and does not communicate the meaning of its content.

Using semantic elements such as:

```html
<header>
<nav>
<main>
<section>
<article>
<footer>
```

makes the structure easier for developers, assistive technologies, and search engines to understand.

Use `<div>` when no more meaningful semantic element is appropriate.

---

## 43. What happens when you enter a URL in the browser?

### Answer

At a high level:

1. The browser interprets the URL.
2. It determines where to send the request.
3. A connection is established with the server.
4. The browser sends an HTTP request.
5. The server returns a response, such as HTML.
6. The browser parses the HTML.
7. The browser builds the DOM.
8. It loads required resources such as CSS, JavaScript, and images.
9. CSS is processed and the page is rendered.
10. JavaScript executes and can modify the page.

This process involves networking, parsing, rendering, and JavaScript execution.

---

## 44. What is progressive enhancement?

### Answer

Progressive enhancement is a development approach where we first build a basic functional experience using fundamental web technologies and then add more advanced features for browsers and devices that support them.

For example:

* HTML → basic structure and functionality
* CSS → visual styling
* JavaScript → enhanced interaction

The goal is to ensure the core experience remains usable even when advanced features are unavailable.

---

# 🔴 Level 9 — Practical Interview Questions

## 45. How would you create an accessible login form?

### Answer

I would use semantic form elements, labels associated with their inputs, appropriate input types, and validation.

Example:

```html
<form action="/login" method="POST">

    <div>
        <label for="email">Email</label>
        <input
            type="email"
            id="email"
            name="email"
            required
        >
    </div>

    <div>
        <label for="password">Password</label>
        <input
            type="password"
            id="password"
            name="password"
            required
        >
    </div>

    <button type="submit">
        Login
    </button>

</form>
```

This provides meaningful labels, appropriate input types, keyboard-friendly controls, and basic browser validation.

---

## 46. What is the difference between `<button>` and `<input type="submit">`?

### Answer

Both can submit a form.

```html
<input type="submit" value="Login">
```

and:

```html
<button type="submit">Login</button>
```

The `<button>` element is more flexible because it can contain text and other permitted content, while `<input type="submit">` is a form input control whose displayed text comes from its `value`.

---

## 47. What is the difference between `<section>`, `<article>`, `<aside>`, and `<div>`?

### Answer

* `<section>` → thematic grouping of related content
* `<article>` → self-contained content
* `<aside>` → content related to the surrounding content but separate from the main flow, such as a sidebar
* `<div>` → generic container with no semantic meaning

Example:

```html
<main>

    <section>
        <h2>Latest Articles</h2>

        <article>
            <h3>HTML Interview Questions</h3>
            <p>Important questions for developers.</p>
        </article>
    </section>

    <aside>
        <h2>Related Topics</h2>
        <p>CSS and JavaScript</p>
    </aside>

</main>
```

---

## 48. What is the difference between HTML and XHTML?

### Answer

HTML is the standard markup language used for web documents.

XHTML is HTML expressed using XML's stricter syntax rules.

XHTML documents historically required stricter rules such as properly nested elements and properly closed tags.

Modern web development generally uses HTML rather than XHTML.

---

## 49. What is the difference between semantic and non-semantic elements?

### Answer

Semantic elements communicate the meaning of their content.

Examples:

```html
<header>
<article>
<nav>
<footer>
```

Non-semantic elements do not describe the meaning of their content.

Examples:

```html
<div>
<span>
```

Semantic HTML generally makes a document easier to understand and improves accessibility and maintainability.

---

## 50. What are the most important HTML concepts a full-stack developer should know?

### Answer

A full-stack developer should be comfortable with:

* HTML document structure
* Elements and attributes
* Semantic HTML
* Forms and validation
* GET and POST
* Input types
* Accessibility
* ARIA basics
* Links and images
* `href` vs `src`
* SEO fundamentals
* Meta tags
* Responsive viewport
* DOM basics
* `data-*` attributes
* Script loading with `async` and `defer`
* Tables and lists
* Browser parsing and rendering
* Proper heading hierarchy
* Accessible interactive elements

These concepts form the foundation for working with CSS, JavaScript, React, and frontend frameworks.

---

# 🎯 Quick Interview Revision

Before an interview, make sure you can explain these without looking at notes:

* [ ] What is HTML?
* [ ] HTML vs programming language
* [ ] HTML5
* [ ] `<!DOCTYPE html>`
* [ ] Elements vs attributes
* [ ] `id` vs `class`
* [ ] Block vs inline
* [ ] `div` vs `span`
* [ ] Semantic HTML
* [ ] `section` vs `article`
* [ ] `strong` vs `b`
* [ ] `em` vs `i`
* [ ] `href` vs `src`
* [ ] `<a>` vs `<link>`
* [ ] `alt` attribute
* [ ] Forms
* [ ] `action` and `method`
* [ ] GET vs POST
* [ ] `name` vs `id`
* [ ] `<label>`
* [ ] Input types
* [ ] Checkbox vs radio
* [ ] Form validation
* [ ] Accessibility
* [ ] ARIA
* [ ] SEO
* [ ] `<title>` and `<meta>`
* [ ] Viewport
* [ ] DOM
* [ ] `data-*`
* [ ] `async` vs `defer`
* [ ] Void elements
* [ ] HTML parsing
* [ ] Progressive enhancement

---

# 🚀 My HTML Learning Goal

I am learning HTML not only to build web pages, but to understand the concepts expected from a **full-stack developer and frontend interview candidate**.

**Next:** CSS → JavaScript → React → Full-Stack Development
