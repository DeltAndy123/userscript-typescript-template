# userscript-typescript-template

Template repo using Webpack and TypeScript to build your userscript for Tampermonkey and more extensions.

Automatically generate headers from your package.json!

## Usage

### 1. Generate repository (two-ways)

#### - Use this template to create your new repository

![](./images/github-use-template.png)

#### - Clone this repository

```bash
# Use Github CLI
$ gh repo clone pboymt/userscript-typescript-template
# Or use 'git clone' command directly
$ git clone https://github.com/pboymt/userscript-typescript-template.git
```

### Development

1. Install dependencies with `npm install` (or `pnpm install`) or `npm ci` (or `pnpm install --frozen-lockfile`).
2. Edit settings in `userscript` object in [`package.json`](./package.json), you can refer to the comments in [`plugins/userscript.plugin.ts`](./plugins/userscript.plugin.ts).
3. Code your userscript in `src` directory (like [`src/index.ts`](./src/index.ts)).
4. Generate userscript with `npm run build` (or `pnpm run build`).

### Testing

After you run `npm run build` (or `pnpm run build`), copy everything in `userscripts/loader.prod.user.js` and paste as a new userscript in your userscript manager (like Tampermonkey).

Make sure you have enabled `Allow access to file URLs` in Tampermonkey settings.
1. Go to chrome://extensions/ in your browser.
2. Find Tampermonkey and click `Details` under it.
3. Enable `Allow access to file URLs` in `Site access` section.

### Compile other file types

You need install other loader plugins to support other file types.

For example, you can use `scss-loader` to compile `.scss` files. Install it with `npm install --save-dev scss-loader node-sass` and add it in [`webpack.config.ts`](./webpack.config.ts). 

### Publish your userscript

You can publish your userscript to [Greasy Fork](https://greasyfork.org/) or other websites.

You can push your userscript to [GitHub](https://github.com) and import it to [Greasy Fork](https://greasyfork.org/import).