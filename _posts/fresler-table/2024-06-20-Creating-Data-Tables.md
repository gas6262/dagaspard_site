---
layout: post
title:  "How To Create A Data Table In React In 3 Easy Steps"
description:  "Learn the simplest way to display a beautiful data table in your React App"
featured: true
author: david
tags: [react, js, data, javascript, freslertable]
image: assets/images/fresler-table.png
---

<iframe width="420" height="315" src="http://www.youtube.com/embed/tQskpxX32So" frameborder="0" allowfullscreen></iframe>


Tired of using underwhelming table libraries or building them from scratch?  In this article, we'll guide you through the simplest method to display a stunning data table in your React app. Whether you're a beginner looking to grasp the basics or a seasoned developer aiming to streamline your workflow, you'll find practical insights and easy-to-follow steps here. We'll explore the use of popular libraries, essential components, and best practices to ensure your data tables not only look great but also perform efficiently.

If you get lost, don't worry! You can clone the example from the [FreslerTable example repo](https://github.com/gas6262/fresler-table-examples/tree/main/examples/simple-table).

By the end of this tutorial, you'll have a solid understanding of how to add a data table React project, customize its appearance to match your app's design, and handle data dynamically. Let's dive in and transform the way you display data in your React applications!

## 1. Install The Table Library

If you don't already have a React app that you want to work with, use [this tutorial](https://react.dev/learn/start-a-new-react-project) to create a basic "Hello World" app.

Once you have your app created, add `@fresler/fresler-table` to your package.json file using npm.

```bash
npm install @fresler/fresler-table --save
```

You must also remove `<React.StrictMode>` from your react app if present. This component prevents the drag and drop functionality of the table library from working correctly. The component reference may be located in your `index.js` or `main.tsx` file. Remove the reference from your index.js file (or wherever the reference may be) like so:

src/index.jsx
```js
import React from "react";
import ReactDOM from "react-dom/client";
import App from "./App.tsx";
import "./index.css";

ReactDOM.createRoot(document.getElementById("root")!).render(
  // <React.StrictMode>
  <App />,
  // </React.StrictMode>,
);
```

## 2. Set Up Your Data

To use the FreslerTable library, you must format your data in json format and also specify your columns using json format. If you wish to use dummy data, feel free to use [this example data](https://github.com/gas6262/fresler-table-examples/blob/main/examples/simple-table/src/data.jsx) and these example [column definitions](https://github.com/gas6262/fresler-table-examples/blob/main/examples/simple-table/src/columns.jsx). Simply add `data.jsx` and `columns.jsx` to your source folder containing your App.tsx or App.jsx.

src/data.jsx
```js
export const data = [
    {
        id: '848e6002-8a92-447d-951b-1ffd5e695578',
        full_name: 'Sig Jeannel',
        job_title: 'Human Resources Assistant III',
        country: 'US',
        is_online: true,
        rating: 3,
        target: 100,
        budget: 47601,
        phone: '(936) 9429601',
        address: '138 Buhler Avenue',
        img_id: 1,
        gender: 'M',
        interim_title: 'Creator',
        assignee: 'janedoe@gmail.com',
        duedate: '2023-10-12T07:00:00.000Z',
    },
    {
        id: '19d18d40-0e64-4837-9420-92130a0ed253',
        full_name: 'Shelden Greyes',
        job_title: 'Operator',
        country: 'GB',
    
    ...
```

src/columns.jsx
```js
export const columns = [
    {
      displayName: 'Name',
      field: 'full_name',
      type: 'string',
      editable: true,
    },
    {
      displayName: 'Job Title',
      field: 'job_title',
      type: 'string',
      editable: true,
    },
    
    ...
```

If you have your own data, format it in json format and create the column definitions.

## 3. Display Your Table

Now you're ready to display your data in your data table. Add the necessary library and data imports to your `App.tsx`.

```js
import '@fresler/fresler-table/css';
import { FreslerTable } from '@fresler/fresler-table';

import { data } from './data';
import { columns } from './columns.jsx';
```

Then, update your App.tsx to instantiate your new table using the imported FreslerTable component.

```js
<FreslerTable
    initData={tableData}
    initCols={columns}
    updateData={setTableData}
```

Your app.tsx should look something like this when complete.

src/App.tsx
```js
import { useState } from 'react';
import reactLogo from './assets/react.svg';
import viteLogo from '/vite.svg';
import './App.css';

import '@fresler/fresler-table/css';
import { FreslerTable } from '@fresler/fresler-table';

import { data } from './data';
import { columns } from './columns.jsx';

function App() {
  const [tableData, setTableData] = useState(data);

  const appendData = (newData) => {
    setTableData([...tableData, ...newData]);
  };

  return (
    <>
      <div className="p-3">
        <div className="row mt-3">
          <FreslerTable
            initData={tableData}
            initCols={columns}
            updateData={setTableData}
          />
        </div>
      </div>
    </>
  );
}

export default App;

```

Start your app and you should now see your data rendered in a simple table.

![Fresler Table]({{ site.baseurl }}/assets/images/fresler-table.png)

# Conclusion

That was easy! 🥳

Great job creating a simple and beautiful data table in your React app. FreslerTable has many additional features that can help take your site to the next level. Learn more at [freslertable.com](freslertable.com). If you have any issues with the library, please feel free to create a github issue on the [FreslerTable github](https://github.com/gas6262/fresler-table-examples/issues).