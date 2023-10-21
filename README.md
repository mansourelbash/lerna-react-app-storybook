![Create Full React Workspaces Using Lerna ](https://i.imgur.com/7snWXD0.png)

> 💥 Now supports TypeScript and React-App-Rewired!  

## Features

- ⚛️ Create React App 3 (React 16.8)
- 📖 Storybook 5
- 🐈 Yarn Workspaces
- 🐉 Lerna 3
- ✨ Host Multiple CRA Apps, Component Libraries & Storybooks in one Monorepo
- 🔥 Hot Reload all Apps, Components & Storybooks
- 👨‍🔬 Test all workspaces with Eslint & Jest using one command
- :octocat: Deploy your apps to Github Pages using one command

## Contents

- [Features](#features)
- [Contents](#contents)
- [Setup](#setup)
  - [Pre-Requisites](#pre-requisites)
  - [Installation](#installation)
- [Usage](#usage)
  - [Starting The React App](#starting-the-react-app)
  - [Starting The Storybook](#starting-the-storybook)
  - [Linting &amp; Testing](#linting-amp-testing)
  - [Deploying to GitHub Pages](#deploying-to-github-pages)
  - [Creating a New CRA App](#creating-a-new-cra-app)
- [How Does It Work?](#how-does-it-work)

## Setup

### Pre-Requisites

- Yarn 1.13.0
- Node 11.14.0

### Installation

```bash
git clone https://github.com/mansourelbash/lerna-react-app-storybook
cd lerna-react-app-storybook
yarn
```

### Adding workspace dependencies

```bash
yarn workspace <workspace_name> <command>
```

This will run the chosen Yarn command in the selected workspace.

Example:

```bash
yarn workspace my-app add react-router-dom --dev
```

This will add `react-router-dom` as `dependencies` in your `packages/my-app/package.json`. To remove dependency use `remove` instead of add

## Usage

### Starting Project in Workspace

From your project root type start command for desired app

```bash
yarn workspace @project/app-single-comp start
```

All available `start` scripts

```json
"scripts": {
    "start:app-ant-design": "yarn workspace @project/app-ant-design-rewired start",
    "start:app-multi": "yarn workspace @project/app-multi-comps start",
    "start:app-single": "yarn workspace @project/app-single-comp start",
    "start:app-ts": "yarn workspace @project/app-typescript start",
    "start:storybook": "yarn workspace @project/storybook storybook",
    "start:storybook-ts": "yarn workspace @project/storybook-typescript storybook",
    ...
  }
```

### Starting The Storybook

```bash
yarn start:storybook
```

### Linting & Testing

```bash
yarn workspace <workspace-root> test
```
