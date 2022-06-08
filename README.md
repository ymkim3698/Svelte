***

## VisualStudio Code : `Start Svelte`

1. `Node js` 설치
2. VS Code -> 플러그인
> * Svelte for VS Code
3. VS Code -> 터미널
* `node --version, npm --version`
4. `npm install -g degit`
5. 번들 선택
> * Rollup : `npx degit sveltejs/template my-app`
> * Webpack : `npx degit sveltejs/template-webpack my-app`
> * [Git Rollup](https://github.com/sveltejs/template)
> * [Git Webpack](https://github.com/sveltejs/template-webpack)
* Rollup으로 진행함
6. `cd my-app`
7. `npm install`

## 서버 시작

1. VS Code -> 터미널
2. cd my-app
3. `npm run dev`
* `HOST=0.0.0.0 npm run dev`

## 서버 종료

1. VS Code -> 터미널
2. `Ctrl + C` -> y

## Git 연동

1. git 설치
2. github 레파지토리 생성 - `기본설정`
3. VS Code -> 터미널
4. cd my-app
5. `git init`
6. `git remote add origin [url]`
7. `git add .`
8. `git commit -m "[comment]"`
9. `git push origin master`
* 단계 별로 천천히 진행 추천

***

# This repo is no longer maintained. Consider using `npm init vite` and selecting the `svelte` option or — if you want a full-fledged app framework and don't mind using pre-1.0 software — use [SvelteKit](https://kit.svelte.dev), the official application framework for Svelte.

---

# svelte app

This is a project template for [Svelte](https://svelte.dev) apps. It lives at https://github.com/sveltejs/template.

To create a new project based on this template using [degit](https://github.com/Rich-Harris/degit):

```bash
npx degit sveltejs/template svelte-app
cd svelte-app
```

*Note that you will need to have [Node.js](https://nodejs.org) installed.*


## Get started

Install the dependencies...

```bash
cd svelte-app
npm install
```

...then start [Rollup](https://rollupjs.org):

```bash
npm run dev
```

Navigate to [localhost:8080](http://localhost:8080). You should see your app running. Edit a component file in `src`, save it, and reload the page to see your changes.

By default, the server will only respond to requests from localhost. To allow connections from other computers, edit the `sirv` commands in package.json to include the option `--host 0.0.0.0`.

If you're using [Visual Studio Code](https://code.visualstudio.com/) we recommend installing the official extension [Svelte for VS Code](https://marketplace.visualstudio.com/items?itemName=svelte.svelte-vscode). If you are using other editors you may need to install a plugin in order to get syntax highlighting and intellisense.

## Building and running in production mode

To create an optimised version of the app:

```bash
npm run build
```

You can run the newly built app with `npm run start`. This uses [sirv](https://github.com/lukeed/sirv), which is included in your package.json's `dependencies` so that the app will work when you deploy to platforms like [Heroku](https://heroku.com).


## Single-page app mode

By default, sirv will only respond to requests that match files in `public`. This is to maximise compatibility with static fileservers, allowing you to deploy your app anywhere.

If you're building a single-page app (SPA) with multiple routes, sirv needs to be able to respond to requests for *any* path. You can make it so by editing the `"start"` command in package.json:

```js
"start": "sirv public --single"
```

## Using TypeScript

This template comes with a script to set up a TypeScript development environment, you can run it immediately after cloning the template with:

```bash
node scripts/setupTypeScript.js
```

Or remove the script via:

```bash
rm scripts/setupTypeScript.js
```

If you want to use `baseUrl` or `path` aliases within your `tsconfig`, you need to set up `@rollup/plugin-alias` to tell Rollup to resolve the aliases. For more info, see [this StackOverflow question](https://stackoverflow.com/questions/63427935/setup-tsconfig-path-in-svelte).

## Deploying to the web

### With [Vercel](https://vercel.com)

Install `vercel` if you haven't already:

```bash
npm install -g vercel
```

Then, from within your project folder:

```bash
cd public
vercel deploy --name my-project
```

### With [surge](https://surge.sh/)

Install `surge` if you haven't already:

```bash
npm install -g surge
```

Then, from within your project folder:

```bash
npm run build
surge public my-project.surge.sh
```
