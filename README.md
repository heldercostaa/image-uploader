<div align="center">

![Language](https://img.shields.io/badge/language-typescript-yellow?logo=typescript&logoColor=white)
[![React](https://img.shields.io/badge/react-222?logo=react)](https://react.dev)
[![TailwindCSS](https://img.shields.io/badge/tailwindcss-222?logo=tailwindcss&logoColor=06B6D4)](https://tailwindcss.com)
[![Vite](https://img.shields.io/badge/vite-222?logo=vite&logoColor=646CFF)](https://vitejs.dev)
[![Maintainer](https://img.shields.io/badge/maintainer-%40heldercostaa-teal?logo=superuser&logoColor=white)](https://github.com/heldercostaa)
[![LinkedIn](https://img.shields.io/badge/linkedin-blue.svg?logo=linkedin)](https://linkedin.com/in/heldercostaa/)

<br />
<a href="#">
  <img src="./public/favicon.svg" alt="Logo" width="80" height="80">
</a>
<h3 align="center" style="font-size: 3em;">Image Uploader</h3>
<p align="center">
  Upload, compress, and manage images with a polished floating widget UI.
  <br />
  <a href="#local-setup-instructions"><strong>Run the project locally »</strong></a>
  <br />
  <br />
  <a href="https://github.com/heldercostaa/image-uploader-api">API Repository</a>
  ·
  <a href="https://github.com/heldercostaa/image-uploader-api#api-reference">API Reference</a>
</p>
</div>

> [!NOTE]
> This project depends on a backend upload endpoint running at `http://localhost:3333/uploads`. If the app is not connected to a live backend, you can still run the frontend locally by following the instructions in the [Local Setup Instructions](#local-setup-instructions) section.

<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#features">Features</a>
    </li>
    <li>
      <a href="#local-setup-instructions">Local Setup Instructions</a>
    </li>
  </ol>
</details>

## About The Project

<div align="center">
  <img src="./docs/1. Uploading.gif" alt="Image Uploader screenshot" style="width: 95%; border-radius: 5px;"/>
</div>
<br />

This is a personal frontend project focused on building a refined image upload experience. The application accepts image files, compresses them in the browser to `.webp`, uploads them to a backend storage endpoint, and provides feedback through animated progress states and per-file actions.

The goal of the project is to explore practical frontend patterns with React, TypeScript, Radix UI, Motion, and Tailwind CSS while keeping the experience compact and visually polished.

### Built With

[![React](https://img.shields.io/badge/React-222?logo=react)](https://react.dev)
[![TypeScript](https://img.shields.io/badge/TypeScript-222?logo=typescript)](https://www.typescriptlang.org)
[![Vite](https://img.shields.io/badge/Vite-222?logo=vite&logoColor=646CFF)](https://vitejs.dev)
[![TailwindCSS](https://img.shields.io/badge/TailwindCSS-222?logo=tailwindcss&logoColor=06B6D4)](https://tailwindcss.com)
[![Radix UI](https://img.shields.io/badge/Radix%20UI-222?logo=radixui)](https://www.radix-ui.com)
[![Axios](https://img.shields.io/badge/Axios-222?logo=axios&logoColor=5A29E4)](https://axios-http.com)
[![Motion](https://img.shields.io/badge/Motion-222)](https://motion.dev)

## Features

- Drag-and-drop support for one or more image uploads
- Native file picker fallback
- Client-side compression to `.webp` before upload
- Per-file progress tracking
- Global upload progress indicator
- Retry failed uploads
- Cancel in-progress uploads
- Copy uploaded file URL to clipboard
- Download uploaded/compressed file
- Animated collapsible widget interface

## Local Setup Instructions

1. **Backend Endpoint**: Ensure you have a backend server exposing the upload route below:

    ```http
    POST http://localhost:3333/uploads
    ```

    The frontend expects a JSON response in this format:

    ```json
    {
      "url": "https://your-storage-url.com/file.webp"
    }
    ```
  > [!TIP]
  > For more details on how to setup the backend, follow the [API Local Setup Instructions](https://github.com/heldercostaa/image-uploader-api#local-setup-instructions).

2. **Install Dependencies**: Install Dependencies: Navigate to the project directory and install the necessary dependencies:

   ```bash
   cd image-uploader
   pnpm install
   ```

3. **Run Development Server**: Start the Vite development server:

   ```bash
   pnpm dev
   ```
