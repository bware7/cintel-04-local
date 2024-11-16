# cintel-04-local
## Bin Ware

## Overview

This project showcases how to build, test, and publish an interactive web app using PyShiny and GitHub Pages. The app allows data exploration of the Palmer Penguins dataset, featuring interactive visualizations, tables, and filtering options.

## Objectives
    1. Set up a GitHub repository and clone it locally.
    2. Create and manage a project-specific Python virtual environment.
    3. Develop an interactive Shiny app (penguins/app.py).
    4. Build and test the app locally.
    5. Deploy the app to GitHub Pages.

## Setup Process

**Step 1: Repository and Environment Setup** 
    
1.Create and Clone Repository:
```bash
git clone <repository-url>
```
2.Set Up Virtual Environment:
```bash
python -m venv .venv
.\.venv\Scripts\activate
```
3.Install Dependencies:
```bash
pip install -r requirements.txt
```


**Step 2: Develop and Test the App** 

1.Run the Shiny App:
```bash
shiny run --reload --launch-browser penguins/app.py
```
2.Test Interactivity:
    - Verify that all features, visualizations, and filters work as expected.


**Step 3: Build and Deploy the App** 

1.Export to Static Assets:
```bash
shiny static-assets remove
shinylive export penguins docs
```
2.Test Locally:
```bash
py -m http.server --directory docs --bind localhost 8008
```
3.Commit and Push to GitHub:
```bash
git add .
git commit -m "message"
git push -u origin main
```
4.Enable GitHub Pages:
    - In the GitHub repository settings: Go to Pages and set the branch to main, with the source as the docs/ folder.


**Step 4: Customize** 

1.Change Browser Tab Title:
    - Edit docs/index.html and update the <title> tag.
2.Add a Favicon (Optional):

    - Add a favicon.ico file to the docs folder and link it in index.html:
```bash
<link rel="icon" type="image/x-icon" href="./favicon.ico">
```

## Features
- Dynamic visualizations with Plotly and Seaborn.
- Reactive filtering by species and attributes.
- Tables, grids, and summary statistics for data exploration.
- Fully static deployment via Shinylive and GitHub Pages.

## Acknowledgments
- Special thanks to ChatGPT for assistance in troubleshooting, code development, and crafting this documentation.