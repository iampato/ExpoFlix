# ExpoFlix App

 A movie listing application built using RN ❤️ Expo


## Presquites:

- Typescript
- Expo

## How to run the project

**Step 1:**

Download or clone this repo by using the link below:

```
git clone https://github.com/iampato/ExpoFlix.git
```

**Step 2:**

Ensure you have expo installed if not no worries


**Step 3:**

Cd into the project directory and install packages using `npm` or `yarn`

```
yarn install
```
or

```
npm i
```


**Step 5:**

Run the project, depending run expo :

```
yarn start
```

or 

```
npm run start
```

If it gives you the option to either run android or ios press `a` for android and `i` for ios 


### Libraries & Tools Used

1. ### State management
    * Zustand
    
2. ### Networking
    * Axios

3. ### UI
    * Fonts -  Expo Google fonts and Expo Fonts
    * Icons - [react-native-vector-icons](https://github.com/oblador/react-native-vector-icons)
    * Animations - Reanimated
    * Blur - Expo Blur
   
4. ### Navigation
    * Expo Router
     
5. ### Testing
    * [Jest](https://jestjs.io/) - a JavaScript testing framework

6. ### Others
   * [react-native-svg](https://github.com/react-native-svg/react-native-svg) - a library for SVG support in React Native
   * 
   * [react-native-safe-area-context](https://github.com/th3rdwave/react-native-safe-area-context) - a library for handling safe area insets in React Native
   * [lottie-react-native](https://github.com/lottie-react-native/lottie-react-native) - a library for rendering Lottie animations in React Native

### Folder Structure
This application uses a multi-module architecture though the packages are not in seperate packages this can easily be done. for purposes of simplicity I under them under `src` 


Here is the folder structure we have been using in this project inside of `src`

```
.
├── app
...
├── components
...
├── core
...
└── features
...
```


1. The **app*** module holds app-related things for example the app entry component, main routes, etc
Ideally, high-level components that are needed by an app

```
├── app
│   ├── App.tsx
│   └── rootNavigation.tsx
```

2. The **core*** module contains common things that an app needs, and various features can depend on this module for example things found on the core module include:
   - assets - a central place for managing assets instead of directly using them in the app, which makes it easy to change assets
   - config - Set up your config; things like `APIURL`, sentry URL, etc
   - constants - constants used in your application
   - theme - the app uses a custom theme to provide theming
   - styles - includes extensions on various colors, text styles, durations, Corners
   - And many more

For this app here were my core modules; constants to hold my immutable variables, sizes for dynamic and responsive designs, textTopography for my custom text topography, and lastly theme that exposed a hook for getting theme colors based on the theme of the device 
```
├── core
│   ├── constants.ts
│   ├── sizes.ts
│   ├── textTopography.ts
│   └── theme.ts
```

3. The **Feature*** module houses all the features and in this app they include

Ideally, a feature has the following;
- screens - screens in that feature
- store - have your state management solution here
- components - reusable components in that feature

```
└── features
    ├── Landing
    │   ├── components
    │   └── screens
    │       ├── landing.screen.tsx
    ├── Home
    │   ├── components
    │   └── screens
    │       └── home.screen.tsx
    ├── Search
    │   ├── components
    │   └── screens
    │       └── search.screen.tsx
    ├── Categories
    │   ├── components
    │   └── screens
    │       └── categories.screen.tsx
    ├── Detail
    │   ├── components
    │   └── screens
    │       └── detail.screen.tsx
    ├── profile
    │   ├── components
    │   └── screens
    │       ├── profile.screen.tsx
    │       └── settings.screen.tsx
```

## Resources

### Design

The app has been inspired by this UI kit (Muvi)[https://ui8.net/kitani/products/muvi---movie-streaming-ui-kit]



