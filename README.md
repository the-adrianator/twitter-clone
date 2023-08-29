# Create T3 App

This is a [T3 Stack](https://create.t3.gg/) project bootstrapped with `create-t3-app`.

## What's next? How do I make an app with this?

We try to keep this project as simple as possible, so you can start with just the scaffolding we set up for you, and add additional things later when they become necessary.

If you are not familiar with the different technologies used in this project, please refer to the respective docs. If you still are in the wind, please join our [Discord](https://t3.gg/discord) and ask for help.

- [Next.js](https://nextjs.org)
- [NextAuth.js](https://next-auth.js.org)
- [Prisma](https://prisma.io)
- [Tailwind CSS](https://tailwindcss.com)
- [tRPC](https://trpc.io)

## Learn More

To learn more about the [T3 Stack](https://create.t3.gg/), take a look at the following resources:

- [Documentation](https://create.t3.gg/)
- [Learn the T3 Stack](https://create.t3.gg/en/faq#what-learning-resources-are-currently-available) — Check out these awesome tutorials

You can check out the [create-t3-app GitHub repository](https://github.com/t3-oss/create-t3-app) — your feedback and contributions are welcome!

## How do I deploy this?

Follow our deployment guides for [Vercel](https://create.t3.gg/en/deployment/vercel), [Netlify](https://create.t3.gg/en/deployment/netlify) and [Docker](https://create.t3.gg/en/deployment/docker) for more information.



## Creating a twitter-clone app
T3 setup 
run npm create t3-app@latest
use typescript - y
other packages - nextAuth, prisma, tailwind, trpc
npm install - y
import alias - default

Prisma db setup
create new db on planetscale.com
make main branch production branch
create new dev branch off of main
connect dev branch with prisma
copy db url and replace in .env variables
copy schema.prisma section and replace generator client and datasource db
uncomment @db.Text annotation in schema.prisma
create index - @@index([userId]) in model Account and model Session
run npx prisma db push - to push database changes to planetscale

Authentication setup
go to discord.com/developers/applications
create and name new application
copy and paste client id to .env variables
reset secret and copy to .env variables
add redirect (t3 app docs) - http://localhost:3000/api/auth/callback/discord
-----------------------------------------------
NextAuth secret - run openssl rand -base64 32

Deployment setup
create and push to git repo
go to vercel and connect with github project
add in environment variables