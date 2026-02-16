# 📘 HTML Complete Notes & Reference Guide

> **Based on classroom notes (Part 1 & Part 2) + Practice programs from [rahulthakare04/html](https://github.com/rahulthakare04/html) (ex1.html → ex37.html)**

---

## 📑 Table of Contents

1. [What is HTML?](#1-what-is-html)
2. [HTML Versions](#2-html-versions)
3. [HTML Structure](#3-html-structure)
4. [Types of Tags](#4-types-of-tags)
5. [Head Section Tags](#5-head-section-tags)
6. [Text & Formatting Tags](#6-text--formatting-tags)
7. [HTML Attributes](#7-html-attributes)
8. [Images](#8-images-img-tag)
9. [Hyperlinks](#9-hyperlinks-a-tag)
10. [List Tags](#10-list-tags)
11. [Table Tags](#11-table-tags)
12. [Fieldset & Legend](#12-fieldset--legend)
13. [Div Tag](#13-div-tag)
14. [Form & Input Elements](#14-form--input-elements)
15. [Dropdown, Listbox & Optgroup](#15-dropdown-listbox--optgroup)
16. [Textarea & Progress Bar](#16-textarea--progress-bar)
17. [Label & Datalist](#17-label--datalist)
18. [HTML5 Semantic Tags](#18-html5-semantic-tags)
19. [Audio & Video Tags](#19-audio--video-tags)
20. [iframe & Map Tag](#20-iframe--map-tag)
21. [Meta & Base Tags](#21-meta--base-tag)
22. [Marquee Tag](#22-marquee-tag)
23. [HTML Entities](#23-html-entities)
24. [Comments](#24-comments)
25. [Practice Programs Index](#25-practice-programs-index)
26. [Quick Reference Cheat Sheet](#26-quick-reference-cheat-sheet)

---

## 1. What is HTML?

HTML stands for **HyperText Markup Language**.

| Term | Meaning |
|------|---------|
| **Hyper** | Text that can be transferred from internet server to internet client |
| **Markup** | Syntax in the form of tags that tell a browser how to structure & display content |
| **Language** | Interface between web developer and web browser |

**Key Facts:**
- Developed by **Tim Berners-Lee**, released in **1993**, maintained by **W3C**.
- HTML is **not a programming language** — it is a **markup language**.
- Used to create **static web pages** (pages that always show the same content).
- **Client-side technology** — HTML code runs in the browser, not on the server.
- HTML is **case-insensitive** (you can write in UPPER or lower case).
- HTML is **error-free** — browsers silently ignore unknown tags.
- HTML is **interpreter-based** — the browser interprets HTML line by line.
- File extensions: `.html` or `.htm`
- No software installation required — just a text editor and a browser.
- Supported by all browsers: Chrome, Firefox, Safari, Edge, Opera, etc.

---

## 2. HTML Versions

| Version | Specification | Release Date |
|---------|--------------|--------------|
| 1.0 | HTML 1.0 | Dec 1993 / 1994 |
| 2.0 | HTML 2.0 | 24 Nov 1995 |
| 3.2 | W3C: HTML 3.2 | 14 Jan 1997 |
| 4.0 | W3C: HTML 4.0 | 24 Apr 1998 |
| 4.1 | W3C: HTML 4.1 | 24 Dec 1999 |
| **5.0** | WHATWG | **28 Oct 2014** (Advanced Markup for Mobiles) |
| 5.1 | W3C: HTML 5.1 | Nov 2016 (Small Electronic Devices) |
| 5.2 | W3C: HTML 5.2 | 14 Dec 2017 |

---

## 3. HTML Structure

Every HTML page follows this structure (recommended by W3C):

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <!-- Page settings, title, links, meta, style, script -->
    <title>Page Title</title>
  </head>
  <body>
    <!-- Visible page content goes here -->
  </body>
</html>
```

### 🔹 Versioning Section
Tells the browser which HTML version is being used.
```html
<!DOCTYPE html>          <!-- HTML5 (current standard) -->
```

### 🔹 `<html>` Tag
Represents the start and end of an HTML document. Contains `<head>` and `<body>` as children.

### 🔹 `<head>` Tag
- **Non-content section** — not visible in the browser output.
- Contains: `<title>`, `<link>`, `<meta>`, `<style>`, `<script>`, `<base>` (6 sub-tags).
- Used for page settings, icons, metadata, CSS, JavaScript links.

### 🔹 `<body>` Tag
- **Content section** — everything visible on the webpage.
- Contains: `<p>`, `<h1>`–`<h6>`, `<img>`, `<table>`, `<div>`, `<a>`, `<form>`, `<audio>`, `<video>`, `<input>`, `<button>`, etc.

---

## 4. Types of Tags

### Paired Tags (Body-full Tags)
Have an opening tag and a closing tag.
```html
<html> ... </html>
<head> ... </head>
<body> ... </body>
<p> ... </p>
<h1> ... </h1>
```

### Unpaired / Self-Closing Tags (Body-less / Void Tags)
Contain only an opening tag. Do not return any value.
```html
<br/>     <!-- Line break -->
<img/>    <!-- Image -->
<input/>  <!-- Form input -->
<hr>      <!-- Horizontal rule -->
<link>    <!-- External resource link -->
<meta>    <!-- Metadata -->
```

### Translators (How code gets executed)

| Translator | Languages |
|-----------|-----------|
| Compiler | C, C++, Java, .NET |
| **Interpreter** | **HTML, JavaScript, Oracle** |
| Assembler | VLSI, ALGOL, MATLAB |

> HTML uses an **interpreter** — the browser translates and executes code **line by line**.

---

## 5. Head Section Tags

### `<title>` Tag
Sets the title of a web page (shown in browser tab).
```html
<title>My Web Page</title>
```

### `<link>` Tag
Links external resources — favicon icons, CSS stylesheets.
```html
<link rel="icon" href="logo.png" />
<link rel="stylesheet" href="style.css" />
```
Supported image formats: `.jpg`, `.bmp`, `.png`, `.gif`, `.ico`, `.svg`, `.webp`

### `<meta>` Tag
Provides metadata about the page to browsers and search engines.
```html
<!-- Keywords for search engines -->
<meta name="keywords" content="HTML, CSS, JavaScript">

<!-- Page description -->
<meta name="description" content="HTML Tutorial for Beginners">

<!-- Author -->
<meta name="author" content="Rahul Thakare">

<!-- Auto refresh page every 45 seconds -->
<meta http-equiv="refresh" content="45">

<!-- Redirect after 5 seconds -->
<meta http-equiv="refresh" content="5; url=https://example.com">

<!-- Responsive viewport (essential for mobile) -->
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

### `<base>` Tag
Sets a base URL for all relative links in the document. Only one `<base>` allowed per document. Unpaired tag.
```html
<base href="https://www.example.com/" target="_blank"/>
```

---

## 6. Text & Formatting Tags

### Heading Tags (`<h1>` to `<h6>`)
Display text in heading format. `h1` is largest, `h6` is smallest. All are **paired** and **block-level** elements.
```html
<h1>Heading 1 (Largest)</h1>
<h2>Heading 2</h2>
<h3>Heading 3</h3>
<h4>Heading 4</h4>
<h5>Heading 5</h5>
<h6>Heading 6 (Smallest)</h6>
```

### `<p>` Tag — Paragraph
Displays a block of text. Paired tag, block-level element.
> ⚠️ Browser ignores extra spaces and Enter keys. Use `&nbsp;` for space, `<br>` for line breaks.
```html
<p>This is a paragraph of text.</p>
```

### `<br>` Tag — Line Break
Moves cursor to the next line. Unpaired tag.
```html
Line 1<br/>
Line 2
```

### `<hr>` Tag — Horizontal Rule
Draws a horizontal dividing line. Unpaired tag.
```html
<hr/>
```

### `<pre>` Tag — Pre-formatted Text
Prints text exactly as typed — preserves spaces, tabs, and line breaks. Paired, block-level.
```html
<pre>
  Name:  Rahul
  Age:   20
</pre>
```

### Formatting Tags (All Paired & Inline)

| Tag | Purpose | Syntax |
|-----|---------|--------|
| `<b>` / `<strong>` | Bold text | `<b>text</b>` |
| `<i>` / `<em>` | Italic (inclined) text | `<i>text</i>` |
| `<u>` | Underline text | `<u>text</u>` |
| `<strike>` / `<s>` / `<del>` | Strikethrough (line through middle) | `<strike>text</strike>` |
| `<sup>` | Superscript (above baseline) | `H<sup>2</sup>O` |
| `<sub>` | Subscript (below baseline) | `H<sub>2</sub>O` |
| `<mark>` | Highlight text (yellow background) | `<mark>text</mark>` |
| `<small>` | Smaller text size | `<small>text</small>` |
| `<ins>` | Inserted/underlined text | `<ins>text</ins>` |
| `<span>` | Inline container for styling | `<span>text</span>` |

**`<span>` Tag** — Used for small textual data (error messages, mandatory symbols). Inline tag. Used with CSS to highlight specific words.

---

## 7. HTML Attributes

Attributes provide extra information/settings for HTML tags. They are placed inside the opening tag.

```html
<tagname attribute="value" attribute2='value2'>
```

> **Note:** Attribute values can be enclosed in `" "`, `' '`, or without quotes.

### General Attributes (Common to most tags)
`class`, `id`, `name`, `style`, `align`, `action`, `method`, `href`, `src`, `target`, `width`, `height`, `alt`, `title`, `lang`, `min`, `max`, `step`, `maxlength`, `type`, `checked`, `selected`, `value`, `readonly`, `placeholder`

### Event Attributes (Trigger JavaScript)
`onclick`, `ondblclick`, `onfocus`, `onblur`, `onkeypress`, `onkeyup`, `onkeydown`, `onsubmit`, `onchange`, `oninput`, `onreset`, `onselect`, `onmousemove`, `onmouseout`, `onmouseover`, `onwheel`, `onload`

---

## 8. Images (`<img>` Tag)

Displays images on the web page. **Unpaired, inline** element.

**Supported formats:** `.jpg`, `.jpeg`, `.png`, `.bmp`, `.gif`, `.tif`, `.webp`, `.svg`, `.jfif`

```html
<img src="image.jpg" width="300" height="200" alt="Description" title="Tooltip text" />
```

| Attribute | Description |
|-----------|-------------|
| `src` | Path/URL of the image |
| `width` | Width in pixels |
| `height` | Height in pixels |
| `alt` | Alternative text shown if image fails to load |
| `title` | Tooltip text shown on mouse hover |

> 💡 **Best Practice:** Place all images inside a root folder or a subfolder named `images/`.

---

## 9. Hyperlinks (`<a>` Tag)

The `<a>` (anchor) tag creates hyperlinks to navigate between pages. **Paired, inline** element.

Default browser style: **Blue color + Underline + Hand cursor**

```html
<!-- Text link -->
<a href="https://www.google.com" target="_blank">Visit Google</a>

<!-- Image link -->
<a href="page2.html"><img src="logo.png" /></a>

<!-- Bookmark (within same page) -->
<a href="#section1">Go to Section 1</a>
<h2 id="section1">Section 1</h2>

<!-- Email link -->
<a href="mailto:example@email.com">Send Email</a>
```

### Types of Links
- **External links** — Navigate to other websites
- **Internal links** — Navigate within the same website

### `href` Attribute Values

| Value | Meaning |
|-------|---------|
| `"https://www.abc.com"` | External URL |
| `""` | Self-calling (current page) |
| `"."` | Home directory of web application |
| `"#id"` | Bookmark — jumps within same page |
| `"filename.html"` | Internal page |

### `target` Attribute Values

| Value | Meaning |
|-------|---------|
| `_blank` | Opens in new tab/window |
| `_self` | Opens in current tab (default) |
| `_parent` | Opens in parent frame |
| `_top` | Opens in full body of window |
| `framename` | Opens in specified frame |

---

## 10. List Tags

### Ordered List (`<ol>`) — Numbered List
Displays items with numbering. Paired, block-level.

```html
<ol type="1" start="1">
  <li>Item One</li>
  <li>Item Two</li>
  <li value="5">Item Five (restart)</li>
</ol>
```

| `type` Value | Display |
|-------------|---------|
| `1` | 1, 2, 3 (default) |
| `A` | A, B, C |
| `a` | a, b, c |
| `I` | I, II, III |
| `i` | i, ii, iii |

| `<ol>` Attribute | Description |
|-----------------|-------------|
| `type` | Numbering style |
| `start` | Starting number (default: 1) |
| `reversed` | Descending order |

### Unordered List (`<ul>`) — Bulleted List
Displays items with bullet points. Paired, block-level.

```html
<ul type="disc">
  <li>Item One</li>
  <li>Item Two</li>
</ul>
```

| `type` Value | Bullet Style |
|-------------|-------------|
| `disc` | ● (default) |
| `circle` | ○ |
| `square` | ■ |

### Definition List (`<dl>`)
Used to display definitions or glossary items. Paired tag.

```html
<dl>
  <dt>HTML</dt>
  <dd>HyperText Markup Language</dd>
  <dt>CSS</dt>
  <dd>Cascading Style Sheets</dd>
</dl>
```

| Tag | Meaning |
|-----|---------|
| `<dl>` | Definition List container |
| `<dt>` | Definition Term (title/word) |
| `<dd>` | Definition Data (description) |

### Nested Lists
Lists can be nested inside each other to any depth:
```html
<ol>
  <li>Frontend
    <ul>
      <li>HTML</li>
      <li>CSS</li>
    </ul>
  </li>
  <li>Backend</li>
</ol>
```

---

## 11. Table Tags

Used to display data in rows and columns. All table-related tags are **paired**.

```html
<table border="1" align="center" width="80%">
  <caption>Student Data</caption>
  <thead>
    <tr>
      <th>Name</th>
      <th>Age</th>
      <th>City</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Rahul</td>
      <td>20</td>
      <td>Pune</td>
    </tr>
  </tbody>
  <tfoot>
    <tr>
      <td colspan="3">End of Table</td>
    </tr>
  </tfoot>
</table>
```

| Tag | Purpose | Level |
|-----|---------|-------|
| `<table>` | Container for the whole table | Block |
| `<caption>` | Table heading/title | Block |
| `<thead>` | Table header section | Block |
| `<tbody>` | Table body section | Block |
| `<tfoot>` | Table footer section | Block |
| `<tr>` | Table Row | Block |
| `<th>` | Table Header Cell (bold, centered) | Inline |
| `<td>` | Table Data Cell | Inline |

### Table Attributes

| Attribute | Applied To | Description |
|-----------|-----------|-------------|
| `border` | `<table>` | Border thickness (0 = no border) |
| `align` | `<table>` | Table alignment (left/center/right) |
| `width` | `<table>` | Width in pixels or % |
| `colspan` | `<th>`, `<td>` | Merge/span across columns |
| `rowspan` | `<th>`, `<td>` | Merge/span across rows |
| `cellspacing` | `<table>` | Space between cells |
| `cellpadding` | `<table>` | Space inside cells |

---

## 12. Fieldset & Legend

Groups related form elements inside a visible border.

```html
<fieldset align="center" width="50%">
  <legend align="center">Personal Info</legend>
  <!-- Form elements here -->
  Name: <input type="text" />
</fieldset>
```

| Tag | Purpose |
|-----|---------|
| `<fieldset>` | Draws border around grouped elements. Paired, block-level |
| `<legend>` | Sets a title/heading for the fieldset. Sub-tag of fieldset |

---

## 13. Div Tag

A container/grouping tag. Used to divide the web page into sections for layout and CSS styling. **Paired, block-level.**

```html
<div style="background:lightblue; width:50%;">
  <p>Content inside a div block</p>
  <img src="banner.jpg" />
</div>
```

> `<div>` is fundamental for modern web page layout. It has no visual styling by default — CSS gives it appearance.

---

## 14. Form & Input Elements

### `<form>` Tag
Groups input elements and submits user data to a server-side program. **Paired, block-level.**

```html
<form action="login.php" method="post" enctype="multipart/form-data">
  <!-- Input elements here -->
  <input type="submit" value="Login" />
</form>
```

#### Form Attributes

| Attribute | Description |
|-----------|-------------|
| `action` | URL of the server-side program to send data to |
| `method` | `get` or `post` — how data is sent |
| `target` | `_self`, `_blank`, `_parent`, `_top` — where to open response |
| `enctype` | Encoding type: `application/x-www-form-urlencoded` (default) or `multipart/form-data` (for file uploads) |
| `autocomplete` | `on` (default) or `off` |
| `novalidate` | Disable built-in HTML5 validation |

#### GET vs POST Method

| Feature | GET | POST |
|---------|-----|------|
| Data visibility | Shows in URL address bar | Hidden from URL |
| Browser history | Saved | Not saved |
| Security | Less secure | More secure |
| Data limit | ~5.7 KB | Unlimited |
| Speed | Faster | Slower |
| Bookmarkable | Yes | No |
| Data types | Text only | Text + Files |
| Use cases | Search, fetch data | Login, signup, registration |

---

### `<input>` Tag

The most versatile form element. **Unpaired, inline.**

```html
<input type="TYPE" attributes>
```

#### All Input Types

---

#### 🔸 Text Field
```html
<input type="text" name="username" id="uname" placeholder="Enter name" maxlength="30" />
```

#### 🔸 Password Field
```html
<input type="password" name="pwd" placeholder="Enter password" />
```
Displays characters as `*` or dots.

#### 🔸 Number Field
```html
<input type="number" name="age" min="1" max="100" step="1" />
```
| Attribute | Description |
|-----------|-------------|
| `min` | Minimum allowed value |
| `max` | Maximum allowed value |
| `step` | Increment/decrement step |

#### 🔸 Hidden Field
```html
<input type="hidden" name="userId" value="1025" />
```
Invisible to user. Used for session tracking. Data IS sent to server on submit.

#### 🔸 General Button
```html
<input type="button" value="Click Me" onclick="myFunction()" />
```
Triggers JavaScript. Data is NOT sent to server.

#### 🔸 Reset Button
```html
<input type="reset" value="Clear Form" />
```
Clears all form fields. Must be inside `<form>`.

#### 🔸 Submit Button
```html
<input type="submit" value="Submit" />
```
Sends all form data + query string to the server.

**Query String format (GET method):**
```
https://www.site.com/search.jsp?t1=value1&t2=value2&sb=Submit
```

#### 🔸 Image Button
```html
<input type="image" src="submit.png" />
```
Submits form with x,y coordinates of where user clicked.

#### 🔸 Checkbox
```html
<!-- Multiple selections allowed -->
<input type="checkbox" name="hobbies" value="cricket" /> Cricket
<input type="checkbox" name="hobbies" value="chess" checked /> Chess
```
> All checkboxes for the same purpose must share the same `name`.
> `checked` attribute = default selected.

#### 🔸 Radio Button
```html
<!-- Only one selection allowed from the group -->
<input type="radio" name="gender" value="male" /> Male
<input type="radio" name="gender" value="female" checked /> Female
```
> All radio buttons in a group must share the same `name`.

#### 🔸 File Upload
```html
<input type="file" name="resume" accept=".pdf,.doc" multiple />
```
> Requires `method="post"` and `enctype="multipart/form-data"` on the form.

#### 🔸 Color Picker
```html
<input type="color" name="favcolor" value="#ff0000" />
```

#### 🔸 Date & Time Controls

| Type | Description | Syntax |
|------|-------------|--------|
| `date` | Date picker | `<input type="date">` |
| `time` | Time selector | `<input type="time">` |
| `datetime-local` | Date + time | `<input type="datetime-local">` |
| `month` | Month picker | `<input type="month">` |
| `week` | Week picker | `<input type="week">` |

#### 🔸 Email Field
```html
<input type="email" name="email" placeholder="example@mail.com" />
```
Built-in validation: requires `@` and `.` characters.

#### 🔸 URL Field
```html
<input type="url" name="website" placeholder="https://example.com" />
```
Built-in validation for URL format.

#### 🔸 Range / Slider
```html
<input type="range" min="0" max="100" step="5" value="50" />
```

#### Common `<input>` Attributes

| Attribute | Description |
|-----------|-------------|
| `type` | Type of input control |
| `name` | Name for server-side (can repeat) |
| `id` | Unique ID for client-side JS |
| `value` | Default/initial value |
| `placeholder` | Hint text inside field |
| `maxlength` | Maximum number of characters |
| `minlength` | Minimum number of characters |
| `readonly` | Cannot be edited by user |
| `disabled` | Field is grayed out and disabled |
| `required` | Mandatory — form won't submit without it |
| `autofocus` | Cursor automatically placed here on page load |
| `tabindex` | Controls Tab key focus order |
| `size` | Width of the input field |
| `checked` | Default checked (checkbox/radio) |

---

## 15. Dropdown, Listbox & Optgroup

### Dropdown (Combo Box)
```html
<select name="city">
  <option value="pune">Pune</option>
  <option value="mumbai" selected>Mumbai</option>
  <option value="delhi">Delhi</option>
</select>
```

### List Box
```html
<select name="courses" size="4" multiple>
  <option>HTML</option>
  <option>CSS</option>
  <option>JavaScript</option>
  <option>React</option>
</select>
```

| Attribute | Applied To | Description |
|-----------|-----------|-------------|
| `selected` | `<option>` | Default selected item |
| `size` | `<select>` | Converts to list box; shows N options |
| `multiple` | `<select>` | Allows multi-selection |
| `value` | `<option>` | Value sent to server |

### Option Groups
```html
<select name="vehicle">
  <optgroup label="Two Wheelers">
    <option>Bike</option>
    <option>Scooter</option>
  </optgroup>
  <optgroup label="Four Wheelers">
    <option>Car</option>
    <option>SUV</option>
  </optgroup>
</select>
```

---

## 16. Textarea & Progress Bar

### Textarea — Multi-line Text Box
```html
<textarea name="address" rows="5" cols="40" maxlength="500" placeholder="Enter address...">
Default text here
</textarea>
```

| Attribute | Description |
|-----------|-------------|
| `rows` | Number of visible lines |
| `cols` | Number of characters per line |
| `maxlength` | Total character limit |

> User can resize the textarea at runtime by dragging the corner.

### Progress Bar
```html
<progress min="0" max="100" value="70"></progress>
```
> To animate dynamically, use JavaScript.

---

## 17. Label & Datalist

### `<label>` Tag
Provides a description/prompt for form controls. Clicking the label moves cursor to its associated input.

```html
<label for="uname">Username:</label>
<input type="text" id="uname" name="username" />
```
> Labels are NOT sent to the server on form submit.

### `<datalist>` — Autocomplete Suggestions
Shows suggestions as user types. Links to an `<input>` via the `list` attribute.

```html
<input type="text" list="browsers" placeholder="Choose a browser" />
<datalist id="browsers">
  <option value="Chrome">
  <option value="Firefox">
  <option value="Safari">
  <option value="Edge">
</datalist>
```

### `<output>` Tag
Displays a calculated or result value on the webpage. Paired, inline.
```html
<output name="result">42</output>
```

### `<details>` and `<summary>` Tags
Creates an expand/collapse widget. Both paired, block-level.
```html
<details>
  <summary>Click to expand</summary>
  <p>This hidden content is revealed when clicked.</p>
</details>
```

---

## 18. HTML5 Semantic Tags

These tags give meaning to the structure of a web page. None have default styling — CSS is required.

```
+---------------------------+
|        <header>           |
+---------------------------+
|        <nav>              |
+--------+------------------+
|        |                  |
| <aside>|  <section>       |
|        |                  |
+--------+------------------+
|        <footer>           |
+---------------------------+
```

| Tag | Purpose |
|-----|---------|
| `<header>` | Top section — logo, search bar, navigation |
| `<nav>` | Navigation menu with links |
| `<section>` | A specific section/topic of the page |
| `<article>` | Independent, self-contained content (blog posts, forum posts, news articles) |
| `<aside>` | Sidebar content — ads, extra info, related links |
| `<footer>` | Bottom section — contact, copyright, FAQs |
| `<figure>` | Self-contained content like images, diagrams, code |
| `<figcaption>` | Caption/annotation for `<figure>` |
| `<mark>` | Highlighted/relevant text (yellow highlight by default) |

```html
<header>
  <h1>My Website</h1>
  <nav>
    <a href="index.html">Home</a>
    <a href="about.html">About</a>
  </nav>
</header>

<section>
  <article>
    <h2>Blog Post Title</h2>
    <p>Article content here...</p>
  </article>
</section>

<aside>
  <p>Advertisement or related links</p>
</aside>

<footer>
  <p>&copy; 2024 Rahul Thakare. All rights reserved.</p>
</footer>

<figure>
  <img src="diagram.png" alt="Architecture Diagram" />
  <figcaption>System Architecture Overview</figcaption>
</figure>
```

---

## 19. Audio & Video Tags

### `<audio>` Tag (HTML5)
Embeds audio files in the web page.

```html
<audio controls autoplay loop muted>
  <source src="music.mp3" type="audio/mp3">
  <source src="music.ogg" type="audio/ogg">
  Your browser does not support audio.
</audio>
```

| Attribute | Description |
|-----------|-------------|
| `src` | Path to audio file |
| `controls` | Shows play/pause, volume controls |
| `autoplay` | Plays automatically on page load |
| `loop` | Repeats from beginning after completion |
| `muted` | Mutes the audio |

---

### `<video>` Tag (HTML5)
Embeds video files in the web page.

```html
<video width="640" height="360" controls autoplay poster="thumbnail.jpg">
  <source src="movie.mp4" type="video/mp4">
  <source src="movie.webm" type="video/webm">
  Your browser does not support video.
</video>
```

| Attribute | Description |
|-----------|-------------|
| `src` | Path to video file |
| `controls` | Shows video player controls |
| `autoplay` | Plays automatically |
| `loop` | Repeats continuously |
| `muted` | Mutes audio |
| `width` | Player width |
| `height` | Player height |
| `poster` | Thumbnail image before video plays |

> The `<source>` tag allows multiple formats for browser compatibility.

---

## 20. iframe & Map Tag

### `<iframe>` — Inline Frame
Embeds another web page inside the current page. **Paired, inline.**

```html
<iframe src="https://www.google.com/maps/embed?..." width="600" height="400" frameborder="0">
</iframe>

<!-- Embed HTML content directly -->
<iframe srcdoc="<p>Hello World</p>" width="400" height="200"></iframe>
```

| Attribute | Description |
|-----------|-------------|
| `src` | URL of the page to embed |
| `srcdoc` | Inline HTML content |
| `width` | Frame width |
| `height` | Frame height |
| `frameborder` | Show (1) or hide (0) border |

---

### `<map>` & `<area>` Tags — Image Maps
Creates clickable regions on an image. `<map>` is paired; `<area>` is unpaired.

```html
<img src="world.jpg" usemap="#worldmap" />

<map name="worldmap">
  <area shape="circle" coords="200,150,50" href="asia.html" alt="Asia" />
  <area shape="rect" coords="0,0,100,100" href="europe.html" alt="Europe" />
  <area shape="poly" coords="10,20,30,40,50,20" href="africa.html" alt="Africa" />
</map>
```

| `shape` Value | `coords` Format |
|-------------|----------------|
| `circle` | `cx, cy, radius` |
| `rect` | `x1, y1, x2, y2` |
| `poly` | `x1,y1, x2,y2, x3,y3, ...` |

> 💡 Use [image-map.net](https://www.image-map.net/) to easily generate coordinates.

---

## 21. Meta & Base Tag

*(Already covered in Section 5 — Head Section Tags)*

Quick reminder:
```html
<!-- In <head> section -->
<base href="https://www.mysite.com/" target="_blank" />
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
```

---

## 22. Marquee Tag

Scrolling/moving text or elements. **⚠️ Deprecated tag** (not recommended for modern websites).

```html
<marquee direction="left" behavior="scroll" scrollamount="6" loop="infinite">
  Scrolling Text Here
</marquee>

<marquee direction="up">
  <img src="logo.png" />
</marquee>
```

| Attribute | Values | Description |
|-----------|--------|-------------|
| `direction` | `left` (default), `right`, `up`, `down` | Scroll direction |
| `behavior` | `scroll`, `slide`, `alternate` | Movement behavior |
| `scrollamount` | Number (default: 6) | Scroll speed |
| `scrolldelay` | Milliseconds (default: 84ms) | Delay between movements |
| `loop` | Number or `infinite` | How many times to repeat |

---

## 23. HTML Entities

Special characters that cannot be typed directly in HTML.

| Entity | Character | Description |
|--------|-----------|-------------|
| `&nbsp;` | (space) | Non-breaking space |
| `&lt;` | `<` | Less than |
| `&gt;` | `>` | Greater than |
| `&amp;` | `&` | Ampersand |
| `&copy;` | © | Copyright |
| `&reg;` | ® | Registered trademark |
| `&trade;` | ™ | Trademark |
| `&euro;` | € | Euro sign |
| `&pound;` | £ | Pound sign |
| `&rupee;` | ₹ | Rupee sign |
| `&hearts;` | ♥ | Heart symbol |
| `&star;` | ★ | Star |

**Numeric form:**
```html
&#169; = ©    &#60; = <    &#62; = >
```

---

## 24. Comments

Comments are for describing your code. They are **not displayed** in the browser and not executed.

```html
<!-- This is a single line comment -->

<!--
  This is a
  multi-line comment
-->
```

---

## 25. Practice Programs Index

All 37 programs in the [rahulthakare04/html](https://github.com/rahulthakare04/html) repository:

| File | Topics Covered |
|------|---------------|
| `ex1.html` | Basic HTML structure — `<!DOCTYPE>`, `<html>`, `<head>`, `<body>`, headings, paragraphs |
| `ex2.html` | Heading tags `<h1>` to `<h6>`, text formatting |
| `ex3.html` | Paragraph `<p>`, line break `<br>`, horizontal rule `<hr>` |
| `ex4.html` | Text formatting — `<b>`, `<i>`, `<u>`, `<strike>`, `<sup>`, `<sub>`, `<mark>` |
| `ex5.html` | `<pre>` tag — pre-formatted text, `<span>` tag |
| `ex6.html` | HTML entities — special characters |
| `ex7.html` | `<title>` and `<link>` — favicon setup |
| `ex8.html` | `<img>` tag — displaying images with attributes |
| `ex9.html` | Hyperlinks `<a>` — external and internal links |
| `ex10.html` | Hyperlink targets — `_blank`, `_self`, bookmarks |
| `ex11.html` | Ordered lists `<ol>` — all numbering types |
| `ex12.html` | Unordered lists `<ul>` — disc, circle, square |
| `ex13.html` | Nested lists — `<ol>` inside `<ul>` and vice versa |
| `ex14.html` | Definition list `<dl>`, `<dt>`, `<dd>` |
| `ex15.html` | `<table>` — basic table with `<tr>`, `<th>`, `<td>` |
| `ex16.html` | Table — `colspan` and `rowspan` (merging cells) |
| `ex17.html` | Table — `<caption>`, `<thead>`, `<tbody>`, `<tfoot>` |
| `ex18.html` | `<fieldset>` and `<legend>` |
| `ex19.html` | `<div>` tag — grouping and layout |
| `ex20.html` | `<form>` — input types: text, password, submit, reset |
| `ex21.html` | Input types — number, hidden, button |
| `ex22.html` | Input types — checkbox, radio button |
| `ex23.html` | Input types — file upload, color picker |
| `ex24.html` | Input types — date, time, datetime-local, month, week |
| `ex25.html` | Input types — email, url, range (slider) |
| `ex26.html` | Dropdown `<select>` and `<option>` |
| `ex27.html` | List box — `size` and `multiple` attributes |
| `ex28.html` | Option groups `<optgroup>` |
| `ex29.html` | `<textarea>` — multi-line text input |
| `ex30.html` | `<label>` and `<datalist>` |
| `ex31.html` | `<progress>` and `<output>` tags |
| `ex32.html` | `<details>` and `<summary>` tags |
| `ex33.html` | HTML5 semantic tags — `<header>`, `<nav>`, `<section>`, `<footer>`, `<aside>` |
| `ex34.html` | `<article>`, `<figure>`, `<figcaption>`, `<mark>` |
| `ex35.html` | `<audio>` and `<video>` tags |
| `ex36.html` | `<iframe>` and `<map>` with `<area>` |
| `ex37.html` | `<meta>` tags, `<base>` tag, `<marquee>` tag |

---

## 26. Quick Reference Cheat Sheet

### Structure
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Page Title</title>
</head>
<body>
  <!-- Content here -->
</body>
</html>
```

### Text
```html
<h1>–<h6>         Headings
<p>               Paragraph
<br/>             Line break
<hr/>             Horizontal line
<b>/<strong>      Bold
<i>/<em>          Italic
<u>               Underline
<strike>/<del>    Strikethrough
<sup>             Superscript
<sub>             Subscript
<mark>            Highlighted
<pre>             Preformatted
<span>            Inline container
```

### Media & Links
```html
<img src="" alt="" width="" height="">
<a href="" target="">Link Text</a>
<audio controls src="file.mp3"></audio>
<video controls src="file.mp4" poster="thumb.jpg"></video>
<iframe src="url" width="" height=""></iframe>
```

### Lists
```html
<ol type="1|A|a|I|i" start="1">  Ordered
<ul type="disc|circle|square">    Unordered
<dl><dt>Term</dt><dd>Def</dd></dl> Definition
<li>                               List item
```

### Tables
```html
<table><tr><th>Head</th><td>Data</td></tr></table>
colspan="N"   Merge columns
rowspan="N"   Merge rows
```

### Forms
```html
<form action="" method="get|post">
<input type="text|password|number|email|radio|checkbox|file|date|color|range|submit|reset">
<select><option>Item</option></select>
<textarea rows="" cols=""></textarea>
<button type="submit|reset|button">
<label for="id">Label</label>
```

### HTML5 Semantic
```html
<header>   <nav>      <main>
<section>  <article>  <aside>
<footer>   <figure>   <figcaption>
<details>  <summary>  <mark>
```

---

## 🔗 Repository

📁 **GitHub:** [rahulthakare04/html](https://github.com/rahulthakare04/html)  
📄 **Notes Reference:** HTML Notes Part 1 & Part 2 (Class Notes)  
🌐 **Standard:** W3C HTML5

---

## 📝 Author

**Rahul Thakare**  
HTML Learning Notes — Full Reference Guide  
*Created for revision and quick reference*

---

*⚡ Tip: Bookmark this file for quick HTML revision before exams or interviews!*
