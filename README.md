### 🗯️ Profanity API

A scalalbe REST API to check profanity in chunks (at scale)

### Test Production API

```js
const res = await fetch("https://profanity-api.profanity-prod.workers.dev/", {
  method: "POST",
  headers: { "Content-Type": "application/json" },
  body: JSON.stringify({ message }),
});
```

### Tech Stack

- Backend - [Hono](https://hono.dev/)
- Database - [@upstash/vector](https://upstash.com/)
- Deployment - [Cloudflare Workers](https://workers.cloudflare.com/)

### Local Set-Up

```bash
$ git clone <...>
$ cd profanity-api
# or any other package manager - remove the current lock file
$ pnpm install
$ pnpm wrangler dev index
```

Make sure to add the required env

```bash
# @upstash vector db credentials

VECTOR_URL=...
VECTOR_TOKEN=...
```

You will require a [`Cloudflare`](cloudflare.com) account to deploy it under their workers/pages

### TO-DO

- [ ] simple test-frontend to hit the endpoint
