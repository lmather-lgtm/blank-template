
# Shopify Blank Template
A blank theme template to help you get started building Shopify themes from scratch.

## Target Audience
**This template is for developers who want to create their own Shopify theme with Liquid from *scratch*.**

If you want to start with a small template that comes with some dummy data check out the [Theme Kit Starter](https://shopify.dev/docs/themes/tools/theme-kit/getting-started). Check out the [Shopify-CLI Dawn template tutorial](https://shopify.dev/docs/themes/getting-started/create) if you want a complete and optimised template with tutorial.

If you want to build a custom web storefront and you are familiar with React you might want to check out [Hydrogen](https://hydrogen.shopify.dev/).

If you want to build your own custom frontend, app or game with your own tools and frameworks, check out the [Shopify Storefront API](https://shopify.dev/docs/api/storefront).

## Getting Started
This section will show you how to create your own copy of this template and link it to your Shopify store so you can start building immediately.

### Prerequisites 
This guide is editor agnostic, although [Visual Studio Code](https://code.visualstudio.com/) is recommended. You should also have the [Shopify CLI](https://shopify.dev/docs/themes/tools/cli/install) and [Theme Kit](https://shopify.dev/docs/themes/tools/theme-kit/getting-started) installed for convenience. Furthermore you should also have Git installed and posses some [basic Git skills](https://www.atlassian.com/git), as well as knowledge of HTML, CSS, JavaScript and Liquid.

### Step by step setup guide
 1. **[Create a copy](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-repository-from-a-template#creating-a-repository-from-a-template)** of the template repository

 2. **[Clone](https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository)** the repository that you just created and open it in the IDE of your choice

 3. **Replace** the data in the `config/schema_settings.json` with your own data<br>
 *You can keep the `name` field as is but replace the `theme_name`, `theme_version`, `theme_author`, `theme_documentation_url` and `theme_support_url` with your own data.*

 4. **Commit and push your changes** to your GitHub repository

 5. **[Follow Shopify's Tutorial](https://shopify.dev/docs/themes/tools/github/getting-started)** on how to connect to and publish from your GitHub repository

#### Update the shop on save (recommended)
1. **Create Access** to your store with [Theme Access](https://apps.shopify.com/theme-access) and copy the generated password

3. **Open a terminal window in your project's root folder**

4. **Get the theme id with Theme Kit**
```bash
theme get --list --password=[yourPassword] --store=[yourStore]
```
`yourPassword`: The password you just created from Theme Access<br>
`yourStore`: the domain of your store usually in the format yourstore.myshopify.com

5. **Create the config.yml file**
```bash
theme get  --password=[yourPassword] --store=[yourStore] --themeid=[yourThemeId]
```
`yourThemeId`: The theme id (in [...])that you get when you run the previous step
> This step will create a `config.yml` file in your project's root directory right next to your `.gitignore` file and the `README.md`. This file **contains sensitive information** so make sure you don't publish it into a public Git repository. You can also add it to the `.gitignore` file.

6. **Update the store on file change**
```bash
theme watch
```

Make sure that your theme is published and now you should be able to see your development store update after you make changes and save the changed file. You can stop the running command with `CTRL + C`.

## Bugs, Issues, Questions, etc.
If you find any bugs, issues, other problems or you have questions when working with this template, please [file an issue](https://github.com/JanTrichter/shopify-blank-theme-template/issues/new) in this repository.