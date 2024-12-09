# full_stack_Installation

## Client

```
npm create vite@latest client -- --template react
```

```
npm install react-router-dom localforage match-sorter sort-by
npm install -D tailwindcss postcss autoprefixer
npx tailwindcss init -p
npm i -D daisyui@latest
npm install react-icons --save

```

### TAILWIND SETTINGS

### tailwind.config.js

```
/** @type {import('tailwindcss').Config} */
export default {
  content: [
    "./index.html",
    "./src/**/*.{js,ts,jsx,tsx}",
  ],
  theme: {
    extend: {},
  },
  plugins: [],
}
```

### index.css

```
@tailwind base;
@tailwind components;
@tailwind utilities;
```

### Font 

```
/* poppins */
@import url('https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');

/* anton  */
@import url('https://fonts.googleapis.com/css2?family=Anton+SC&display=swap');

.font-poppins{
    font-family: "Poppins", sans-serif;
}
.font-anton{
    font-family: "Anton SC", sans-serif;
}
```

## Server

```
npm init -y
npm i express cors mongodb dotenv

```

## BASIC SETTINGS

```
    //Header
const express = require('express');
const cors = require('cors');
const app = express();
const port = process.env.PORT || 5001;

    // Middleware
app.use(cors());
app.use(express.json());

//---------------------------------------------------
// Footer
//___________________________________________________

app.get('/', (req, res) => {
    res.send('Server Running...');
})

app.listen(port, () => {
    console.log(`Server Running...${port}`);
})

```
