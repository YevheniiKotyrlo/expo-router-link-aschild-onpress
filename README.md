# expo-router-link-aschild-onpress

On web, `<Link asChild>` around a DOM element passes it React Native's `onPress`, and React warns that `onPress` is an unknown event handler property. This repository is `npx create-expo-app@latest` (the default template: Expo 58.0.21, `expo-router` 58.0.28), with `npx expo install --fix` run once and one change in `src/app/index.tsx`: on web it renders

```tsx
<Link asChild href="/explore">
  <a>Explore</a>
</Link>
```

## Steps

Web, the development server, npm.

1. Clone and install:
   ```sh
   git clone https://github.com/YevheniiKotyrlo/expo-router-link-aschild-onpress
   cd expo-router-link-aschild-onpress
   npm install
   ```
2. Start the dev server and wait for `Waiting on http://localhost:8081`:
   ```sh
   npx expo start
   ```
3. Open http://localhost:8081 in a browser and read the console.

Expected: no warning; the anchor navigates to `/explore`, which it does.

What I see in Chromium 156 (Windows 11, Node 26.12.1):

```
Unknown event handler property `onPress`. It will be ignored.
```
