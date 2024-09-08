# Supercharging VS Code: Customizing Beyond Themes with CSS & JS

**Visual Studio Code (VS Code)** is a popular and flexible code editor. While themes and extensions help improve the interface, what if you could **take it further**? In this post, I’ll show you how to push VS Code's customization beyond its themes using **CSS and JavaScript**. Whether it's removing clutter, adding custom fonts, or tweaking UI elements, I’ll guide you through creating a workspace that fits your needs perfectly.

## Key Insights 💡
- VS Code's flexibility allows for deep customization beyond themes and extensions.
- Custom CSS and JS can significantly alter VS Code's appearance and functionality.
- Performance impact is minimal, mainly affecting initial load time.
- Customization can enhance focus and productivity, especially on smaller screens.
- Experimenting with fonts, themes, and custom UI elements can create a personalized coding environment.
- Advanced users can leverage Developer Tools for precise modifications.

## Table of Contents 📚
- [Why I Use VS Code](#why-i-use-vs-code)
- [Customization Goals](#customization-goals)
- [Using the Custom CSS and JS Loader Extension](#using-the-custom-css-and-js-loader-extension)
- [Customizing Fonts, Themes, and Icons](#customizing-fonts-themes-and-icons)
- [Changing Keybindings](#changing-keybindings-and-shortcuts)
- [Advice for Developers](#final-thoughts-and-advice-for-developers)

## Resource Quick Links 🔗
- [My GitHub Repository](https://github.com/mohankumarpaluru/VSCodeCustomConfigs) (Configs & Settings)
- [Custom CSS and JS Loader](https://marketplace.visualstudio.com/items?itemName=be5invis.vscode-custom-css) (VS Code Extension)
- [Recommended Fonts](https://github.com/mohankumarpaluru/VSCodeCustomConfigs#fonts) (Monospace, Geist Mono, JetBrains Mono, Fira Code)


## Why I Use VS Code

I’ve experimented with a variety of editors—**Sublime Text, Notepad++, PyCharm, Atom, VSCodium**, and the newer **Zed Editor**. Although **PyCharm** was great for Python, it felt **heavy** and lacked support for other languages in the community edition. **VSCodium**, while telemetry-free and lighter than VS Code, required too much effort to configure.

In the end, **VS Code** emerged as my top choice due to its:
- **Broad language support**
- **Rich ecosystem of themes and extensions**
- **Responsive and lightweight feel**

However, there were still elements I didn’t need, especially when coding on my **small-screen laptop** without access to a monitor. That’s why I decided to dig deeper into customizations that would streamline my workflow.


## Customization Goals

While VS Code is highly customizable out of the box, it still has **clutter** I rarely use. My goal was to:
1. **Reduce the clutter**: Hide elements like the **Activity Bar**, **Minimap**, and **Status Bar** that I don’t always need.
2. **Create a focused environment**: When working on a small screen, less is more. By hiding UI elements and focusing solely on the code, I can maximize screen space.
3. **Personalize the interface**: Apply custom **fonts, tooltips, and icons** to make the editor feel like my own space.

## Using the Custom CSS and JS Loader Extension

To get started, I used the **Custom CSS and JS Loader** extension, which lets you inject custom stylesheets and scripts into VS Code as its **built using Electron** (a framework based on HTML, CSS, and JavaScript),

### Step 1: Install the Extension
Install it via the **VS Code Marketplace** by searching for "Custom CSS and JS Loader" or through this [link](https://marketplace.visualstudio.com/items?itemName=be5invis.vscode-custom-css).

### Step 2: Configure Custom CSS and JS
Next, you need to point VS Code to your custom CSS and JS files by adding paths in the `settings.json` file:

1. Open the Command Palette (`Ctrl + Shift + P`).
2. Type `Open User Settings (JSON)` and press Enter.
3. Add the following paths for your CSS and JS files:

```json
"vscode_custom_css.imports": [
    "file:///C:/path-to-your/custom-vscode.css",
    "file:///C:/path-to-your/vscode-script.js"
]
```

4. Save the file and reload VS Code.
5. Use the Command Palette to enable your custom files by typing `Enable Custom CSS and JS`.

### Customise the CSS and JS by Inspecting Elements with Developer Tools

Since VS Code is built using Electron, you can inspect and modify its elements just like a web page:

1. Open **Developer Tools** by typing `Toggle Developer Tools` in the Command Palette.
2. Right-click on elements you want to modify (e.g., tooltips, command palette) and inspect their CSS classes.
3. Apply your custom styles in your CSS file to change the appearance of these elements.

---
> [!TIP]
> **Customizing the Coding Editor**
> | Before | After |
> |--------|-------|
> | ![Before](https://raw.githubusercontent.com/mohankumarpaluru/VSCodeCustomConfigs/main/screenshots/code_before.png) | ![After](https://raw.githubusercontent.com/mohankumarpaluru/VSCodeCustomConfigs/main/screenshots/code_after.png) |
>
> You can completely change how the editor looks by altering the font styles, removing unnecessary elements, and adding tooltips with cleaner designs.
>
> **Custom Command Palette**
> | Before | After |
> |--------|-------|
> | ![Before](https://raw.githubusercontent.com/mohankumarpaluru/VSCodeCustomConfigs/main/screenshots/command_pallate_before.png) | ![After](https://raw.githubusercontent.com/mohankumarpaluru/VSCodeCustomConfigs/main/screenshots/command_pallate_after.png) |
>
> I customized the **Command Palette** to have a more centered appearance with a blurred background, making it look sleek and modern.
>
> **Revamping the Blank Page**
> | Before | After |
> |--------|-------|
> | ![Before](https://raw.githubusercontent.com/mohankumarpaluru/VSCodeCustomConfigs/main/screenshots/blank_icon_before.png) | ![After](https://raw.githubusercontent.com/mohankumarpaluru/VSCodeCustomConfigs/main/screenshots/blank_icon_after.png) |
>
> Instead of the default VS Code logo, I replaced it with custom SVG artwork from my tech stack. This adds a personal touch whenever there are no open files.

## Customizing Fonts, Themes, and Icons

To further enhance the look and feel, I suggest experimenting with fonts, themes, and icon packs. Here are my favorites:

### Fonts:
- **[Monospace](https://monaspace.githubnext.com/)** by GitHub Next
- **[Geist Mono](https://vercel.com/font)** by Vercel
- **[JetBrains Mono](https://www.jetbrains.com/lp/mono/)**
- **[Fira Code](https://github.com/tonsky/FiraCode)**

### Themes:
- **Catppuccin**
- **Monokai Pro** (Filter Octagon)

### Icons:
- **Monokai Pro Icon Pack**
- **Material Theme Icons** by Equinusocio

In my setup, I use a combination of these fonts along with the **Monokai Pro theme** for a polished, cohesive look.


## Changing Keybindings and Shortcuts

Custom keybindings allow you to toggle certain UI elements without cluttering your screen. Here are a few shortcuts I added to my workflow:

- **Activity Bar Toggle**: `Alt + B`
- **Minimap Toggle**: `Ctrl + M Ctrl + M`
- **Menu Bar Toggle**: `Alt + M`

To edit or add keybindings:
1. Open the Command Palette and type `Open Keyboard Shortcuts (JSON)`.
2. Paste your custom keybindings or download my config file from GitHub for an instant setup.

You can also place these keybindings directly into `%APPDATA%/Code/User` for easier access.

## Final Thoughts and Advice for Developers

Customizing VS Code can greatly enhance your coding experience. **For beginners**, start with fonts, icons, and themes to improve readability and aesthetics. **Advanced users** can explore CSS and JS modifications for more profound changes.

The **goal is to boost productivity and create a comfortable coding environment**. Experiment with different customizations to find what works best for your workflow.

[My GitHub repository](https://github.com/mohankumarpaluru/VSCodeCustomConfigs) includes all custom settings, CSS, JS, and keybindings used in this guide. Feel free to use it as a starting point for your own customizations.

For a visual guide to this customization process, you can check out [this helpful video](https://www.youtube.com/watch?v=9_I0bySQoCs) that inspired the customizations used in this article.

Remember, the best setup is one that helps you focus on your code. Happy coding!
