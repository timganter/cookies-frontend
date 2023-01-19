# What is this? 

This is a frontend built on a bare bones [SvelteKit](https://kit.svelte.dev/) install for testing reading and writing cookies to a backend. Originally developed for communicating and testing an AdonisJs backend for testing reading/writing cookies. Here is an AdonisJs repo to test with 👉 [https://github.com/timganter/cookies](https://github.com/timganter/cookies). 

# Installation

1. `npm install`
1. `npm run dev`

# Details

- You should see two buttons on the homepage. One for Baking (writing) a cookie and one for Eating (reading) a cookie.
- Check out `routes/+page.ts` for implementation details. 
- Clicking the Bake Cookie button will make a fetch call to http://localhost:3333/bake-cookie which should be a backend that writes a cookie.
- Clicking the Eat Cookie button will make a fetch call to http://localhost:3333/eat-cookie which should be a backend that reads and returns the value of the cookie.
