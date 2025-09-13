# recipe-importer

A place to publicly host recipe pages that I take pictures of, translate to Schema.org Recipe JSON-LD, and import with AnyList.

## Overview

This GitHub Pages site provides a simple way to host raw HTML recipe files that are compatible with AnyList import. All recipes include proper Schema.org Recipe JSON-LD markup for seamless integration with recipe management apps.

**Live Site:** https://traviscaro.github.io/recipe-importer/

## Features

- 📱 **AnyList Compatible**: All recipes include proper Schema.org Recipe JSON-LD markup
- 🌐 **Public Hosting**: Accessible via GitHub Pages at predictable URLs
- 📁 **Simple Upload**: Just add HTML files to the `recipes/` directory
- 🎨 **Clean Interface**: Modern, responsive design for easy reading
- 🔍 **Automatic Discovery**: Index page lists all available recipes

## How to Add a New Recipe

1. **Create an HTML file** with your recipe content and proper Schema.org markup
2. **Save the file** in the `recipes/` directory (e.g., `recipes/my-recipe.html`)
3. **Commit and push** the file to the repository
4. **Access your recipe** at `https://traviscaro.github.io/recipe-importer/recipes/my-recipe.html`

## Recipe HTML Template

Your HTML files should include:

- Proper Schema.org Recipe JSON-LD in the `<head>` section
- Clean, readable HTML structure
- Navigation back to the main index

See `recipes/chocolate-chip-cookies.html` for a complete example.

### Required Schema.org Fields for AnyList

Make sure your JSON-LD includes these fields:

```json
{
  "@context": "https://schema.org/",
  "@type": "Recipe",
  "name": "Recipe Name",
  "description": "Brief description",
  "prepTime": "PT15M",
  "cookTime": "PT30M",
  "totalTime": "PT45M",
  "recipeYield": "4 servings",
  "recipeIngredient": [
    "ingredient 1",
    "ingredient 2"
  ],
  "recipeInstructions": [
    {
      "@type": "HowToStep",
      "text": "Step 1 instructions"
    }
  ]
}
```

## AnyList Import Instructions

1. Copy the full URL of any recipe (e.g., `https://traviscaro.github.io/recipe-importer/recipes/chocolate-chip-cookies.html`)
2. Open AnyList and go to the Recipes section
3. Tap the "+" button and select "Import from Web"
4. Paste the URL and tap "Import"
5. AnyList will automatically extract the recipe data using the Schema.org markup

## File Structure

```
├── index.html              # Main page listing all recipes
├── _config.yml            # GitHub Pages configuration
├── recipes/               # Directory for recipe HTML files
│   └── chocolate-chip-cookies.html
└── README.md             # This file
```

## Local Testing

To test locally before pushing:

1. Install Jekyll: `gem install bundler jekyll`
2. Run: `bundle exec jekyll serve`
3. Open: `http://localhost:4000`

## Contributing

Feel free to submit pull requests with new recipes or improvements to the site structure!
