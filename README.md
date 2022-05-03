# Level 2 Netflix Shows

This project aims to demonstrate how to use components and CSS frameworks.

## Components

"In Svelte, an application is composed from one or more *components*. A component is a reusable self-contained block of code that [includes] HTML, CSS and JavaScript that belong together, written into a `.svelte` file." - [Svelte](https://svelte.dev/tutorial/basics)

Here's an example of a component called `Header.svelte` which contains all the HTML and CSS for a header.

```html
<header>
  <img src="logo.png" alt="Site logo">
  <h1>Main heading</h1>
</header>

<style>
  header {
    display: flex;
    align-items: center;
  }

  img {
    height: 6rem;
  }

  h1 {
    font-size: 2rem;
    font-weight: bold;
    margin-left: 1rem;
  }
</style>
```

With this, you can reuse this `Header` component in any of your files by first *importing* it and then using it like any other HTML tag.

Here's an eaxmple of the `Header` component being used on the home page.

```html
<script>
  import Header from '$components/Header.svelte'
</script>

<Header />

<nav>
  <a href=".">Home</a>
  <a href="page-1">Page 1</a>
  <a href="page-2">Page 2</a>
  <a href="page-3">Page 3</a>
</nav>

<!-- more content.... >
```

Now, where it says `<Header />` all of the code - including the image and heading - from the `Header` component will be. This saves space and, if you're using the same components alot, time. You can write your component once and reuse it as many times as you need to. If you want to change it: just change it once and all the pages where you used it will be updated.

## CSS Frameworks

"CSS frameworks are tools used by UI developers to make their job easier. Rather than reinventing the wheel each time a new project comes up; frameworks give developers the tools to quickly spin-up user interfaces that can be tweaked and iterated on throughout a project instead of spending time starting from a blank document." - [Medium](https://medium.com/html-all-the-things/what-is-a-css-framework-f758ef0b1a11)

Here's an example of adding the [Bulma](https://bulma.io/) framework to your project.

```html
<!DOCTYPE html>
<html lang="en">
	<head>
		<meta charset="utf-8" />
		<link rel="icon" href="/favicon.ico" />
		<meta name="viewport" content="width=device-width, initial-scale=1" />
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bulma@0.9.1/css/bulma.min.css">
    %svelte.head%
	</head>
	<body>
		<div id="svelte">%svelte.body%</div>
	</body>
</html>
```

Once added, you can use any of the classes from the [Bulma documentation](https://bulma.io/documentation/) to style your HTML.

Here's an example of styling a `Header` component.

```html
<header class="hero">
  <div class="hero-body">
    <img class="image is-64x64" src="logo.png" alt="Site logo">
    <h1 class="title">Main heading</h1>
  </div>
</header>
```

You'll notice that there's no `style` section or actual CSS here - that's because it's already been written by the Bulma developers. They've worked hard to make sure that Bulma works on almost all devices and is accessible to everyone. You're job becomes simply to link your HTML to the right CSS classes to get the look you want.

CSS frameworks are customisable too, but that's beyond the scope of this README. You can check out [Bulma's customisation](https://bulma.io/documentation/customize/) if you're interested.