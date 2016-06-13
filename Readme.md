# Getting Started

[Follow the first page of the getting started guide on React Native](https://facebook.github.io/react-native/docs/getting-started.html)

**If you are on a windows machine you can only develop an Android app.**

**If you are on a Mac I recommend downloading [Nuclide](http://nuclide.io/docs/quick-start/getting-started/), an IDE created by Facebook for React Native**


## Initializing the project

```
react-native init NativeReddit
```

## Installing the dependencies

Enter the folder you just created above, `NativeReddit`:

```
cd NativeReddit
```

Then install the following 4 modules (`--save` saves references to each module in your `package.json` file).

```
npm install redux react-redux redux-thunk isomorphic-fetch --save
```

# Reddit Native

[Background]

# Creating the Native Reddit App

Open the `NativeReddit` folder in the IDE/text editor of your choice (e.g. Nuclide/Atom/Sublime).

`NativeReddit/index.ios.js` is the entry point to your app if you build an iOS app while `NativeReddit/index.android.js` is the entry point to your app if you build an Android app. I'll refer to the index file as `index.*.js` and if you are building an Android app you'll refer to the `index.android.js` file while if you are building an iOS app you will refer to `index.ios.js`.

## Creating our first native component

First we'll create a top navigation bar that will initially hold the current view's title.

In `NativeReddit` create a folder called `components` then create the file `components/reddit-nav-bar.js` (React Native does not recognize `.jsx` extensions, so we'll stick to `.js`).

First we'll import all the modules needed to build our own module:

```javascript
import React, { Component } from 'react';
import {
  StyleSheet,
  Text,
  View
} from 'react-native';
```

To create the component we'll use an `ES6` class and extend React Native's `Component` class. The class will include two methods `constructor()` and `render()`:

```javascript
class RedditNavigationBar extends Component {
  constructor(props){
    super(props);
    this.title = props.title;
  }

  render(){
    return (
      <View>
        <View style={styles.toolbar}>
          <Text style={styles.title}>{this.title}</Text>
        </View>
      </View>
    )
  }
}
```

In the constructor we pass the `props` to the parent's class using `super(props)`.

The `render()` function is what returns the UI for this component. Note that we are no longer using `<div>`'s, `<View>`'s and `<Text>` are actual native UI elements that React Native will create for us.

## Creating our list of Reddit top stories

In `components/` create the file `components/reddit-list.js`  There are several new concepts that we'll need in order to build our list of Reddit stories. We'll improve the component incrementally.



```js

```