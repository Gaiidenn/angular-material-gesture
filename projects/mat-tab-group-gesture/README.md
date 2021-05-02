# Angular Material TabGroup Gesture

This library provide a simple directive to enable gesture behaviors for the MatTabGroup component on top of @angular/material library.

#####Gesture features :

* Scroll tab header with your finger IF there are too much tabs to show it all on your screen
* Swipe between tabs by swiping the tab content from left to right (or right to left)


## Getting started
Install the library from `npm`

`npm i --save @angular-material-gesture/mat-tab-group-gesture`

Next, import the MatTabGroupGestureModule in your app's module

<b>app.module.ts</b>

```ts
import { MatTabGroupGestureModule } from 'mat-tab-group-gesture';
...
@NgModule({
  ...
  imports: [
    ...
    MatTabGroupGestureModule,
  ],
  ...
})
export class AppModule { }
```

After that, you will be able to add gesture directive to mat-tab-group :

```html
<mat-tab-group matTabGroupGesture [swipeLimitWidth]="80" [connectEdges]="true">
    ...
</mat-tab-group>
```

## API Documentation

#### MatTabGroupGesture
Directive responsible for managing gesture behaviors

Selector: `matTabGroupGesture`

#### Properties

| Name   | Default value    | Description
| -----  | -------    | -----------
| swipeLimitWidth   | 80    | The minimum length of the "swipe" gesture to trigger the tabs navigation
| connectEdges   | true    | If true, the first tab and the last tab are connected (swiping for next tab on last tab will swipe to the first tab & vice-versa)

