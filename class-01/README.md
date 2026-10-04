# Class 1: Your First Web Page

**This class you'll learn:**

- The structure of every web page: `<!DOCTYPE html>`, `<html>`, `<head>`, `<title>`, `<body>`
- Headings `<h1>`–`<h6>`, paragraphs `<p>`, bold `<strong>` / `<b>`, line breaks `<br>`
- Comments `<!-- -->`

No colours or layout yet. Plain black text is exactly right for today.

## Before you start

1. Open VS Code → **File → Open Folder** → open your `web-programming-lab-2026` folder.
2. In the sidebar, open `class-01/starter/`.
3. Right-click `index.html` → **Open with Live Server**. Your browser opens the page.
4. Put VS Code and the browser side by side. Every time you save, the browser updates.

Right now the page shows everything on one line. By the end, it will be a proper café home page.

## Cheat sheet

| Tag | What it does | Example |
|---|---|---|
| `<!DOCTYPE html>` | Says "this is a modern HTML page". Always the first line. | |
| `<html>` | Wraps the whole page | |
| `<head>` | Information **about** the page (not shown on the page) | |
| `<title>` | The text in the browser tab. Goes inside `<head>`. | `<title>Bean & Byte Café</title>` |
| `<body>` | Everything you **see** on the page | |
| `<h1>`–`<h6>` | Headings. `h1` is the most important; use only one per page. | `<h2>About us</h2>` |
| `<p>` | A paragraph | `<p>Fresh coffee.</p>` |
| `<strong>` | Important text, shown bold | `<strong>Closed</strong>` |
| `<b>` | Bold look only, no extra meaning | `<b>New!</b>` |
| `<br>` | New line inside a paragraph. No closing tag. | `Line one<br>Line two` |
| `<!-- -->` | A comment: a note for humans; the browser ignores it | `<!-- TODO -->` |

**Remember:**
- Most tags come in pairs: `<p>` opens, `</p>` closes (note the `/`).
- Close tags in reverse order: `<p><strong>Hi</strong></p>` ✅, not `<p><strong>Hi</p></strong>` ❌
- The browser ignores extra spaces and new lines in your code. Use `<p>` and `<br>` to control lines.

## Part A: Café home page

Open `class-01/starter/index.html` and complete **TODO 1 to TODO 8**.

## Part B: About me

1. In the `class-01/starter/` folder, create a new file called `about-me.html`.
   (Right-click the folder in VS Code → **New File**.)
2. In the empty file, type `!` and press **Tab**. VS Code writes the page structure for you.
3. Build a page about yourself:
   - Title: `About me`
   - Your name as the main heading (`h1`)
   - A sub-heading "My hobbies" with a paragraph about them
   - A sub-heading "My favourite drink" with a paragraph about it. Make the drink's name **bold**.
   - A sub-heading "Where I'm from" with your town and state on separate lines (use `<br>`)

To view it, right-click `about-me.html` → **Open with Live Server**.

## Check your work

- [ ] The browser tab shows **Bean & Byte Café**
- [ ] There is one big main heading and three sub-headings
- [ ] Each day of the opening hours is on its own line
- [ ] Each line of the address is on its own line
- [ ] "freshly roasted coffee" and "Closed" are bold
- [ ] `about-me.html` works and has your name as its heading
- [ ] You submitted your work (see below)

## How to submit

1. Open **Source Control** in VS Code (the branch icon in the left sidebar).
2. Type a message, for example `Class 1: home page + about me`.
3. Click **Commit**. If VS Code asks to stage all changes, click **Yes**.
4. Click **Sync Changes** to upload your work to GitHub. (The first time, a browser may open asking you to sign in to GitHub.)
5. Open your fork on GitHub and check that your files are in `class-01/starter/`.
6. Submit the link to your `class-01` folder where your demonstrator asks. It looks like this:
   `https://github.com/YOUR-USERNAME/web-programming-lab-2026/tree/main/class-01`

Prefer the terminal?

```bash
git add .
git commit -m "Class 1: home page + about me"
git push
```

## Stretch challenges (finished early?)

1. **All six headings:** Add a test section using `<h1>` to `<h6>`. Then try `<h7>`. What happens, and why?
2. **Italics:** Find out the difference between `<em>` and `<i>`. (Hint: it's like `<strong>` and `<b>`.) Use one on your About me page.
3. **Horizontal line:** Look up `<hr>` and use it to separate the sections on your About me page.
4. **View source:** Open any website, press **Ctrl + U** (Mac: **Cmd + Option + U**) and find its `<title>` and an `<h1>`.
5. **Validator:** Paste your HTML into <https://validator.w3.org/#validate_by_input>. Fix any errors it finds.
