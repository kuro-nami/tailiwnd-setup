## How to setup Tailwind CSS

Step 0: Create src folderand add index.html and script.js and input.css
and make sure PostCSS Language Support extension and tailwind intellisense are ON

Step 1: Run the following commands

```
npm install -D tailwindcss
npx tailwindcss init
```

Step 2: Update tailwind.config.js file to include this line:

```
content: ["./src/**/*.{html,js}"],
```

Step 3: add to input.css:

```
@tailwind base;
@tailwind components;
@tailwind utilities;
```

Step 4: Add this in head of html:

```
<link href="./output.css" rel="stylesheet">
Step 5: Run the following command:
```

npx tailwindcss -i ./src/input.css -o ./src/output.css --watch

```

```
