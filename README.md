# CleanCode Next.js TS Snippets

**Customizable Next.js snippet extension** for VS Code, focused on clean code patterns.

## Features

- `nx_client` → Next.js Client Function Component
- `nx_server` → Next.js Server Function Component
- `nx_fetch`  → Function for Fetch data and parses as JSON ,includes basic error handling.
- `nx_useState`  → React useState hook with TypeScript (defaults to any type).
- Structured comment blocks (Imports, Types, Event Handlers, Constants, Hooks, TSX)
- Built-in `className` prop + `cn` utility pattern
- Accessibility reminder stub

## Usage

1. Clone or download this repo.
2. In VS Code: **Developer: Load Extension From Folder** → select this folder.
3. Open a `.tsx`/`.ts`  file and type `nx_client` or `nx_server`  or any snippet+ `Tab`.

## Examples

### Client Component
Type `nx_client` + Tab and you’ll get:

```tsx
'use client';

// ─────────────────── Imports ───────────────────
import { cn } from "@/lib/utils";

// ─────────────────── Types ─────────────────────
interface ComponentProps {
  className?: string;
}

// ──────────────── Event Handlers ───────────────

// ─────────────────── Constants ──────────────────

// ────────────────────────────────────────────────
export function Component({ className }: ComponentProps) {
  // ─────────────────── Hooks ─────────────────────

  // ─────────────────── TSX ─────────────────────
  return (
    <div className={cn('', className)}>
      {/* TODO: Add aria-* attributes for accessibility */}
      {/* … */}
    </div>
  );
}
```

### Server Component
Type `nx_server` + Tab and you’ll get:

```tsx
// ─────────────────── Imports ───────────────────
import { cn } from "@/lib/utils";

// ─────────────────── Types ─────────────────────
interface ComponentProps {
  className?: string;
}

// ──────────────── Event Handlers ───────────────

// ─────────────────── Constants ──────────────────

// ────────────────────────────────────────────────
export function Component({ className }: ComponentProps) {
  // ─────────────────── Hooks ─────────────────────

  // ─────────────────── TSX ─────────────────────
  return (
    <div className={cn('', className)}>
      {/* TODO: Add aria-* attributes for accessibility */}
      {/* … */}
    </div>
  );
}
```
### Fetching Function 
Type `nx_fetch` + Tab and you’ll get:

```tsx 
//---Fetch Data---
async function fetchData<T>(url: string): Promise<T> {
  try {
    const response = await fetch(url);
    if (!response.ok) {
      throw new Error(`HTTP error! status: ${response.status}`);
    }
    const data: T = await response.json();
    return data;
  } catch (error) {
    console.error("Error fetching data:", error);
    throw error; // Re-throw the error or handle it as needed
  }
}

```
### useState React Hook
Type `nx_useState` + Tab and you’ll get:

```tsx 
// NOTE: Remember to add 'import { useState } from 'react';' at the top of your file
const [dataState, setDataState] = useState<any>(/*initialValue*/);

```

---

## Contact
Created by **Ramzi Hadrouk**.  
Follow me on
 [GitHub](https://github.com/yourusername) for more projects and updates.

---
---
---
## Contributing

Feel free to tweak the snippet file in `snippets/nextjs-snippets.json`.
```
├── package.json
├── snippets/
│    └── nextjs-snippets.json
│── images/
│     └── icon.png
└── README.md
```
**To install locally:** in VS Code press <kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>P</kbd>, choose **Developer: Load Extension From Folder**, and pick this project root.

Enjoy your clean-code boilerplate workflow! 🚀
