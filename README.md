<div align="center">
	<img src="https://i.imgur.com/uphwMrZ.jpg" title="Yuu" alt="Yuu" />
</div>

# Yuu

A VuePress theme that supports multiple color themes and some other useful features. Heavily based off of the default VuePress theme.

## Installation

You can add Yuu to your current VuePress project by running:

```bash
yarn add vuepress-theme-yuu

# or if you prefer npm
npm install vuepress-theme-yuu
```

## Features/configuration

![Yuu user settings dropdown menu](https://i.imgur.com/FKz0hI3.png)

Everything that's supported in the 0.14.1 version of the default VuePress theme is supported on Yuu. Updates will be made occassionally to try to keep up with the default's themes features and CSS and etc.

Below is a list of the additional configurable features Yuu has to offer.

### Dark theme

Yuu, by default, comes with an option to allow users to switch to a dark theme. You can disable this via the `disableDarkTheme` option.

```js
module.exports = {
	themeConfig: {
		yuu: {
			disableDarkTheme: true,
		},
	},
};
```

### Color themes

Yuu currently supports 3 color themes: the default (green) theme, a blue theme, and a red theme. If you want to include any of the non-default themes, you'll need to be explicit about which ones.

```js
module.exports = {
	themeConfig: {
		yuu: {
			colorThemes: ['blue', 'red'],
		},
	},
};
```

#### Forced color themes per page

You can force themes on a per page basis as well. Using YAML front matter on the page(s) you want to display a specific theme:

```md
---
forceTheme: blue
---
```

#### Disallowing forced themes from being ignored

Users will still be able ignore forced themes via the user settings dropdown menu. You can disable this via the `disableThemeIgnore` option.

```js
module.exports = {
	themeConfig: {
		yuu: {
			disableThemeIgnore: true,
		},
	},
};
```
