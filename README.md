My Recipes Scheduler

"My Recipes Scheduler" is a web-based application designed to help you organize your recipes, plan your weekly meals, and automatically generate a corresponding grocery list. The app is built as a single HTML file that dynamically loads recipe data from a Google Sheets document, making recipe management easy and collaborative.
Features

    Recipe Management via Google Sheets:

        Recipes are managed directly within a Google Sheets file.

        Each sheet in the Google Sheets document represents a single recipe.

        The name of the sheet is used as the recipe's name.

        Recipe details (ID, default servings, personal score), ingredients (name, quantity, unit, and detailed nutritional information per 100g/ml), and procedure steps are entered in a structured, row-based format within each sheet.

    Dynamic Recipe Display:

        The app fetches and parses data from your Google Sheets using a Google Apps Script.

        Displays a browsable list of all your recipes.

        Shows calculated nutritional information per serving (calories, fat, saturated fat, carbs, sugars, protein, salt).

        Displays a 5-star rating (with quarter-star precision) based on your personal score (1-10 scale).

        Provides expandable sections for detailed ingredient lists, full recipe nutrition, and step-by-step procedures.

    Weekly Meal Planner:

        Allows you to create a meal plan for a customizable number of days (1-7).

        Assign recipes from your collection to breakfast, lunch, and dinner slots for each day.

        Specify the number of servings for each meal, enabling batch cooking planning.

        Dynamically calculates and displays the total calories for each day based on selected recipes and servings.

        Saves your weekly meal plan in your browser's localStorage for persistence.

    Automated Grocery List Generation:

        Summarizes all ingredients required for the recipes planned in your week menu.

        Scales ingredient quantities based on the number of servings specified for each meal.

        Provides a consolidated list for easy grocery shopping.

    User-Friendly Interface:

        Clean, modern design using Tailwind CSS.

        Responsive layout for use on desktop and mobile devices.

        Simple navigation between Recipes, Week Menu, and Groceries pages.

        Theme color: Dark Green.

How It Works

The application is a single index.html file. It uses JavaScript to:

    Fetch Data: Call a deployed Google Apps Script Web App URL.

    Process Data: The Google Apps Script reads your designated Google Sheets file, processes each sheet (recipe), and returns the data as a JSON object.

    Render Content: The HTML app then parses this JSON to dynamically display recipes, allow meal planning, and generate grocery lists.

    Local Storage: The weekly meal plan is saved locally in the user's browser.

Setup

    Google Sheets Document:

        Create a Google Sheets file.

        Structure each sheet as a recipe, following the specified row-based layout for metadata, ingredients (with nutritional info per 100g/ml), and procedure steps. The sheet name becomes the recipe name.

    Google Apps Script:

        Copy the provided Apps Script code into the script editor of your Google Sheets file (Extensions > Apps Script).

        Deploy the script as a Web App, ensuring:

            Execute as: "Me"

            Who has access: "Anyone"

        Copy the generated Web App URL.

    HTML Configuration:

        Open the index.html file of this application.

        Update the APPS_SCRIPT_WEB_APP_URL constant with the URL you copied from your deployed Google Apps Script.

    Hosting:

        Host the index.html file on a static web hosting service (e.g., GitHub Pages, Netlify, Vercel, Firebase Hosting).

Usage

Once set up and hosted:

    Navigate to the app's URL in your browser.

    Recipes Tab: Browse your recipes. Click on details to expand ingredients and procedure.

    Week Menu Tab: Select the number of days for your plan. Assign recipes and servings for breakfast, lunch, and dinner for each day.

    Groceries Tab: Click "Update & View Groceries List" (from the Week Menu page) to see a consolidated list of ingredients needed for your planned meals.

To add or modify recipes, simply edit your Google Sheets document. The app will fetch the latest data the next time it loads (or when refreshed).

This project demonstrates a simple yet effective way to manage dynamic content for a web application using Google Sheets as a user-friendly backend, facilitated by Google Apps Script.

_I created this webapp in close collaboration with Gemini._
