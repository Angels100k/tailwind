step 1. terminal do 
```
npm install -D tailwindcss
```
step 2. create tailwind.config.js
add this code in tailwind.config.js
```
/** @type {import('tailwindcss').Config} */
module.exports = {
    content: ["./**/*.{html,js}"],
    theme: {
      extend: {},
    },
    plugins: [],
  }
```

step 3, create css file "/src/index.css"
and add this code in it
```
@tailwind base;
@tailwind components;
@tailwind utilities;
```

step 4, create a script in package.json
```
  "scripts": {
    "dev": "npx tailwindcss -i ./src/input.css -o ./dist/output.css --watch"
  }
```

step 5, add this code in index.html
```
<link href="/dist/output.css" rel="stylesheet">
```
step 6, run this command in terminal
```
npm run dev
```
step 7, add this code in index.html
start using tailwindcss
```
  <h1 class="text-3xl font-bold underline">
    Hello world!
  </h1>
  ```