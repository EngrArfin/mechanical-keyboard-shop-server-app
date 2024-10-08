## mechanical-keyboard-shop-server-app

# Project Description:

Mechanical Keyboard Shop Server App
The Mechanical Keyboard Shop Server App is a backend development project designed to support the operations of an online store specializing in mechanical keyboards. This project is built using Node.js for its runtime environment, Express.js for handling server-side logic and routing, Mongoose for interacting with MongoDB to manage data persistence, and TypeScript for adding type safety and improving code quality.

## Tech Stack

**Server:** TypeScript, Node, Express, MongoDB, Mongoose, Zod.....

(This project Client: React with Vite, TypeScript, Redux, RTK Query)

## Deployment Step By Step

npm create vite
Project Name: mechanical-keyboard-shop-client-app

√ Select a framework: » React
√ Select a variant: » TypeScript

cd mechanical-keyboard-shop-client-app

## Server Project Installation Step By Step

cmd
code .

command line---

```bash
  npm init -y
```

```bash
  npm install express
```

```bash
  npm install mongoose --save
```

```bash

  npm install typescript --save-dev

```

```bash

  npm i cors

```

```bash
  npm i dotenv
```

```bash
tsc init
```

```bash
"rootDir": "./src"
"outDir": "./dist"
```

app.ts

```bash
  const express = require('express')
const app = express()
const port = 3000

app.get('/', (req, res) => {
  res.send('Hello World!')
})

```

```bash
import express, { Application, Request, Response } from "express";
import cors from "cors";
const app: Application = express();
const port = 3000;

//parser

app.use(express.json());
app.use(cors());

app.get("/", (req: Request, res: Response) => {
  res.send("Hello World!");
});
console.log(process.cwd());
export default app;

//C:\Program2\mechanical-keyboard-shop-server-app\.env


```

server.ts

```bash

  app.listen(port, () => {
  console.log(`Example app listening on port ${port}`)
})

```

step-2 server.ts

```bash

import mongoose from "mongoose";
import config from "./app/config";
import app from "./app";

async function main() {
  try {
    await mongoose.connect(config.database_url as string);
    app.listen(config.port, () => {
      console.log(`Example app listening on port ${config.port}`);
    });
  } catch (err) {
    console.log(err);
  }
}

main();


```

step- arc/app/config index.ts

```bash
import dotenv from "dotenv";

import path from "path";

dotenv.config({ path: path.join((process.cwd(), ".env")) });

export default {
  port: process.env.PORT,
  database_url: process.env.DATABASE_URL,
};

```

.env

```bash
PORT = 5000
DATABASE_URL= mongodb+srv://mechanical-ms:mechanical12345@cluster0.xu7sm0d.mongodb.net/mechanical-keyboard-shop-server-app?retryWrites=true&w=majority&appName=Cluster0

```

```bash

```

## Run Project

![App Screenshot](c:\Users\DELL\Pictures\Screenshots\basic project.png)

#Project Basic Setup  
.env.local
.env.example

Src/
Assets/icons/images
Components/form/layout/ui
Config
Hooks
Lib
Pages
Redux
Routes
Styles
Utils

#Next

App.css delete
App.tsx. some clear
Index.css clear

## Running Tests

To run tests, run the following command

```bash
  npm run test
```

## If You want project clone and Run Locally

Clone the project

```bash
  git clone https://github.com/EngrArfin/mechanical-keyboard-shop-client-app.git
```

Go to the project directory

```bash
  cd mechanical-keyboard-shop-client-app
```

Install dependencies

```bash
  npm install
```

Start the server

```bash
  npm run start
```

--------------------The End----------------------
