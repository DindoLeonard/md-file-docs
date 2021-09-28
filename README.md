# WEED WORLD V2

We use expo when initially developing this as there's still no need for native sdk's other than expo sdk.

### Attention!:

- Initial advice to use yarn in developing when installing dependecies.
- During development if you'll have a yellow box warning about `Setting a timer for a long period of time`, reference this [solution in stackoverflow](https://stackoverflow.com/questions/44603362/setting-a-timer-for-a-long-period-of-time-i-e-multiple-minutes)
- If you have problem with Reanimated2 library, try type in terminal try `expo -r c`. reference for the [solution is stackoverflow](https://stackoverflow.com/questions/67130651/reanimated-2-failed-to-create-a-worklet-maybe-you-forgot-to-add-reanimateds-ba)

### Why Yarn?

npm seems to have a problem with redux-toolkit.
would also make the codebase more consistent if we all use yarn.

**=>** We always aspire and push for good coding practices and structure, to achieve good maintainability and ease for development.

## Installation and Start

1. Clone the repo
   ```sh
   git clone https://github.com/Quantum-L/WeedWorldApp_V2.git
   ```
2. Install packages, to install all dependencies, open terminal in root and type.
   ```sh
   yarn
   ```
3. To start development with expo type. (it will open a server in chrome)
   ```sh
   yarn start
   ```
   or
   ```sh
   expo start
   ```

## Project guide for onboarding

- In this project, we are following the Atomic Design for structure and and for maintainability, see reference about it: see [article](https://bradfrost.com/blog/post/atomic-web-design/) or this [3min-video](https://www.youtube.com/watch?v=Yi-A20x2dcA)
- For most UI-components and some layouts, this project is mainly using [UI-Kitten](https://akveo.github.io/react-native-ui-kitten/docs/getting-started/what-is-ui-kitten#what-is-ui-kitten).
- under `screens` folder, you'll see `Routes` folder, which will conditionally render either the AuthScreen or MainScreen. You can then follow the flow of the navigation from there initially.
- The root `screens` folder has all the screens in our app, There's a folder for every screen inside it and has `index.tsx` which is primary component, `index.tsx` in the any specific screen folder mainly consists of any sub-components within containing screen folder if there's any.
- The `App.tsx` file in the root is where we put all the wrappers and initial set-up for the app.
- We are using [redux-toolkit](https://redux-toolkit.js.org/introduction/getting-started) for our global state management. It is in the root folder named `redux`. Inside it you can find slices in the `slices` folder, redux store is consists of slices. Each slice has it's own initial state and reducers or actions to mutate the its current state.
- Every firebase authentication/firestore queries are in the `firebase` folder at the root and named as such inside it. You'll see the descriptive name of every function you're looking for in each file under services which is exported for the app.
- We use React Navigation for our mobiel app navigation. Reference to docs [React Navigation](https://reactnavigation.org/docs/getting-started/)
- Added a testComponents folder if ever any dev wanted to experiment and test any reference.

## Contributing

### 1. Create/Pick a task from our github under projects or issues.

### 2. Create a branch off of `main`

preferable to be in this format. `label/issue-name-on-github`

```sh
git checkout -b enhancement/issuename
```

to check your current branch

```sh
git branch
```

### 3. Do your stuff

Make commits according to its purpose.For example, if you are building a new feature, don't do code cleanup. Do code cleanup in a separate commit (or better separate branch)
Commit message template: `[Commit Type][Author] Add user login`
**Commit types:**

- Feature
- Fix
- Fix Test
- Misc
- Test
- Adjustment

### 4. Link pull request if you commit: [reference](https://docs.github.com/en/issues/tracking-your-work-with-issues/linking-a-pull-request-to-an-issue)

### 5. Push to Github often. Rebase often. Always git pull if you at the start of the day also

Pushing and pulling often reduces the chance of conflicts and being out of sync. Try to do this a few times a day.

### 6. When ready, create a Pull Request from your branch to `main` branch.

Tag the reviewers to review your PR. Mention the reviewers in Discord along with a link to your PR.

### 7. After it a successful review and merge or rebase, you can now delete the branch and go back to the `main` branch and a pull request there again to update the main branch.

1. `git checkout main`
2. `git pull`

## Tech Stack

- **Front:** [React Native](https://reactnative.dev/docs/getting-started) with [Expo](https://docs.expo.dev/)
- **UI-Lib:**
  - [React Native Elements](https://reactnativeelements.com/)
  - [React Native Paper](https://callstack.github.io/react-native-paper/)
- **Language:** [TypeScript](https://www.typescriptlang.org/docs/) and [JavaScript](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
- **Global State-Mangement:** [React Redux with Redux Tollkit](https://redux-toolkit.js.org/tutorials/quick-start)
- **DB:** [Firebase Firestore](https://firebase.google.com/docs/firestore)
- **Auth:** [Firebase Authentication](https://firebase.google.com/docs/auth)
- **Routing:** [React Navigation](https://reactnavigation.org/docs/getting-started)
- **Hosting:** Soon
