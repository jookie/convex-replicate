# Use Convex with Replicate to create images from doodles

Stack:

- [Convex](https://convex.dev)
- [Replicate](https://replicate.com/)
- [Next.js](https://nextjs.org/)
- [Tailwind CSS](https://tailwindcss.com/)

Tutorials:

- [A Tour of Convex](https://docs.convex.dev/get-started)
- [Convex Templates](https://www.convex.dev/templates)
- [Using Convex with Vercel](https://docs.convex.dev/production/hosting/vercel)
- []()
- []()
- []()
- []()

## Getting Started

Install packages:
```bash
npm install
```

Continuously deploy to the Convex backend
(this will create a (free) Convex account if you don't have one):
```bash
npx convex dev
```

Get a [Replicate API key](https://replicate.com/account/api-tokens)
(free to try) and add it to your
[environment variables](https://docs.convex.dev/production/environment-variables)
in the [Convex Dashboard](https://dashboard.convex.dev)

In another terminal, run the frontend:
```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `app/page.tsx`. The page auto-updates as you edit the file.

Editing files in `convex/` will auto-update your "Dev" deployment in Convex.

## Learn More

To learn more about Convex, check out the following resources:
- [Docs](https://docs.convex.dev) has details on the platform and APIs.
- [Stack](https://stack.convex.dev) has tips and best practices.

## 1: The reactor
In this section, you'll explore the reactor through the Convex Dashboard to get familiar with:

Tables that store your data as relational Documents
Query functions that read from your tables reactively
Mutation functions that write to your tables
Screenshot of a chat app

The Convex Dashboard is your hub for viewing and managing your Convex projects. From any Convex app, you can always quickly jump into the dashboard for that particular backend with the convex command. Let's do that now for our new chat app:

'''
npx convex dashboard
'''

## Convex functions
In our chat app's messages module, we have two functions you can find in convex/messages.ts:

messages:list is a query function, which reads data from your Convex tables.
messages:send is a mutation function, which writes data into your Convex tables.
Let's dive into query functions first.

## Reading data with query functions

messages:list is a query function that retrieves up to 100 of the most recent documents in the messages table using the ctx.db object provided by Convex:

export const list = query({
  args: {},
  handler: async (ctx) => {
    // Grab the most recent messages.
    const messages = await ctx.db.query("messages").order("desc").take(100);
    // Reverse the list so that it's in a chronological order.
    return messages.reverse();
  },
});

Hosting your Convex app on Vercel allows you to automatically re-deploy both your backend and your frontend whenever you push your code.

## Deploy the frontend on Vercel

The easiest way to deploy your Next.js frontend is to use the [Vercel Platform](https://vercel.com/new?filter=next.js).

See the [Convex docs on production deployments](https://docs.convex.dev/production/hosting/)
for details on deploying a production backend.

This guide assumes you already have a working React app with Convex. If not follow the Convex React Quickstart first. Then:

### Create a Vercel account

If you haven't done so, create a Vercel account. This is free for small projects and should take less than a minute to set up.

### Link your project on Vercel

Create a Vercel project at https://vercel.com/new and link it to the source code repository for your project on GitHub or other Git platform.

Vercel import project

### Override the Build command

Override the "Build command" to be npx convex deploy --cmd 'npm run build'.

If your project lives in a subdirectory of your repository you'll also need to change Root Directory above accordingly.