# EvilFlowersViewer - PDF Viewer based on pdf.js

# Introduction

EvilFlowersViewer is a PDF viewer based on pdf.js library that allows users to view and interact with PDF documents directly in the browser. This project is being developed by a university team, and aims to provide a reliable and efficient PDF viewer that is easy to use and customize.

# Features

- PDF document rendering directly in the browser
- Zoom in and out of documents
- Page navigation through a page thumbnail view
- Text search within documents

## Features Under Development

- Citation export
- Customizable user interface with themes
- Annotation tools for highlighting and commenting on text
- and more...

# Getting started

To get started with EvilFlowersViewer, follow these steps:

1. Install EvilFLowersViewerPackage:

```bash
npm install @evilflowers/evilflowersviewer
```

2. Import the Viewer component into your project:

```ts
import { Viewer } from '@evilflowers/evilflowersviewer'
import '@evilflowers/evilflowersviewer/dist/style.css'
```

3. Use Viewer component in your JSX:

```tsx
const MyPdfWrapper = (props) => {
  return <Viewer data={base64Data} />
}
```

## Demo

Check out our [demo](https://tp2022-t16.evilflowers.org/demo) for an interactive demo of EvilFlowersViewer. On the demo page, you can see how the project was developed through different sprints, with detailed documentation and descriptions of each sprint goal and task. You can also explore the different features of EvilFlowersViewer.

# Contributing

We welcome contributions from the community to help make EvilFlowersViewer even better. To contribute, please follow these steps:

1. Fork the EvilFlowersViewer repository
2. Create a new branch for your changes
3. Make your changes and commit them with a clear commit message
4. Push your changes to your forked repository
5. Create a pull request to merge your changes into the main EvilFlowersViewer repository

# Technical documentation

## Code structure in src folder

In src folder we have all neccesary sub-folders, tsx, css and ts files.
Main sub-folders:

- assets - svg icons used in our PDF Viewer
- examples_PDF - different types of PDFs. Mainly used for testing functionality
- lib - contains index.ts file and sub-folder for all components
- utils - sub-folder that contains helper functions, translation json files

## App.tsx

A React component that represents an application with a viewer for PDF files. It imports the **Viewer** component from a file located in the ./lib/components directory. The Viewer component is responsible for rendering the PDF data.

## Viewer.tsx

Is responsible for rendering a PDF file. The component takes a base64-encoded string of the PDF file as a prop (**data**) and converts it to binary format using a utility function called **base64ToBinary**.

The _Viewer_ component utilizes the useEffect and useState hooks from React. The first useEffect hook is responsible for setting the theme of the viewer based on the user's preference or the system's preferred color scheme. If the theme is set to 'dark' or if the user's system prefers a dark color scheme, the class 'dark' is added to the HTML element with the id 'evilFlowersViewer'. Otherwise, the 'dark' class is removed.

The second useEffect hook is triggered whenever the data prop changes. It converts the base64-encoded string to binary using the **base64ToBinary** utility function and sets the result to the documentData state variable.

The Viewer component renders a 'div' element. Inside this div, there is another 'div' element with a dynamic class based on the current theme. This inner 'div' represents the background of the viewer. If **documentData** is available, it renders the _Document_ component and passes the **data** prop, which contains the binary representation of the PDF.

## BottomBar Component

### BottomBat.tsx

### Preview.tsx

## Document Component
