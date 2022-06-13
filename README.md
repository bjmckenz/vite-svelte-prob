# vite-svelte-prob

# vite-svelte-prob
Demonstration of error building svelte with svelte-tablesort package

# Steps
* npm init svelte foo
* cd foo
* npm install
* npm install svelte-tablesort
* Copy example html from svelte-tablesort readme
* (Either) npm run build
* (or) npm run dev

# Results
* First, build fails with "TableSort not exported". Once that is hacked by adding "TableSort": "./TableSort.svelte" in the package.json, then vite complains that rollup failed to resolve it:

[vite]: Rollup failed to resolve import "svelte-tablesort" from "src/routes/index.svelte".
This is most likely unintended because it can break your application at runtime.
If you do want to externalize this module explicitly add it to
`build.rollupOptions.external`
> [vite]: Rollup failed to resolve import "svelte-tablesort" from "src/routes/index.svelte".
This is most likely unintended because it can break your application at runtime.
If you do want to externalize this module explicitly add it to
`build.rollupOptions.external`
This is most likely unintended because it can break your application at runtime.
If you do want to externalize this module explicitly add it to
`build.rollupOptions.external`
    at onRollupWarning (C:\Users\bjmckenz\Desktop\SOURCE\vite-svelte-prob\node_modules\vite\dist\node\chunks\dep-8f5c9290.js:41772:19)
    at onwarn (C:\Users\bjmckenz\Desktop\SOURCE\vite-svelte-prob\node_modules\vite\dist\node\chunks\dep-8f5c9290.js:41588:13)
    at Object.onwarn (C:\Users\bjmckenz\Desktop\SOURCE\vite-svelte-prob\node_modules\rollup\dist\shared\rollup.js:23224:13)
    at ModuleLoader.handleResolveId (C:\Users\bjmckenz\Desktop\SOURCE\vite-svelte-prob\node_modules\rollup\dist\shared\rollup.js:22508:26)
    at C:\Users\bjmckenz\Desktop\SOURCE\vite-svelte-prob\node_modules\rollup\dist\shared\rollup.js:22469:26

# package.json
	"devDependencies": {
		"@sveltejs/adapter-auto": "next",
		"@sveltejs/kit": "next",
		"eslint": "^8.16.0",
		"eslint-plugin-svelte3": "^4.0.0",
		"svelte": "^3.44.0",
		"svelte-check": "^2.7.1",
		"typescript": "^4.7.2"
	},
	"type": "module",
	"dependencies": {
		"svelte-tablesort": "^2.0.2"
	}
}
