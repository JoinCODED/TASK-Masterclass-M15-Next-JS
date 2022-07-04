# Next.js

🤓: Can I get my website in the first page of Google?
🧑‍💻: Why yes, just use `Next.js`!

## Setup

1. Go to your `Development` folder.
2. Create a `Next.js` app using `npx create-next-app --ts` (note: if you have both `yarn` and `npm` installed use `npx create-next-app --ts --use-npm`).
   - Call the app `task-masterclass-m15-next-js`

## Exploring Next.js

1. Create a `components` folder.
2. Add a `hello.txt` file inside of `public/`.
   - Go to `http://localhost:3000/hello.txt`, what do you see?
3. Add a `Footer.tsx` component inside of `components/` and a corresponding `Footer.module.css` file inside of `styles/`.
   - Add a `footer` tag and add some content to it
   - Style your footer using the `classes` imported from `Footer.module.css` (don't waste too much time styling).
4. Add a `Navbar.tsx` component inside of `components` and a corresponding `Navbar.module.css` inside of `styles/`.
   - Add a `nav` tag with a `ul` tag inside.
     - Add an `li` tag inside of your `ul` tag and add a `Link` component imported from `next/link`.
       - Have the link take the user to the home page (i.e., `href="/"`)
     - Add another `li` tag inside of your `ul` tag with a `Link` component inside.
       - Have the link take the user to the about page that we will create (i.e., `href="/about"`)
   - Style your navbar using the `classes` imported from `Navbar.module.css` (don't waste too much time styling).
5. Add a `Layout` component inside of `components/` with a corresponding `Layout.module.css` file inside of `styles/`. It should look similar to the example [here](https://nextjs.org/docs/basic-features/layouts).
6. Add an `about.tsx` page inside of `pages/` with a corresponding `About.module.css` file inside of `styles/`.
   - Add some lorem ipsum and style it
7. Test out that your `Navbar` links to the different pages correctly.
8. Commit and push your code.
