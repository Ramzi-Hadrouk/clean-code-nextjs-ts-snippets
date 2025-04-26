# CleanCode Next.js TS Snippets

**Customizable Next.js snippet extension** for VS Code, focused on clean code patterns.

## Features

- `nfcc` → Next.js Client Function Component
- `nfcs` → Next.js Server Function Component
- Structured comment blocks (Imports, Types, Event Handlers, Constants, Hooks, TSX)
- Built-in `className` prop + `cn` utility pattern
- Accessibility reminder stub

## Usage

1. Clone or download this repo.
2. In VS Code: **Developer: Load Extension From Folder** → select this folder.
3. Open a `.tsx` or `.jsx` file and type `nfcc` or `nfcs` + `Tab`.

## Examples

### Client Component
Type `nfcc` + Tab and you’ll get:

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
Type `nfcs` + Tab and you’ll get:

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

## Contributing

Feel free to tweak the snippet file in `snippets/nextjs-snippets.json`.

**To install locally:** in VS Code press <kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>P</kbd>, choose **Developer: Load Extension From Folder**, and pick this project root.

Enjoy your clean-code boilerplate workflow! 🚀
