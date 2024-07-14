
# Frontend Guide

## Introduction

Welcome to the frontend of the MERN Book Store App. This application serves as the client-side component of a book store, providing a user-friendly interface for browsing, purchasing, and managing books. 

## Techstack

The frontend of this application utilizes the following technologies:<br>
<center><img src="https://go-skill-icons.vercel.app/api/icons?i=react,redux,tailwind,vite,javascript,html,css" /></center><br>

- **React**: A JavaScript library for building user interfaces.<br>
- **Redux**: A predictable state container for JavaScript apps.
- **Tailwind CSS**: A utility-first CSS framework for rapidly building custom designs.
- **Vite**: A build tool that aims to provide a faster and leaner development experience for modern web projects.
- **JavaScript**: The programming language of the web.
- **HTML5**: The standard markup language for creating web pages.
- **CSS3**: The style sheet language used for describing the presentation of a document written in HTML or XML.

## Code Workflow

The frontend code is structured as follows:

1. **Entry Point**: `index.html` and `src/main.jsx` are the main entry points of the application. They set up the React app and render the root component.

2. **Configuration**: Configuration files such as `vite.config.js` and `postcss.config.js` hold the configuration settings for the development server and PostCSS, respectively.

3. **Components**: The `src/components` directory contains reusable React components that make up the user interface.

4. **Pages**: The `src/pages` directory includes the different pages of the application, such as the home page, product pages, and user account pages.

5. **Redux**: The `src/store` directory contains the Redux store setup and slices for managing application state.

6. **Styling**: Tailwind CSS is configured in `tailwind.config.js` and used throughout the components for styling.

7. **Public Assets**: Static assets like images and fonts are stored in the `public` directory.

## Setup

To set up and run the frontend of the MERN Book Store App, follow these steps:

1. **Clone the Repository**: Clone the repository to your local machine.

   ```bash
   git clone <repository-url>
   cd frontend
   ```

2. **Install Dependencies**: Install the required dependencies using npm.

   ```bash
   npm install
   ```

3. **Run the Development Server**: Start the Vite development server.

   ```bash
   npm run dev
   ```

   The development server should now be running, and you can view the application in your browser at `http://localhost:3000`.

## Errors and Solutions

Here are some common errors you might encounter during setup and their solutions:

| Error                            | Reason                                          | Solution                                                                                                                                                       |
|----------------------------------|-------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Module not found**             | Missing module or incorrect import path         | Verify the module is installed and the import path is correct. If the module is not installed, run `npm install <module_name>`.                                 |
| **SyntaxError**                  | Syntax error in the JavaScript/JSX code         | Check the code syntax and fix any errors. Refer to the error message for specific details about the location of the error.                                      |
| **CORS Policy Error**            | Cross-origin requests are blocked               | Ensure the backend server has CORS enabled and properly configured to allow requests from the frontend's origin.                                                |
| **Build Error**                  | Issues during the build process                 | Check the error message for details and fix any issues in the code or configuration files. Ensure all necessary dependencies are installed.                     |
| **Network Error**                | Issues with API requests                        | Verify that the backend server is running and the API endpoints are correct. Check network connectivity and the browser's console for error details.             |
| **Tailwind CSS not applying**    | Tailwind CSS classes not being applied correctly| Ensure Tailwind CSS is properly configured and included in the project. Check `tailwind.config.js` and verify that the paths to your template files are correct. |
| **Hot Module Replacement (HMR) Error** | Issues with Vite's HMR                         | Restart the development server. If the issue persists, clear the browser cache or try accessing the app in a private/incognito window.                          |
| **ESLint Errors**                | Code does not follow linting rules              | Fix the linting errors as indicated by the ESLint output. Configure `.eslintrc.cjs` if necessary to adjust the linting rules to your preference.                 |
| **PostCSS Plugin Error**         | Issues with PostCSS plugins                     | Check the `postcss.config.js` file and ensure all required PostCSS plugins are installed and correctly configured.                                              |
