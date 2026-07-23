- Always check types using `pnpm run type-check`.
- Always use shadcn skill for UI components and interacting with shadcn.
- Never make try catches without logging the error, and never ignore errors silently. Always log the error with context.
- When using [Convex](https://www.convex.dev/) for authentication always use [Convex Auth](https://labs.convex.dev/auth)
- When you want email sending:
  - Plain Next.js on cloudflare workers: Use `send_email` binding (https://developers.cloudflare.com/email-service/configuration/send-bindings/)
  - With Convex: Send emails through Cloudflare Email Service through API using their library [cloudflare](https://www.npmjs.com/package/cloudflare) ([docs](https://github.com/cloudflare/cloudflare-typescript/blob/main/src/resources/email-sending/api.md)).

<!-- BEGIN:nextjs-agent-rules -->
# This is NOT the Next.js you know

This version has breaking changes — APIs, conventions, and file structure may all differ from your training data. Read the relevant guide in `node_modules/next/dist/docs/` before writing any code. Heed deprecation notices.
<!-- END:nextjs-agent-rules -->
