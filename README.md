# My library

A shelf of the books you've read, drawn as real spines. You pick each book's thickness, size and spine colour, switch between fiction and non-fiction, and watch new books fly onto the shelf as you add them.

It's a single web page with no server and no sign-up, so it runs on GitHub Pages for free.

## Make your own shelf

1. Click **Use this template** (or fork this repository) to get your own copy.
2. In your copy, go to **Settings → Pages**, set the source to the `main` branch, and save. After a minute your shelf is live at `https://<your-username>.github.io/<repo-name>/`.
3. Open your shelf. It asks your name, then shows an empty shelf with two dashed outline books: one leaning by the bookend for what you're reading now, and one for books you've read.
4. Click a dashed book (or a **+** under the shelf) to add a book. To add the books you've already read in one go, choose **Upload in bulk** in that form. **Upload list** is also on the **All books** page, in the menu under the round profile button.
5. Open **All books** from the profile menu and click the download icon at the top right (with "All" selected) to save your `books.csv`. Replace the `books.csv` file in your repository with it (**Add file → Upload files**, then commit), and your public shelf shows your books. To make more changes later, click **Edit this shelf** at the bottom of the page; **Done editing** in the same spot shows the shelf as visitors see it.

To change the name at the top of the page, edit the `<h1>` and `<title>` in `index.html`.

## How saving works

Everything you change while editing is saved in your browser straight away, so you can close the tab and carry on later on the same device. Visitors to your site see whatever is in `books.csv` in your repository. Your edits become public when you download `books.csv` from the All books page and commit it.

While `books.csv` has no books in it, anyone who opens the site gets an empty shelf of their own to fill, saved in their browser. You can use the site this way without a GitHub account at all.

If someone else clicks **Edit this shelf** on your site, their changes stay in their own browser and never touch your repository.

## Adding a book

Under the shelf there's a **+** next to **Currently reading** for the book you're reading now (it gets a red bookmark; you can have up to three on the go), and a **+** next to **Read** for books you've finished. Both open the same form. Book names and authors typed in lower case get their capitals tidied up, so "the power of now" becomes "The Power of Now". Type the book name and the page looks it up on [Open Library](https://openlibrary.org): it fills in the author for you to confirm, picks fiction or non-fiction, and suggests the correct title if you made a typo. You can add a note, such as a favourite line.

Under **Design your book** you set:

- **Thickness**: Thin, Medium or Thick. Leave it empty and it's set from the book's page count, or picked at random.
- **Size**: Small, Regular or Tall.
- **Spine style**: Solid, Gradient (fades into a second colour) or With bands (a coloured band near the top and bottom).
- **Spine colour**: one of 12 colours or any colour you like. Leave it empty for a random one.

The books you're reading now lean against a wooden bookend at the start of the shelf. After a gap come the books you've read, newest first, which scroll sideways with the arrows when there are more than fit. While editing, an empty reading spot shows a dashed outline of a book you can click to add one. Click a book while editing and use the links under the shelf: **Edit** opens the same form filled in with the book, so you can fix its name or redesign its spine; **Remove** takes it off the shelf (with an Undo); and for a book you're reading, **Mark as read** sends it hopping over to the read side.

## Your profile

The round button at the top right shows the first letter of your name with a small red bookmark. If you skipped the name, it shows an open book instead, and the menu it opens has an "Add your name" line: type your name and press Enter.

## Day and night

By day the shelf stands against a soft sage-green wall. Pull the cord on the lamp hanging at the top left and the lamp switches on: the room turns into a night library, with a warm beam of light falling on the books you're reading. Pull it again to switch back. The page remembers your choice, and until you pull the cord it follows your computer's light or dark setting.

## Seeing all your books

Click the round profile button at the top right and choose **All books** to see every book in a table: title, author, category, status, what it's about, thickness, size and spine. Click any column heading to sort by it, and again to reverse. Show all of them, only fiction or only non-fiction, and click the download icon at the top right to save what you see as a CSV file that opens in Excel or Google Sheets. **Bookshelf** in the same menu takes you back to the spines. You can also link straight to the table by adding `#all-books` to the address.

While you're editing your shelf, the table is editable too. Click any title, author or note to change it (Enter saves, Esc cancels), use the small dropdowns to change the category, status (Read or Reading), thickness, size or spine style, and click the little spine swatch to pick a new colour. The **+** next to the "All books" title adds a book, **Upload list** adds many at once, and the ✕ at the end of a row removes a book, with an Undo. Every change is saved straight away and shows up on the bookshelf. Visitors see the same table without any of the editing controls.

## Uploading a list

Upload a CSV file, such as a Google Sheet downloaded with **File → Download → Comma-separated values**. Every book needs a title, author and category; the design columns are optional and anything left empty is picked at random. Columns can be in any order, and others are ignored.

| Column | Also accepted as | Values |
| --- | --- | --- |
| `title` (required) | `book name`, `book` | The book's name |
| `author` (required) | `writer` | The author's name |
| `category` (required) | `genre`, `type` | Fiction or Non-fiction |
| `thickness` | | Thin, Medium or Thick |
| `size` | `small` | Small, Regular or Tall (`Yes` in a `small` column means Small) |
| `spine` | `style` | Solid, Gradient or Bands |
| `color` | `colour` | A colour like `#2E5C9A`, or words such as `blue`, `gradient blue`, `gradient red tan`, `tan with maroon border` |
| `color2` | `band colour`, `second colour` | The gradient's second colour or the band colour |
| `note` | `favourite line`, `quote` | Shown in quotes under the shelf |

Every book on the list is added as read. Books missing an author or category are listed so you can fix them, and the rest are added. Books already on the shelf with the same name are skipped, or you can replace the whole shelf with the list. `books-template.csv` (the same file as **Download sample CSV** in the upload window) is a starting point: its column headings say which columns are required and what each one takes, and notes in brackets in a heading are ignored when you upload.

## Trying it on your computer

The page reads `books.csv` from the same folder, which browsers don't allow for files opened straight from disk. Start a small local server in this folder instead:

```
python3 -m http.server
```

and open `http://localhost:8000`.

## Credits

Book details come from [Open Library](https://openlibrary.org). The 3D book idea was inspired by [Sebastien Castiel's animated 3D book in CSS](https://scastiel.dev/animated-3d-book-css) and [calibre-web](https://github.com/janeczku/calibre-web).
