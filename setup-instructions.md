## How to setup Tailwind CSS (Make sure you have downloaded latest version of node.js: https://nodejs.org/en)

Step 1: Create index.html and then create an src folder with script.js and input.css files.

Step 2: Open Terminal (Ctrl+`) and paste the following command and press enter (you will have to wait a few seconds for it to install packages):

```
npm install -D tailwindcss
```

Step 3: Now paste this line and press enter in the terminal:

```
npx tailwindcss init
```

Step 2: Go in tailwind.config.js file change the content: [ ] line to include this:

```
content: ["*.{html,js}"],
```

Step 3: Go to input.css and paste this:

```
@tailwind base;
@tailwind components;
@tailwind utilities;
```

Step 4: Paste the following command into terminal and press Enter:

```
npx tailwindcss -i ./src/input.css -o ./src/output.css --watch
```

Step 5: Paste this in head of index.html:

```
<link href="./src/output.css" rel="stylesheet">
```

Step 6: Now paste this in the first curly bracket in package.json file:

```
,
  "scripts": {
    "run": "npx tailwindcss -i ./src/input.css -o ./src/output.css --watch"
  }
```

Step 7: You need to keep the terminal running for tailwind to work, not infront - you can close it, but don't delete it, if you accidentally delete it, paste this and press enter:

```
npm run run
```

### Warning: Make sure that you do not make any changes to the .json files and dont change their location aswell as tailwind.config.js file's location or your tailwind might stop working.

## Installing Prettier in tailwindcss:

Step 1: Run the following command in terminal:

```
npm install -D prettier prettier-plugin-tailwindcss
```

Step 2: Create a file with name "prettier.config.js" and the following code to it:

```
module.exports = {
    plugins: ["prettier-plugin-tailwindcss"],
};
```

Step 3: Add this to the plugins: [] of your tailwind.config.js file: 

```
plugins: ["prettier-plugin-tailwindcss"],
```

### Done!
