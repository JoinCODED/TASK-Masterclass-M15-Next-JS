# Next.js

🤓: Can I get my website in the first page of Google?
🧑‍💻: Why yes, just use `Next.js`!

## Setup

1. Go to your `Development` folder.
2. Create a `Next.js` app using `npx create-next-app --ts` (note: if you have both `yarn` and `npm` installed use `npx create-next-app --ts --use-npm`).
   - Call the app `task-masterclass-m15-next-js`

## Exploring Next.js

1. Create a `components` folder.
2. Add a `hello.txt` file inside of `public/` and write whatever you want in it.
   - Go to `http://localhost:3000/hello.txt`, what do you see?
3. Add a `Footer.tsx` component inside of `components/` and a corresponding `Footer.module.css` file inside of `styles/`.
   - Add a `footer` tag and add some content to it
   - Style your footer using the `classes` imported from `Footer.module.css` (don't waste too much time styling).
4. Add a `Navbar.tsx` component inside of `components` and a corresponding `Navbar.module.css` inside of `styles/`.
   - Add a `nav` tag with a `ul` tag inside.
     - Add an `li` tag inside of your `ul` tag and add a `Link` component imported from `next/link`.
       - Have the link take the user to the home page (i.e., `href="/"`)
     - Add another `li` tag inside of your `ul` tag with a `Link` component inside (add an anchor tag as a child of the `Link` component to add your text, but make sure the `href` is on `Link` no `a`).
       - Have the link take the user to the about page that we will create (i.e., `href="/about"`)
   - Style your navbar using the `classes` imported from `Navbar.module.css` (don't waste too much time styling).
5. Add a `Layout` component inside of `components/` with a corresponding `Layout.module.css` file inside of `styles/`. It should look similar to the example [here](https://nextjs.org/docs/basic-features/layouts).
6. Add an `about.tsx` page inside of `pages/` with a corresponding `About.module.css` file inside of `styles/`.
   - Add some lorem ipsum and style it
7. Test out that your `Navbar` links to the different pages correctly.
8. Commit and push your code.

### Dynamic Routes Bonus

1. Create a folder called `articles` inside of `pages/` and add an `index.tsx`.
2. Add a page component inside of `index.tsx`.

   ```tsx
   import type { NextPage } from "next";
   import Link from "next/link";

   const ArticlePage: NextPage = () => {
     return (
       <>
         <h1>Articles</h1>
         <Link href="/articles/1">
           <a>Article 1</a>
         </Link>
         <Link href="/articles/2">
           <a>Article 1</a>
         </Link>
       </>
     );
   };

   export default ArticlePage;
   ```

3. Add a file called `[id].tsx` inside of `pages/articles`.
4. Display the article id inside of `[id].tsx` (hint: look [here](https://nextjs.org/docs/routing/dynamic-routes))

### Meta Bonus

1. Create a shared `Meta` component.

   ```tsx
   import type { NextPage } from "next";

   const Meta: NextPage = (props) => {
     // your code here
   };

   Meta.defaultProps = {
     // your default props go here
   };

   export default Meta;
   ```

2. Use the following [website](https://www.seoptimer.com/meta-tag-generator) to generate the skeleton of the meta tags.
   - Make sure the content in the tags are all dynamic (i.e., use the props to display the `title`, `description`, and `keywords`).
     - Add the default props in `Meta.defaultProps`
   - Add a link to our favicon
   - Bonus: allow the favicon to be overridden using the props
3. Add the `Meta` component to your `Layout` component.
