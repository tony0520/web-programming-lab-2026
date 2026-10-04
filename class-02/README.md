# Class 2: Links, Lists, Images, Tables and Forms

**This class the café website grows to three pages:**

| Page | File | You'll practise |
|---|---|---|
| Home | `index.html` | **Links**, **lists**, **images**. This is your Class 1 page (with its map), upgraded. |
| Menu | `menu.html` | **Tables** |
| Order | `order.html` | **Forms** |

Still no styling. CSS comes in Class 3.

## Before you start

1. **Get this class's files:** on GitHub, open your fork → **Sync fork → Update branch**. Then in VS Code: Source Control → **⋯** → **Pull**.
2. Open `class-02/starter/` in the sidebar.
3. Right-click `index.html` → **Open with Live Server**.

## Part A: Home page (`index.html`)

Work through **TODO 1 to TODO 7**.

Key ideas:
- **Attributes** (from Class 1) add information inside the opening tag: `<a href="menu.html">Menu</a>`
- `<header>`, `<main>`, `<section>` and `<footer>` describe the parts of the page. They don't change how it looks.
- Lists: `<ul>` = bullet list, `<ol>` = numbered list, with `<li>` for each item
- An image path is **relative** to the HTML file. `images/logo.svg` means "the `images` folder next to this file".
- **`alt`** text describes an image for people who can't see it, and appears if the image fails to load.
- Special characters: write `&amp;` for &, `&copy;` for ©

## Part B: Menu table (`menu.html`)

Work through **TODO 1 to TODO 6**.

```
<table>
  <caption>  title of the table
  <thead>    heading rows    <tr> <th>
  <tbody>    data rows       <tr> <td>
  <tfoot>    footer rows
```

- `<tr>` = table row, `<th>` = heading cell, `<td>` = data cell
- `colspan="4"` makes one cell stretch across 4 columns
- Tables are for **data** (like a menu or a timetable), not for page layout

## Part C: Order form (`order.html`)

Work through **TODO 1 to TODO 6**.

- `<label for="email">` must match `<input id="email">`. Then clicking the label selects the input.
- The **`name`** attribute is what gets sent. Without `name`, the data is not sent!
- Radio buttons in a group share the **same `name`**, so only one can be chosen.
- `required`, `type="email"` and `min`/`max` give you free checks from the browser.

**Try this when you finish:** fill in the form and click **Place order**. Look at the address bar:

```
order.html?name=Nur+Aisyah&email=aisyah%40example.com&item=latte&quantity=2...
```

That's your form data! Each field is sent as `name=value`. Now remove the `name` attribute from one field, submit again, and see what changes.

## Check your work

- [ ] All 3 pages open, and the navigation links move between them
- [ ] All images appear. No broken image icons.
- [ ] Opening hours are a bulleted list
- - [ ] The menu table has a caption, headings, a Drinks and a Food section, and a footer
- [ ] Clicking any form label selects its field
- [ ] You can't submit the form without a name, a valid email, an item and the checkbox ticked
- [ ] Submitting shows all your fields in the address bar
- [ ] You submitted your work (see below)

## How to submit

Same steps as Class 1: **Source Control → message → Commit → Sync Changes**, check your files on GitHub, then paste the link to your `class-02` folder into the **class Google Form**:
`https://github.com/YOUR-USERNAME/web-programming-lab-2026/tree/main/class-02`

## Stretch challenges (finished early?)

1. **Video:** Create `about.html` with a short story about the café and an embedded YouTube video about making coffee (on YouTube: **Share → Embed**, then copy the code). Add it to the navigation on all pages.
2. **Hours table:** Rewrite the opening hours as a table. Use `rowspan` to merge Monday–Friday into one cell.
3. **Figures:** Wrap the banner image in `<figure>` with a `<figcaption>`.
4. **Datalist:** Add a "How did you hear about us?" text field with suggestions using `<datalist>`.
5. **Keyboard test:** Can you fill in the whole order form using only **Tab**, the arrow keys and **Space**? If something can't be reached, find out why.
6. **Validator:** Paste your HTML into <https://validator.w3.org/#validate_by_input> and fix any errors. (A warning about the table `border` attribute is expected. CSS replaces it in Class 3.)
