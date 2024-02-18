# DISCLAIMER

This is a fork of the original
[react-tailwindcss-datepicker](https://github.com/onesine/react-tailwindcss-datepicker)

In the original, some code contained optional chaining, and in the particular project where this
datepicker was needed:

-   React 16 had to be used
-   optional chaining wasn't being transpiled, so CRA was throwing an error
-   migrating from CRA to vite isn't an option
-   updating Babel or Node.js isn't an option

So (modifications from react-tailwindcss-datepicker 1.6.6 into this package):

-   The code was replaced from optional chaining to the traditional if() check or a ternary.
-   The babel.config.json file that had beed added to the .npmignore list and was missing has here
    been removed from .npmignore and added to the the root directory of this project.

# Info for THE ORIGINAL React Tailwindcss Datepicker

<p align="center">
    <a href="https://react-tailwindcss-datepicker.vercel.app/" target="_blank">
      <img alt="React Tailwindcss Datepicker" width="100" style="border-radius: 100%;" src="https://raw.githubusercontent.com/onesine/react-tailwindcss-datepicker/master/assets/img/calendar_logo.svg?raw=true">
    </a><br><br>
    A modern date range picker component for React using Tailwind 3 and dayjs. Alternative to Litepie Datepicker which uses Vuejs.
</p>

<div align="center">
    
[![npm version](https://img.shields.io/npm/v/react-tailwindcss-datepicker?style=flat-square)](https://www.npmjs.com/package/react-tailwindcss-datepicker)
[![npm downloads](https://img.shields.io/npm/dt/react-tailwindcss-datepicker?style=flat-square)](https://www.npmjs.com/package/react-tailwindcss-datepicker)
    
</div>

## Contents

-   [DISCLAIMER](#disclaimer)
-   [Info for THE ORIGINAL React Tailwindcss Datepicker](#info-for-the-original-react-tailwindcss-datepicker)
    -   [Contents](#contents)
    -   [Features](#features)
    -   [Documentation](#documentation)
    -   [Installation of React Tailwindcss Datepicker React 16](#installation-of-react-tailwindcss-datepicker-react-16)
        -   [Install via npm](#install-via-npm)
        -   [Install via yarn](#install-via-yarn)
    -   [Simple Usage](#simple-usage)
        -   [Tailwindcss Configuration](#tailwindcss-configuration)
    -   [Theming options](#theming-options)
    -   [PlayGround FOR THE ORIGINAL](#playground-for-the-original)
    -   [Contributing TO THE ORIGINAL](#contributing-to-the-original)
    -   [Official Documentation repo FOR THE ORIGINAL](#official-documentation-repo-for-the-original)
    -   [Thanks to](#thanks-to)
    -   [License](#license)

## Features

-   ✅ Theming options
-   ✅ Dark mode
-   ✅ Single Date
-   ✅ Single date use Range
-   ✅ Shortcuts
-   ✅ TypeScript support
-   ✅ Localization(i18n)
-   ✅ Date formatting
-   ✅ Disable specific dates
-   ✅ Minimum Date and Maximum Date
-   ✅ Custom shortcuts

## Documentation

Go to [full documentation](https://react-tailwindcss-datepicker.vercel.app/)

## Installation of React Tailwindcss Datepicker React 16

⚠️ React Tailwindcss Datepicker React 16 uses Tailwind CSS 3 (with the
[@tailwindcss/forms](https://github.com/tailwindlabs/tailwindcss-forms) plugin) &
[Dayjs](https://day.js.org/en/) under the hood to work.

### Install via npm

```
$ npm install react-tailwindcss-datepicker-react16
```

### Install via yarn

```
$ yarn add react-tailwindcss-datepicker-react16
```

Make sure you have installed the peer dependencies as well with the below versions.

```
"dayjs": "^1.11.6",
"react": "^16.13.0"
```

## Simple Usage

#### Tailwindcss Configuration

Add the datepicker to your tailwind configuration using this code

```javascript
// in your tailwind.config.js
module.exports = {
    // ...
    content: [
        "./src/**/*.{js,jsx,ts,tsx}",
        "./node_modules/react-tailwindcss-datepicker-react16/dist/index.esm.js"
    ]
    // ...
};
```

Then use react-tailwindcss-select in your app:

```jsx
import React, { useState } from "react";
import Datepicker from "react-tailwindcss-datepicker-react16";

const App = () => {
    const [value, setValue] = useState({
        startDate: new Date(),
        endDate: new Date().setMonth(11)
    });

    const handleValueChange = newValue => {
        console.log("newValue:", newValue);
        setValue(newValue);
    };

    return (
        <div>
            <Datepicker value={value} onChange={handleValueChange} />
        </div>
    );
};

export default App;
```

## Theming options

**Light Mode**

![Light Mode](https://raw.githubusercontent.com/onesine/react-tailwindcss-datepicker/master/assets/img/Screen_Shot_2022-08-04_at_17.04.09_light.png?raw=true)

**Dark Mode**

![Dark Mode](https://raw.githubusercontent.com/onesine/react-tailwindcss-datepicker/master/assets/img/Screen_Shot_2022-08-04_at_17.04.09_dark.png?raw=true)

**Supported themes**
![Theme supported](https://raw.githubusercontent.com/onesine/react-tailwindcss-datepicker/master/assets/img/Screen_Shot_2022-08-04_at_17.04.09_theme.png?raw=true)

**Teal themes example**
![Theme supported](https://raw.githubusercontent.com/onesine/react-tailwindcss-datepicker/master/assets/img/Screen_Shot_2022-08-04_at_17.04.09_teal.png?raw=true)

You can find the demo at [here](https://react-tailwindcss-datepicker.vercel.app/demo)

> **Info ON THE ORIGINAL**
>
> 👉 To discover the other possibilities offered by this library, you can consult the
> [full documentation](https://react-tailwindcss-datepicker.vercel.app/).

## PlayGround FOR THE ORIGINAL

Clone the `master` branch and run commands:

```sh
# Using npm
npm install && npm dev

# Using yarn
yarn install && yarn dev

```

Open a browser and navigate to `http://localhost:8888`

## Contributing TO THE ORIGINAL

See
[CONTRIBUTING.md](https://github.com/onesine/react-tailwindcss-datepicker/blob/master/CONTRIBUTING.md)

## Official Documentation repo FOR THE ORIGINAL

[https://github.com/onesine/react-tailwindcss-datepicker-doc](https://github.com/onesine/react-tailwindcss-datepicker-doc)

## Thanks to

-   [React Tailwindcss Datepicker](https://github.com/onesine/react-tailwindcss-datepicker)
-   [Vue Tailwind Datepicker](https://vue-tailwind-datepicker.com/)
-   [React](https://reactjs.org/)
-   [Tailwind CSS](https://tailwindcss.com/)
-   [dayjs](https://day.js.org/)

## License

[MIT](LICENSE) Licensed. Copyright (c) Lewhe Onesine 2022.
