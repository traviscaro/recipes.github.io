# AnyList Import Guide

This guide explains how to use the recipe collection with AnyList's web import feature.

## How AnyList Import Works

AnyList can automatically import recipes from websites that include proper Schema.org Recipe markup. This site is specifically designed to be compatible with AnyList's import feature.

## Step-by-Step Import Process

### 1. Find the Recipe URL
- Navigate to https://traviscaro.github.io/recipes.github.io/
- Click on the recipe you want to import
- Copy the full URL from your browser's address bar
- Example: `https://traviscaro.github.io/recipes.github.io/recipes/chocolate-chip-cookies.html`

### 2. Import in AnyList
1. Open the AnyList app on your device
2. Go to the "Recipes" section
3. Tap the "+" button to add a new recipe
4. Select "Import from Web"
5. Paste the recipe URL
6. Tap "Import"

### 3. Review and Save
- AnyList will automatically extract:
  - Recipe name
  - Ingredients list
  - Instructions
  - Prep/cook times
  - Serving size
  - Description
- Review the imported data
- Make any necessary adjustments
- Save the recipe

## What Gets Imported

The Schema.org markup includes:

- **Recipe Name**: Main title
- **Description**: Brief overview
- **Prep Time**: Preparation time in minutes
- **Cook Time**: Cooking time in minutes
- **Total Time**: Combined time
- **Yield**: Number of servings or pieces
- **Ingredients**: Complete list with measurements
- **Instructions**: Step-by-step directions
- **Category**: Type of dish (dessert, main course, etc.)
- **Cuisine**: Cuisine type (American, Italian, etc.)
- **Keywords**: Searchable tags

## Troubleshooting

### Import Not Working?
- Make sure you're copying the complete URL
- Verify the URL starts with `https://traviscaro.github.io`
- Try refreshing the recipe page before copying the URL
- Check that you have a stable internet connection

### Missing Information?
- Some optional fields may not import if not included in the recipe
- You can manually add missing information after import
- Report any systematic issues with the recipe markup

### AnyList Alternatives
If you don't use AnyList, other recipe managers that support Schema.org import include:
- Recipe Keeper
- Paprika
- Copy Me That
- BigOven

## Creating AnyList-Compatible Recipes

When adding new recipes to this collection, ensure your HTML includes:

1. **Required JSON-LD structure** in the `<head>` section
2. **Proper Schema.org Recipe type** (`"@type": "Recipe"`)
3. **All essential fields** (name, ingredients, instructions)
4. **Proper time format** (ISO 8601 duration format like "PT15M" for 15 minutes)

See `recipe-template.html` for the complete structure needed for AnyList compatibility.