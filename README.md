# Storyforge Frontend

React Native app for Storyforge — an AI-powered short video creation tool.

## Tech Stack

- **Framework**: Expo + React Native
- **Navigation**: React Navigation (Stack)
- **State Management**: Zustand
- **Language**: TypeScript

## Quick Start

```bash
# Install dependencies
npm install

# Start Expo dev server
npx expo start

# Run on Android
npx expo start --android

# Run on iOS
npx expo start --ios
```

## Screens

| Screen | Path | Description |
|--------|------|-------------|
| ProjectList | `/` | List all projects, create new |
| CreateProject | `/create` | Enter idea, select template |
| ProjectDetail | `/project/:id` | Card-based workflow view |
| Settings | `/settings` | Model vendor configuration |

## Project Structure

```
storyforge-frontend/
├── App.tsx                       # Root app with navigation
├── src/
│   ├── api/                      # API client & endpoints
│   ├── components/               # Reusable UI components
│   ├── screens/                  # Page screens
│   ├── store/                    # Zustand state stores
│   ├── types/                    # TypeScript types
│   └── config.ts                 # API base URL
├── app.json
└── package.json
```

## Components

| Component | Description |
|-----------|-------------|
| Card | Generic card with confirm/redo actions |
| ProgressBar | Progress indicator for generation stages |
| TemplateCard | Horizontal scrollable template card |

## Configuration

Set the backend API URL in `src/config.ts`:

```ts
export const API_BASE_URL = __DEV__
  ? 'http://localhost:3000'
  : 'https://your-production-url.com';
```

## Related

- [Backend](https://github.com/xtangxtang/storyforge) — Express API server

## License

ISC
