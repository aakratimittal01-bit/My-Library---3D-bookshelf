# My library

A shelf of the books you've read, drawn as real spines. The books you're reading now lean against a bookend, finished ones stand in a row, and a hanging lamp turns the room into a night library.

It's a single web page with no server and no sign-up, so it runs on GitHub Pages for free.


https://github.com/user-attachments/assets/a3faca88-5f2b-41dd-b4ee-adb03b1f30ac



## Make your own shelf

1. Click **Use this template** (or fork this repository) to get your own copy.
2. Open `books.csv` and delete everything except its first line (the column headings), so your shelf starts empty.
3. Go to **Settings → Pages**, choose **Deploy from a branch**, select **main** and **/ (root)**, and click **Save**. After a minute or two your shelf is live at `https://<your-username>.github.io/<repo-name>/`.
4. Open your shelf. It asks your name, then shows an empty shelf with two dashed outline books: one leaning by the bookend for what you're reading now, and one for books you've read.
5. Click a dashed book (or a **+** under the shelf) to add a book. To add the books you've already read in one go, choose **Upload in bulk** in that form.
6. When you're happy, open **All books** from the round profile button, click the download icon (with **All** selected) and upload that `books.csv` to your repository, replacing the old one. Now everyone who opens your link sees your shelf.

To change the name at the top of the page, edit the `<h1>` and `<title>` in `index.html`.

## How saving works

Everything you add or change is saved in your browser straight away, and it's what you see whenever you open your shelf on that device, while editing or after **Done editing**. Adding books never needs a CSV file.

`books.csv` in your repository is what *other people* see when they open your link, since your browser's copy lives only on your computer. To share your latest shelf with them, open **All books**, click the download icon, and upload that `books.csv` to your repository. If you only use the shelf for yourself, you can skip this.

**Edit this shelf** at the bottom of the page shows the + buttons and editing links; **Done editing** hides them. If someone else clicks **Edit this shelf** on your site, their changes stay in their own browser and never touch your repository.

## Adding and changing books

- **+ next to Currently reading** (or the dashed leaning book): the book you're reading now. It gets a red bookmark. You can have up to three on the go.
- **+ next to Read** (or the dashed upright book): a book you've finished. The newest go at the front of the read section.
- Type the book name and the author is filled in from [Open Library](https://openlibrary.org) for you to confirm. Category is picked for you, typos get a "Did you mean…", and names typed in lower case get their capitals.
- **About the book** is optional: a favourite line or what it's about.
- **Design your book** (optional) sets thickness, size and spine colour (solid or gradient). Anything you leave empty is chosen for you.

Click a book while editing to see **Edit**, **Remove** and, for books you're reading, **Mark as read**, which pops the book out of the pile and glides it over to the read side.

## Uploading a list

Choose **Upload in bulk** in the add form, or **Upload list** on the All books page, and pick a CSV file (for example a Google Sheet downloaded as **Comma-separated values**). Every book needs a title, author and category; everything else is optional. Click **Download sample CSV** in the upload window for a starting file: its column headings say what each column takes. The optional **status** column takes Read or Reading: books marked Reading go to the currently reading corner (up to three), and an empty status means read. Books already on the shelf are skipped, or you can replace the whole shelf. Files saved by Excel in its older format are read correctly too.

## All books

Open the round profile button and choose **All books** for every book in a table. Filter by fiction or non-fiction, click a column heading to sort, and use the download icon to save what you see as a CSV. While editing, click any cell to change it, use **+** next to the title to add a book, or **Upload list** to add many at once.

## Your profile

The round button at the top right shows the first letter of your name with a small red bookmark. If you skipped the name, it shows an open book, and the menu has an **Add your name** line.

## Day and night

By day the shelf stands against a sage-green wall. Pull the cord on the lamp at the top left to switch to the night library, with a warm beam falling on the books you're reading. Pull it again to switch back. The page remembers your choice; until then it follows your computer's light or dark setting.

## Trying it on your computer

The page reads `books.csv` from the same folder, which browsers don't allow for files opened straight from disk. Start a small local server in this folder instead:

```
python3 -m http.server
```

and open `http://localhost:8000`.

## Credits

Book details come from [Open Library](https://openlibrary.org). The 3D book idea was inspired by [Sebastien Castiel's animated 3D book in CSS](https://scastiel.dev/animated-3d-book-css) and [calibre-web](https://github.com/janeczku/calibre-web).
