# Next.js Template

A standard template used by everyone at Fanth for building web apps. Built with Next.js, Tailwind CSS, shadcn/ui, Lucide icons, Framer Motion, and multiple deployment options.

## Tech Stack

- **Framework:** [Next.js 15](https://nextjs.org/) with Turbopack
- **React:** v19
- **Styling:** [Tailwind CSS 4](https://tailwindcss.com/)
- **Components:** [shadcn/ui](https://ui.shadcn.com/) (New York style)
- **Icons:** [Lucide React](https://lucide.dev/)
- **Animations:** [Framer Motion](https://motion.dev/)
- **Package Manager:** pnpm
- **Language:** TypeScript

## Features

- Server Components (RSC) ready
- Cloudflare Pages deployment via [OpenNext](https://opennext.js.org/)
- Docker support with GitHub Container Registry
- GitHub Actions CI/CD
- Prettier with Tailwind CSS plugin
- [Renovate](https://docs.renovatebot.com/) for automated dependency updates

## Getting Started

```bash
# Install dependencies
pnpm install

# Run development server with Turbopack
pnpm dev
```

Open [http://localhost:3000](http://localhost:3000) to see the result.

## Scripts

| Command | Description |
|---------|-------------|
| `pnpm dev` | Start dev server with Turbopack |
| `pnpm build` | Build for production |
| `pnpm start` | Start production server |
| `pnpm lint` | Run ESLint |
| `pnpm preview` | Build and preview Cloudflare deployment |
| `pnpm deploy` | Deploy to Cloudflare Pages |

## Adding shadcn/ui Components

```bash
pnpm dlx shadcn@latest add button
```

## Icons

This template works great with [Lucide React](https://lucide.dev/) icons (recommended for shadcn/ui) or [Phosphor Icons](https://phosphoricons.com/).

### Install Lucide React

```bash
pnpm add lucide-react
```

### Usage Example

```tsx
import { Search, Menu, X } from "lucide-react";

export function Header() {
  return (
    <header>
      <button><Menu className="h-5 w-5" /></button>
      <button><Search className="h-5 w-5" /></button>
    </header>
  );
}
```

## Animations

For animations we use [Framer Motion](https://motion.dev/).

```bash
pnpm add framer-motion
```

### Usage Example

```tsx
import { motion } from "framer-motion";

export function FadeInBox() {
  return (
    <motion.div
      initial={{ opacity: 0, y: 20 }}
      animate={{ opacity: 1, y: 0 }}
      transition={{ duration: 0.3 }}
    >
      Hello!
    </motion.div>
  );
}
```

## Deployment

### Cloudflare Pages

```bash
pnpm deploy
```

### Docker

The included Dockerfile is automatically built and pushed to GHCR via GitHub Actions on push to `master`.