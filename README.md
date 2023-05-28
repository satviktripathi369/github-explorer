# 🔗 [satvik-github-explorer-username.vercel.app](https://github-explorer-k436-2zj37fk89-satviktripathi369.vercel.app/)



My personal portfolio website, built with [Next.js](https://nextjs.org/), [Tailwind CSS](https://tailwindcss.com/), and deployed to preview(https://vercel.com/). Some ideas borrowed from Jirihofmann (https://github.com/jirihofman).

Data about user and projects are gathered via GitHub API.

## Tech stack
- **Framework**: [Next.js](https://nextjs.org/)
- **Deployment**: [Vercel](https://vercel.com)
- **Styling**: [Tailwind CSS](https://tailwindcss.com)
## Running Locally


```sh
git clone https://github.com/satviktripathi369/github-explorer.git
cd portfolio
```


Create a `.env` file similar to [`.env.example`].
```sh
mv .env.example .env.local
```
Add GitHub token into the new file.
```sh
GH_TOKEN=YOUR_GH_TOKEN
# If you have Vercel projects, create a token here https://vercel.com/account/tokens to get more info.
VC_TOKEN=YOUR_VERCEL_TOKEN
```

Then install dependencies and run the development server:
```sh
# Install dependencies.
npm install
# Replace jirihofman's personal info with octocat's.
npm run setup
# Start hacking.
npm dev
```

Edit `data.json` to put your personal information there.


## Cloning / Forking

Please remove all of my personal information in `data.json` before deploying your own version of this site by running `npm run setup`. Once you are happy with your `data.json`, set
```sh
# .env or .env.local

IS_TEMPLATE=false
```
in your ENVs to prevent `npm build` from reverting `data.json` back to Octocat's data.

### To check before deploying
- [ ] `data.json`: githubUsername, description, heroNames. Handled by `setup.mjs`.
- [ ] `README.md`: link at the top
- [ ] `app/layout.jsx`: metadata - title, description, favicon. Handled by `setup.mjs`.
- [ ] `public/favicon.ico`. Handled by `setup.mjs`.
