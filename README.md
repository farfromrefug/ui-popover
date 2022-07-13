<!-- ⚠️ This README has been generated from the file(s) "blueprint.md" ⚠️--><!-- ⚠️ This README has been generated from the file(s) "blueprint.md" ⚠️-->
<!--  !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
      !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
      !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
      !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
      !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
      !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
      !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
      !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
      !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
      DO NOT EDIT THIS READEME DIRECTLY! Edit "bluesprint.md" instead.
      !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
      !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
      !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
      !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
      !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
      !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
      !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
      !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
      !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!! -->
<h1 align="center">@nativescript-community/ui-popover</h1>
<p align="center">
		<a href="https://npmcharts.com/compare/@nativescript-community/ui-popover?minimal=true"><img alt="Downloads per month" src="https://img.shields.io/npm/dm/@nativescript-community/ui-popover.svg" height="20"/></a>
<a href="https://www.npmjs.com/package/@nativescript-community/ui-popover"><img alt="NPM Version" src="https://img.shields.io/npm/v/@nativescript-community/ui-popover.svg" height="20"/></a>
	</p>

<p align="center">
  <b>Popover plugn</b></br>
  <sub><sub>
</p>

<br />


| <img src="https://raw.githubusercontent.com/nativescript-community/ui-popover/master/images/demo-ios.gif" height="500" /> | <img src="https://raw.githubusercontent.com/nativescript-community/ui-popover/master/images/demo-android.gif" height="500" /> |
| --- | ----------- |
| iOS Demo | Android Demo |


[](#table-of-contents)


[](#table-of-contents)

## Table of Contents

* [Installation](#installation)
* [Configuration](#configuration)
* [API](#api)
	* [Properties](#properties)
	* [Methods](#methods)
	* [Events](#events)
* [Usage in Angular](#usage-in-angular)
	* [Examples:](#examples)
* [Usage in React](#usage-in-react)
	* [Examples:](#examples-1)
* [Usage in Svelte](#usage-in-svelte)
	* [Examples:](#examples-2)
* [Usage in Vue](#usage-in-vue)
	* [Examples:](#examples-3)
* [Demos and Development](#demos-and-development)
	* [Setup](#setup)
	* [Build](#build)
	* [Demos](#demos)
* [Questions](#questions)


[](#installation)


[](#installation)

## Installation
Run the following command from the root of your project:

`ns plugin add @nativescript-community/ui-popover`


[](#configuration)


[](#configuration)

## Configuration
For gestures to work, make sure to add the following code block inside the main application file (e.g. app.ts):

```typescript
import { install } from '@nativescript-community/ui-popover';
install();
```


[](#api)


[](#api)

## API

### Properties

| Property            | Default                           | Type                        | Description                                             |
| ------------------- | --------------------------------- | --------------------------- | ------------------------------------------------------- |
| leftDrawer          | `undefined`                       | `View`                      | View containing the content for the left side drawer    |
| rightDrawer         | `undefined`                       | `View`                      | View containing the content for the right side drawer   |
| topDrawer          | `undefined`                       | `View`                      | View containing the content for the top side drawer    |
| bottomDrawer         | `undefined`                       | `View`                      | View containing the content for the bottom side drawer   |
| mainContent         | `undefined`                       | `View`                      | View containing the main content of the app             |
| gestureEnabled      | `true`                            | `boolean`                   | Boolean setting if swipe gestures are enabled           |
| backdropColor       | `new Color('rgba(0, 0, 0, 0.7)')` | `Color`                     | The color of the backdrop behind the drawer             |
| leftDrawerMode      | `slide`                           | `Mode ('under' or 'slide')` | The color of the backdrop behind the drawer             |
| rightDrawerMode     | `slide`                           | `Mode ('under' or 'slide')` | The color of the backdrop behind the drawer             |
| gestureMinDist     | `10`                           | number | The min "swipe" distance to trigger the menu gesture             |
| gestureHandlerOptions     | `null`                           | PanGestureHandlerOptions | Options to customize the pan gesture handler             |
| leftSwipeDistance     | `40`                           | number | The "left" zone size from where the gesture is recognized             |
| rightSwipeDistance     | `40`                           | number | The "right" zone size from where the gesture is recognized             |
| topSwipeDistance     | `40`                           | number | The "top" zone size from where the gesture is recognized             |
| bottomSwipeDistance     | `40`                           | number | The "bottom" zone size from where the gesture is recognized             |
| leftOpenedDrawerAllowDraging     | `true`                           | boolean | Allow dragging the opened menu             |
| rightOpenedDrawerAllowDraging     | `true`                           | boolean | Allow dragging the opened menu             |
| topOpenedDrawerAllowDraging     | `true`                           | boolean | Allow dragging the opened menu             |
| bottomOpenedDrawerAllowDraging     | `true`                           | boolean | Allow dragging the opened menu             |



### Methods

| Name         | Return | Description                                     |
| ------------ | ------ | ----------------------------------------------- |
| open()       | `void` | Programatically open the drawer                 |
| close()      | `void` | Programatically close the drawer                |
| toggle()     | `void` | Programatically toggle the state of the drawer  |
| install()    | `void` | Install gestures                                |

### Events

| Name      | Event Data         | Description                  |
| --------- | ------------------ | ---------------------------- |
| open      | `side`, `duration` | Drawer opens                 |
| close     | `side`, `duration` | Drawer closes                |


[](#usage-in-angular)


[](#usage-in-angular)

## Usage in Angular
Import the module into your project.

```typescript
import { DrawerModule } from "@nativescript-community/ui-popover/angular";

@NgModule({
    imports: [
        DrawerModule
    ]
    schemas: [
        NO_ERRORS_SCHEMA
    ]
})

export class AppModule { }
```

### Examples:

- [Basic Drawer](demo-snippets/ng/basic-drawer)
  - A basic sliding drawer.
- [All Sides](demo-snippets/ng/all-sides)
  - An example of drawers on all sides: left, right, top, bottom.



[](#usage-in-react)


[](#usage-in-react)

## Usage in React

Register the plugin in your `app.ts`.

```typescript
import DrawerElement from '@nativescript-community/ui-popover/react';
DrawerElement.register();
```

### Examples:

- [Basic Drawer](demo-snippets/react/BasicDrawer.tsx)
  - A basic sliding drawer.
- [All Sides](demo-snippets/react/AllSides.tsx)
  - An example of drawers on all sides: left, right, top, bottom.


[](#usage-in-svelte)


[](#usage-in-svelte)

## Usage in Svelte

Register the plugin in your `app.ts`.

```typescript
import DrawerElement from '@nativescript-community/ui-popover/svelte';
DrawerElement.register();
```

### Examples:

- [Basic Drawer](demo-snippets/svelte/BasicDrawer.svelte)
  - A basic sliding drawer.
- [All Sides](demo-snippets/svelte/AllSides.svelte)
  - An example of drawers on all sides: left, right, top, bottom.


[](#usage-in-vue)


[](#usage-in-vue)

## Usage in Vue

Register the plugin in your `app.js`.

```typescript
import DrawerPlugin from '@nativescript-community/ui-popover/vue'
Vue.use(DrawerPlugin);
```

### Examples:

- [Basic Drawer](demo-snippets/vue/BasicDrawer.vue)
  - A basic sliding drawer.
- [All Sides](demo-snippets/vue/AllSides.vue)
  - An example of drawers on all sides: left, right, top, bottom.


[](#demos-and-development)


[](#demos-and-development)

## Demos and Development


### Setup

To run the demos, you must clone this repo **recursively**.

```
git clone https://github.com/@nativescript-community/ui-popover.git --recursive
```

**Install Dependencies:**
```bash
npm i # or 'yarn install' or 'pnpm install'
```

**Interactive Menu:**

To start the interactive menu, run `npm start` (or `yarn start` or `pnpm start`). This will list all of the commonly used scripts.

### Build

```bash
npm run build

npm run build.angular # or for Angular
```

### Demos

```bash
npm run demo.[ng|react|svelte|vue].[ios|android]

npm run demo.svelte.ios # Example
```

[](#questions)


[](#questions)

## Questions

If you have any questions/issues/comments please feel free to create an issue or start a conversation in the [NativeScript Community Discord](https://nativescript.org/discord).