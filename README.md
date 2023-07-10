# Frontend Folder Structure

Folder structure for Frontend projects.

## Structure

[Tool](https://tree.nathanfriend.io/)

```
└── src/
    ├── application/
    │   ├── services
    │   ├── store
    │   ├── style
    │   └── assets
    ├── modules/
    │   ├── @common
    │   └── ModuleExample/
    │       ├── __mocks__
    │       ├── __tests__
    │       ├── @common
    │       └── pages/
    │           └── PageExample/
    │               ├── __mocks__
    │               ├── __tests__
    │               ├── components
    │               ├── context
    │               ├── hooks
    │               ├── store
    │               ├── utils
    │               ├── PageExample.tsx
    │               └── index.ts
    └── pages
```

- Files on folders named **{name}** will not be compiled.

## @Common Folder Example

- Put the elements only used inside that module or page.
- On the components folder, if there are a lot of components, we can use [Atomic Design](https://github.com/danilowoz/react-atomic-design) to organice them.

```
└── @common/
    ├── components/
    │   ├── atoms
    │   ├── molecules
    │   ├── organisms
    │   └── templates
    ├── context
    ├── hooks
    ├── store
    └── utils
```

## Component Structure Example

- Always nest components and files inside the folder where they are used.
- Write component names as PascalCase.
- Write folder names as kebab-case.

```
├── card
│   ├── components
│   │   ├── header
│   │   │   ├── components
│   │   │   │   └── user-box
│   │   │   │       ├── UserBox.tsx
│   │   │   │       ├── UserBox.scss
│   │   │   │       └── index.ts
│   │   │   ├── Header.tsx
│   │   │   ├── Header.scss
│   │   │   └── index.ts
│   │   └── footer
│   │       ├── Footer.tsx
│   │       ├── Footer.scss
│   │       └── index.ts
│   ├── utils
│   └── hooks
├── Card.tsx
├── Card.scss
├── Card.stories.tsx
└── index.ts
```

### Component example

```javascript
import React from "react";

// --> types

const Card = () => {
  // --> States

  // --> Effects
  return <div></div>;
};

export default Card;
```

### Commits and branches

- Use conventional commits https://www.conventionalcommits.org

```bash
type(<scope>): description
```

Branches:

```bash
origin/{owner}/{jira-ticket}/{description}

origin/joe/PROJECTX-10/login-page-header
```
