# The new conda-forge.org

As you might have noticed, for the last few months we have been changing different parts of the conda-forge.org website. Read more to learn more about what we changed, how it works and how to contribute.

<!-- truncate -->

## Old vs new

The [old conda-forge.org](https://github.com/conda-forge/conda-forge.github.io/tree/1d3214c295a46a249434de4fcf48c6b8d747a07f) documentation was written with [Sphinx](https://www.sphinx-doc.org). Some extra extensions were responsible for the other parts of the website; e.g. the [blog](https://github.com/conda-forge/blog), the [RSS feed](https://github.com/conda-forge/conda-forge.github.io/tree/1d3214c295a46a249434de4fcf48c6b8d747a07f/newsfeed), the [frontpage](https://github.com/conda-forge/conda-forge.github.io/blob/1d3214c295a46a249434de4fcf48c6b8d747a07f/index.html.tmpl), [feedstock outputs](https://github.com/conda-forge/conda-forge.github.io/blob/1d3214c295a46a249434de4fcf48c6b8d747a07f/feedstock_outputs.html.tmpl), or the [status page](https://github.com/conda-forge/status/tree/bde62db0bc9de460f533d60ca6218604c3e42fa5/site).

The new website has been rewritten using the [Docusaurus](https://docusaurus.io/) project. This allows us to have a single framework for all the sections of the site. There are some big differences if we compare the new site with the old one:

- Sphinx was written in Python. Docusaurus uses the Node.js stack.
- Most of our docs were written in RST. Docusaurus handles Markdown and MDX (Markdown + JSX).
- Instead of generating static HTML from Jinja templates, we now prefer fetching the JSON payloads and render the relevant pages at build time (i.e. when we run `npm run build`) or at load time (when the user visits the website). This allows to have all the website rendering logic in the same repository with a unified theme, search engine and statistics.

## What we have changed

- The theme for the whole site is responsive, accessible, mobile friendly and supports dark/light modes. A style guide is available too.
- The Status dashboard fetches data dynamically and provides detailed views for each migration.
- The Packages section lists latest updates in addition to mapping packages to feedstocks.
- A new Download page displays links to the latest Miniforge installers.
- The documentation has been split in two top-level categories: Docs and Community.
- Algolia generously serves the backend for the search bar.
- Netlify will render previews on each opened PR for a smoother contribution process.
- The blog posts and the announcements feed are served natively by Docusaurus.
- We converted all the Sphinx-native ReStructuredText documents to Docusaurus-friendly Markdown.
- The conda-forge.yml docs are autogenerated from the conda-smithy schemas.
- ... and a bunch of smaller changes in the documentation. Refer to the [meta-issue](https://github.com/conda-forge/conda-forge.github.io/issues/1971) for more information!

## New features you can use

- Learn how to use and maintain packages from conda-forge in the [main documentation section](/docs).
- Read about how our community is set up in the [Community section](/community)
- The most recent changes to our infrastructure will be announced in [News](/news). You can also subscribe to the [RSS feed](pathname:///news/rss.xml) and browse the [archive](/news/archive/).
- Important information about the ecosystem is discussed in the [Blog](/blog). You can also subscribe to the [RSS feed](pathname:///blog/rss.xml) and browse the [archive](/blog/archive/). The posts are sometimes categorized with [tags](/blog/tags/) too.
- Use the search bar to locate any document in the website! It should be smart enough to remember the content you need more often. Use the <kbd>Cmd/Ctrl</kbd>+<kbd>K</kbd> shortcut for faster access.
- The [Status dashboard](/status) will inform you about the latest incidents and ongoing migrations. Each migration has now a permalink you can explore and share!
- The [Packages](/packages) section will help you find all the packages in conda-forge. If you don't type anything in the search bar, it will list the last 100 uploads to the Anaconda.org channel. The metadata link in each row will take you to the [`conda-metadata-app` dashboard](https://conda-metadata-app.streamlit.app/).
- Use the [Download page](/download) to get the latest Miniforge installers.

## How to help and contribute

We have changed a lot of things, so there's a chance we missed something somewhere. If you have suggestions or errors to report, please let us know in the [website issue tracker](https://github.com/conda-forge/conda-forge.github.io/issues). Feel free to check the [documentation contribution guidelines](/docs/user/contributing/#improve-the-website) too.

## Acknowledgements

This revamp was a months-long effort. The core team would like to take a moment to thank to all the contributors that made it possible (in alphabetical order): Afshin Darian, Asmit Malakannawar, Gabriela Vives, Isabela Presedo-Floyd, Klaus Zimmermann, Tania Allard.
