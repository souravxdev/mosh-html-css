# Interview Questions | Web Development Fundamentals & HTML Basics

## Q1. What is the difference between HTML, CSS, and JavaScript?

**Answer:**

- **HTML (HyperText Markup Language)** is a markup language used to define the structure and content of a web page — headings, paragraphs, images, links, etc.
- **CSS (Cascading Style Sheets)** is a styling language used to control the visual presentation — colors, fonts, layout, spacing, etc.
- **JavaScript** is a programming language used to add interactivity and dynamic behavior — form validation, animations, API calls, etc.

In short: HTML builds the skeleton, CSS dresses it up, and JavaScript makes it move.

---

## Q2. Explain the client-server model and how a web page loads in the browser.

**Answer:**

The **client** (browser) sends an **HTTP request** to a **server** (a computer hosting the website). The server processes the request and sends back an **HTTP response** containing an HTML document. As the browser reads the HTML, it discovers references to other resources like images, CSS files, and scripts — each triggering a separate HTTP request. Many of these requests are sent **in parallel** for faster loading. Once all resources are fetched, the browser **renders** (displays) the page by constructing the **DOM (Document Object Model)** — a tree-like representation of all the elements in the HTML document.

---

## Q3. What is the DOM?

**Answer:**

The **DOM (Document Object Model)** is a programming interface that represents the structure of an HTML document as a tree of objects. When the browser parses an HTML file, it creates the DOM — where each HTML element becomes a node in the tree. This allows JavaScript (and the browser itself) to dynamically access, modify, add, or delete elements and their content on the page.

---

## Q4. What is the difference between HTTP and HTTPS?

**Answer:**

- **HTTP (HyperText Transfer Protocol)** is the protocol used for communication between the client and the server. It is a plain-text protocol.
- **HTTPS (HTTP Secure)** is HTTP with **encryption** (using TLS/SSL). All messages exchanged between the client and server are encrypted, preventing eavesdropping, tampering, and man-in-the-middle attacks.

In modern web development, HTTPS is the standard and is required for features like geolocation, service workers, and for ranking well in search engines.

---

## Q5. What are HTTP status codes? Name the main categories and a few important codes.

**Answer:**

HTTP status codes indicate whether an HTTP request was successfully completed. They are grouped into five categories:

| Range | Category | Example |
|-------|----------|---------|
| 1xx | Informational | 100 Continue |
| 2xx | Success | 200 OK, 201 Created |
| 3xx | Redirection | 301 Moved Permanently, 304 Not Modified |
| 4xx | Client Error | 400 Bad Request, 401 Unauthorized, 403 Forbidden, 404 Not Found |
| 5xx | Server Error | 500 Internal Server Error, 502 Bad Gateway, 503 Service Unavailable |

Most commonly asked in interviews: **200** (success), **301** (permanent redirect), **400** (bad request), **401** (unauthorized), **403** (forbidden), **404** (not found), and **500** (internal server error).

---

## Q6. What is the purpose of the `<!DOCTYPE html>` declaration?

**Answer:**

The `<!DOCTYPE html>` declaration tells the browser that the document is an **HTML5** document. It must be the very first line in an HTML file (before the `<html>` tag). Without it, browsers may render the page in **quirks mode**, where they emulate older, non-standard behavior for backward compatibility — leading to inconsistent rendering across browsers.

---

## Q7. What is the difference between semantic and non-semantic HTML elements? Why does it matter?

**Answer:**

- **Non-semantic elements** like `<div>` and `<span>` tell nothing about their content. They are generic containers.
- **Semantic elements** like `<article>`, `<nav>`, `<header>`, `<footer>`, `<main>`, `<section>`, `<figure>`, `<time>`, and `<mark>` clearly describe the meaning and purpose of their content.

**Why it matters:**

1. **SEO** — Search engines can better understand and index page content.
2. **Accessibility** — Screen readers use semantic elements to help visually impaired users navigate the page.
3. **Maintainability** — Code is easier to read and understand for developers.

---

## Q8. What is the difference between block-level and inline elements? Give examples.

**Answer:**

- **Block-level elements** always start on a new line and take up the full available width. Examples: `<div>`, `<p>`, `<h1>`–`<h6>`, `<ul>`, `<ol>`, `<table>`, `<section>`, `<article>`.
- **Inline elements** do not start on a new line and only take up as much width as their content needs. Examples: `<span>`, `<a>`, `<strong>`, `<em>`, `<img>`, `<mark>`, `<time>`.

This distinction affects layout behavior and is fundamental to understanding CSS box model and page flow.

---

## Q9. What is the difference between the `<head>` and `<body>` sections of an HTML document?

**Answer:**

- The `<head>` section contains **metadata** — information about the page that is not displayed directly. This includes the character set (`<meta charset="UTF-8">`), viewport settings for responsive design, page title (`<title>`), meta descriptions for SEO, keywords, and links to external stylesheets or scripts.
- The `<body>` section contains all the **visible content** that users see and interact with — text, images, links, forms, videos, etc.

---

## Q10. What is the `alt` attribute in the `<img>` tag and why is it important?

**Answer:**

The `alt` attribute provides **alternative text** for an image. It is important for three reasons:

1. **Accessibility** — Screen readers read the alt text aloud, making images accessible to visually impaired users.
2. **SEO** — Search engines use alt text to understand what the image contains, improving page indexing.
3. **Fallback** — If the image fails to load, the alt text is displayed in place of the image.

Every meaningful image should have a descriptive `alt` attribute. Decorative images can use an empty `alt=""` to indicate they should be skipped by screen readers.

---

## Q11. What is the difference between `<strong>` / `<em>` and `<b>` / `<i>` tags?

**Answer:**

- `<strong>` conveys **strong importance or urgency** semantically. Browsers render it as bold by default.
- `<b>` makes text bold visually but carries **no semantic meaning**. It is considered deprecated for emphasis.
- `<em>` conveys **stress emphasis** semantically. Browsers render it as italic by default.
- `<i>` was originally for italic text but is now considered deprecated for emphasis. Its modern use is for **icons** (e.g., Font Awesome icons use `<i>` tags).

Always prefer `<strong>` and `<em>` because they provide meaning to search engines and assistive technologies, not just visual styling.

---

## Q12. What are HTML entities and when do you use them?

**Answer:**

HTML entities are special codes used to display **reserved characters** that have special meaning in HTML. They start with `&` and end with `;`.

Common examples:

| Entity | Character | Use Case |
|--------|-----------|----------|
| `&lt;` | < | Less-than sign (reserved in HTML for tags) |
| `&gt;` | > | Greater-than sign |
| `&amp;` | & | Ampersand (reserved as entity start) |
| `&copy;` | &copy; | Copyright symbol |
| `&nbsp;` | | Non-breaking space — keeps two words together on the same line |

Without entities, characters like `<` and `>` would be interpreted as HTML tags by the browser.

---

## Q13. How do you structure a typical web page using HTML5 semantic elements?

**Answer:**

A well-structured HTML5 page uses semantic elements to define its layout:

```html
<header>         <!-- Introductory content, logo, nav -->
  <nav>          <!-- Navigation links -->
    <ul>...</ul>
  </nav>
</header>

<main>           <!-- Primary content (only one per page) -->
  <section>      <!-- Grouped related content, should have a heading -->
    <h2>...</h2>
    <article>    <!-- Independent, self-contained content -->
      <figure>   <!-- Image with optional caption -->
        <img src="..." alt="..." />
        <figcaption>...</figcaption>
      </figure>
    </article>
  </section>
</main>

<aside>          <!-- Sidebar, ads, related links -->
</aside>

<footer>         <!-- Footer content, secondary nav -->
  <nav>...</nav>
</footer>
```

Key rules: only **one `<main>`** per page, every `<section>` should have a **heading**, and `<article>` represents any independent, self-contained content (blog posts, comments, product cards, etc.).

---

## Q14. What is the difference between a relative URL and an absolute URL?

**Answer:**

- A **relative URL** is defined relative to the current page's location. Example: `href="about.html"` navigates to `about.html` in the same directory.
- An **absolute URL** starts from the root of the website (beginning with `/`) or includes the full domain. Example: `href="/about.html"` or `href="https://example.com/about.html"`.

**When to use which:**
- Use **relative URLs** for internal links within the same project — they are portable and won't break if the domain changes.
- Use **absolute URLs** for linking to external websites or when referencing resources from the site root.

---

## Q15. What is the `<meta>` viewport tag and why is it essential for responsive design?

**Answer:**

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
```

This tag tells the browser how to control the page's dimensions and scaling on different devices:

- `width=device-width` sets the page width to match the device's screen width.
- `initial-scale=1.0` sets the initial zoom level to 100%.

Without this tag, mobile browsers render the page at a desktop-width viewport (typically 980px) and then shrink it down, making text unreadably small. This tag is **essential** for responsive web design and is expected in every modern HTML document.
