<div align="center">
	<img src="https://i.imgur.com/uphwMrZ.jpg" title="Yuu" alt="Yuu" />
</div>

# Yuu

A VuePress theme that supports multiple color themes and some other useful features. Extended upon the default VuePress theme with some adjustments.

## Installation

You can add Yuu to your current VuePress project by running:

```bash
yarn add vuepress-theme-yuu
# or npm install vuepress-theme-yuu
```

## Features/configuration

![Yuu user settings dropdown menu](https://i.imgur.com/bqKYL5y.png)

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

Yuu currently supports 3 color themes: the default (green) theme, a blue theme, and a red theme. By default, any additional themes will be included. If you only want to use certain themes, you'll need to be explicit about which ones.

```js
module.exports = {
	themeConfig: {
		yuu: {
			colorThemes: ['red'],
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

### Extra options

If you want to add your own options to or around the dropdown menu, you can do so via the `extraOptions` setting. The strings provided are the names of the components to use (most likely located in your `/docs/.vuepress/components/` directory).

```js
module.exports = {
	themeConfig: {
		yuu: {
			extraOptions: {
				before: 'BeforeContent',
				after: 'AfterContent',
				above: 'AboveContent',
				below: 'BelowContent',
			},
		},
	},
};
```

`before` and `after` will be placed before or after the cog icon, and `above` and `below` will be placed inside the dropdown menu, above or below the default Yuu options. You can target these elements in your CSS with the selectors `.user-options-before`, `.user-options-after`, `.user-options-above`, and `.user-options-below`.
