# Part 1 | Fundamentals of Web Development

## Language & Tools of Web Development

- Every website has two parts, a frontend and a backend.
- `Frontend` - User interact / Visual aspects.
- `Backend` - Powers the frontend / store data in database and providing it to the frontend.
- Frontend developers use HTML, CSS & JavaScript to build frontends.
- `HTML` - Hyper Text Markup Language - Markup Language - Building the blocks
- `CSS` - Cascading Style Sheet - Styling Language - Adding styles / asthetics / visual looks
- `JavaScript` - Progrraming Language - Adding functionality to a web page

## How the Web Works

- `URL` - Uniform Resource Locator - A way to locate a resource on the internet.
- `Resources` - Web pages(HTML document), Images, Videos, Fonts.
- `Client` - Browser
- `Server` - Computer or computers that hosts our target website.
- `Client-Server model` - The client requests a service, the server provides that service.
- `HTTP` - Hypertext Transfer Protocol - A language that used by client and server to talk to each other. Not a programming language, it's just a plain textual language for communicating over the internet.
- `HTTPS` - HTTP with encryption, the message exchanged between the client and the server are encrypted.
- `index.html` - Represents the home page of any website.
- `HTTP request` - Client to server message
- `HTTP response` - Server to client message
- HTTP response contains an `HTML document`.
- As the browser reads this HTML document from response, it constructs a `DOM` (Document Object Model).
- `DOM` - This is a model that represents the object or elements in our HTML document.
- `Elements` - All the building blocks of web page, like paragraphs of text, images, links and other stuff.
- As the browser is reading this HTML document that is returned from the server, it discovers references to other resources in this document, like images, fonts and other stuff. Each of these resources has an address or a URL. For each resource, the browser sends a separate HTTP request to the server to fetch that resource. Many of these http requests are sent in parallel so we can see the page as quickly as possible. Once the browser has all the necessary resources, it will render the HTML document.
- `Rendering an HTML document` - displaying it.

---

- `HTTP Response Status Codes` - HTTP response status codes indicate whether a specific HTTP request has been successfully completed. Responses are grouped in five classes:
  1. Informational responses (100 – 199)

  ```
   a. 100: Continue
   b. 101: Switching Protocols
   c. 102: Processing
   d. 103: Early Hints
  ```

  2. Successful responses (200 – 299)

  ```
   a. 200: OK
   b. 201: Created
   c. 202: Accepted
   d. 203: Non-Authoritative Information
   e. 204: No Content
   f. 205: Reset Content
   g. 206: Partial Content
   h. 207: Multi-Status
   i. 208: Already Reported
   j. 226: IM Used
  ```

  3. Redirection messages (300 – 399)

  ```
   a. 300: Multiple Choices
   b. 301: Moved Permanently
   c. 302: Found
   d. 303: See Other
   e. 304: Not Modified
   f. 305: Use Proxy
   g. 306: unused
   h. 307: Temporary Redirect
   i. 308: Permanent Redirect
  ```

  4. Client error responses (400 – 499)

  ```
   a. 400: Bad Request
   b. 401: Unauthorized
   c. 402: Payment Required
   d. 403: Forbidden
   e. 404: Not Found
   f. 405: Method Not Allowed
   g. 406: Not Acceptable
   h. 407: Proxy Authentication Required
   i. 408: Request Timeout
   j. 409: Conflict
   k. 410: Gone
   l. 411: Length Required
   m. 412: Precondition Failed
   n. 413: Content Too Large
   o. 414: URI Too Long
   p. 415: Unsupported Media Type
   q. 416: Range Not Satisfiable
   r. 417: Expectation Failed
   s. 418: I'm a teapot
   t. 421: Misdirected Request
   u. 422: Unprocessable Content
   v. 423: Locked
   w. 424: Failed Dependency
   x. 425: Too Early
   y. 426: Upgrade Required
   z. 428: Precondition Required
   aa. 429: Too Many Requests
   ab. 431: Request Header Fields Too Large
   ac. 451: Unavailable For Legal Reasons
  ```

  5. Server error responses (500 – 599)

  ```
   a. 500: Internal Server Error
   b. 501: Not Implemented
   c. 502: Bad Gateway
   d. 503: Service Unavailable
   e. 504: Gateway Timeout
   f. 505: HTTP Version Not Supported
   g. 506: Variant Also Negotiates
   h. 507: Insufficient Storage
   i. 508: Loop Detected
   j. 510: Not Extended
   k. 511: Network Authentication Required
  ```

## Inspecting HTTP Requests & Responses

- `Chrome Devtools` - Powerful tool used by frontend developers.
- `Headers` - Request & Response

## HTML Very Basics

- `index.html` - Represents the home page of any website.
- `<!doctype html>` - Doctype declaration - Telling the browser this is a HTML 5 document.
- `Element` = `Tag`
- Most HTML elements have an opening and a closing tag.
- `127.0.0.1` - This IP address represents the local/current computer.
- `5500` - Port number our web server is listening. Our web server is waiting for http requests on this port.
- `img` - Self closing element.
- `src`, `alt` - Attribute of `img` element.
- With attributes we can supply additional information about an element.
- `src` - Attribute to specify the path to a image.
- `alt` - Attribute to give the browser some text to display in case the image cannot be displayed.
- `Elements with opening and closing can have child elements.`
- `Self closing elements can't have child elements.`
- `p` - Paragrapg tag - Text element

## CSS Very Basics

- `CSS declaration` - Contains a property and a value.
- `border-radius` - If it's at border radius to a value that is half of the width, we will get a round image.
- `class` - Attribute - Class is short for classification and we can use this attribute to put this element inside a different class or a different category.

## Formatting Code

- Browsers ignore white spaces in HTML and CSS code.

## Validating Web Pages

- `https://validator.w3.org/` - Standard HTML validator - 3 methods (URL, File Upload, Direct Input)
- `https://jigsaw.w3.org/css-validator/` - Standard CSS validator - 3 methods (URL, File Upload, Direct Input)
- If web pages aren't displayed as expected, always start with a quick validation because this can often point you in the right direction.

## The Head Section

- `head` - We use the head section to give browsers and search engines information about the web page.
- `<meta charset="UTF-8" />` - This meta element is used for defining the character set.
- `Character Set` - Computers don't understand characters like ABC, they only understand numbers which are represented in the binary format, zeros and ones, using a character set we can map a character to a numeric value.
- `ASCII` - American Standard Code for Information Interchange - ASCII can only represent the characters in the English language.
- `UTF-8` - This character set can represent almost all characters in the world.
- `Viewport` - Viewport is the visible area of a web page.
- `content="width=device-width, initial-scale=1.0"` - Defining the initial width and zoom factor for the viewport.
- `<meta name="keywords" content="HTML, CSS" />` - Defining keywords on a web page. In the past these keywords were heavily used for search engine optimization.
- `<meta name="description" content="A simple HTML page..." />` - Defining a description for this page. This will appear on Google or other search engines when someone searches for a website. With this meta element, we can give information about a web page.

## Text

- `p` - The p element represents a paragraph.
- `em` - The em element represents stress emphasis of its contents. Browsers display emphasized content in italic. The purpose of the em element is to emphasize content in our HTML document and this helps search engines extract important content in our documents.
- `i` - Previously this element was used to make text italic, but this element is considered deprecated because HTML is not meant for styling. So we don't use the i element to display content as italic. `This element is now used for icons`.
- `strong` - The strong element represents strong importance, seriousness, or urgency for its contents. By default strong elements are displayed as bold.
- `b` - To make text bold. This element is considered deprecated because styling should be done in CSS and not in HTML.
- In HTML we have 6 heading elements, H1, H2, H3, H4, H5 and H6.
- Heading 1 represents the most important heading and heading 6 represents the least important heading. We should use these headings to create a hierarchy, not for styling text. Every web page should have one and only one h1 element. After we use h1, then we should use h2. We should not jump to h4.
- The better we can represent the structure of our document using HTML, the better search engines can read and understand our content.

## Entities

- Some characters are reserved in HTML and to display them we have to use a special notation.
- To solve this problem, we're going to use HTML entities.
- All these entities start with an ampersand(&) and end with a semicolon(;), in between these two characters, we type a few characters that determine the type of the HTML entity.
- HTML Entity List: https://www.w3schools.com/html/html_entities.asp
- Most common used entities:

1. `&lt;` - <
2. `&gt;` - >
3. `&copy;` - ©
4. `&nbsp;` - Non-Breaking Space - If we want to make sure that any two words are always together without breaking for line break, we have to replace the regular space between those two words with a non breaking space which is an HTML entity.

## Hyperlinks

- What is the difference between a link and a hyperlink?
- A link is just an address, a URL, the location of the target page. A hyperlink is the element that the user can click on to navigate to that target page.
- Almost every web page on the Internet has links to other pages or websites. To create these links we use the anchor element.
- `a` - Anchor element - If the a element has an href attribute, then it represents a hyperlink (a hypertext anchor) labeled by its contents.
- `href` - Every anchor element should have an href(hypertext reference) attribute. It basically means a URL or a link. We can use a relative or an absolute URL.
- `Relative URL` - A relative URL starts from the current page.
- `Absolute URL` - An absolute URL start with a / and this represents the root of our project.
- `download` - This attribute instructs browsers to download a URL instead of navigating to it, so the user will be prompted to save it as a local file.
