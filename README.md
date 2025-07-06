
# Vivaldi - Transparent & Glass UI

A simple yet powerful custom CSS script for the Vivaldi browser that provides a clean, modern aesthetic by making key UI elements transparent.

This theme makes the **Address Bar** and **Status Bar** fully transparent, and gives you two easy-to-switch options for the **Side Panel**: fully transparent or a beautiful "frosted glass" blur effect.


![image](https://github.com/user-attachments/assets/24c7c7fb-e4db-45f1-8496-464e961a8be5)


---

## Features

- **Transparent Address Bar:** The main toolbar containing the address and navigation buttons becomes completely transparent.
- **Transparent Status Bar:** The footer/status bar becomes completely transparent.
- **Configurable Side Panel:** Choose the style you prefer for the side panel with a simple code change:
    - **Option 1: Fully Transparent:** Makes the panel invisible until you hover over its contents.
    - **Option 2: Clear Glass Blur:** Gives the panel a "frosted glass" effect, blurring the content behind it.

## Installation

Follow these steps to apply this custom UI to your Vivaldi browser.

#### Step 1: Enable CSS Modifications in Vivaldi

You must first enable Vivaldi's experimental feature that allows loading custom CSS.

1.  Open Vivaldi and go to the following URL: `vivaldi://experiments`
2.  Find **"Allow for using CSS modifications"** and check the box to enable it.
3.  A restart of the browser may be required.



#### Step 2: Download and Place the CSS File

1.  Download the `main.css` file from this repository.
2.  Create a folder on your computer in a safe, permanent location (e.g., `Documents/Vivaldi CSS`).
3.  Place the downloaded `main.css` file inside this new folder.

#### Step 3: Tell Vivaldi Where to Find Your CSS

1.  In Vivaldi, go to **Settings > Appearance**.
2.  Scroll down to the **CUSTOM UI MODIFICATIONS** section.
3.  Click the **"Select Folder..."** button and choose the folder you created in the previous step (e.g., `Documents/Vivaldi CSS`).



#### Step 4: Restart Vivaldi

Close and reopen Vivaldi completely for the changes to take effect. Your UI should now have the new transparent theme!

---

## How to Customize the Panel Effect

This script is designed to be easily configurable. You can switch between a fully transparent panel and a glass blur panel by editing the `main.css` file.

**The rule is simple: Uncomment the style you want, and make sure the other one is commented out.** A block of code is "commented out" when it is surrounded by `/*` and `*/`.

### Option 1: Set Panel to Fully Transparent

To make the panel fully transparent, make sure the code looks like this:

```css
/* --- OPTION 1: FULLY TRANSPARENT PANEL --- */
/* Uncomment this block to make the side panel completely see-through. */

#panels-container,
.panel-group {
    background: transparent !important;
    border: none !important;
    box-shadow: none !important;
}


/* --- OPTION 2: CLEAR GLASS BLUR PANEL (DEFAULT) --- */
/* (Make sure Option 1 is commented out with /* ... */ if you use this one). */

/*

#panels-container,
.panel-group {
    /* ... css rules ... */
}

*/
```

### Option 2: Set Panel to Clear Glass Blur

To give the panel a frosted glass effect, make sure the code looks like this:

```css
/* --- OPTION 1: FULLY TRANSPARENT PANEL --- */
/* Uncomment this block to make the side panel completely see-through. */

/*

#panels-container,
.panel-group {
    background: transparent !important;
    border: none !important;
    box-shadow: none !important;
}

*/


/* --- OPTION 2: CLEAR GLASS BLUR PANEL (DEFAULT) --- */
/* Uncomment this block to give the side panel a clear, frosted glass effect. */

#panels-container,
.panel-group {
    /* The Substance: A very subtle, nearly-transparent background. */
    background-color: rgba(255, 255, 255, 0.1) !important;

    /* The Blur: This blurs the content behind the panel. */
    backdrop-filter: blur(40px) !important;

    /* The Edge: A subtle border to define the glass. */
    border: 1px solid rgba(255, 255, 255, 0.18) !important;

    /* Clean Up: Remove any leftover shadows. */
    box-shadow: none !important;
}
```

After editing the `main.css` file, **save it and restart Vivaldi** to see your changes.
