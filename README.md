# vue-cli-issue-reproduction

## Steps to reproduce

```bash
# install dependencies
npm install

# build a web component will throw error
./node_modules/.bin/vue-cli-service build --target wc --name hello-world src/components/HelloWorld.vue
```

## Error detail

```bash
Building for production as web component... ERROR  TypeError: Cannot read property 'tapAsync' of undefined
TypeError: Cannot read property 'tapAsync' of undefined
    at compiler.hooks.compilation.tap.compilation (/Users/******/Sources/vue-cli-demo/node_modules/@vue/cli-plugin-pwa/lib/HtmlPwaPlugin.js:18:63)
    at SyncHook.eval [as call] (eval at create (/Users/******/Sources/vue-cli-demo/node_modules/tapable/lib/HookCodeFactory.js:17:12), <anonymous>:15:1)
    at SyncHook.lazyCompileHook [as _call] (/Users/******/Sources/vue-cli-demo/node_modules/tapable/lib/Hook.js:35:21)
    at Compiler.newCompilation (/Users/******/Sources/vue-cli-demo/node_modules/webpack/lib/Compiler.js:451:26)
    at hooks.beforeCompile.callAsync.err (/Users/******/Sources/vue-cli-demo/node_modules/webpack/lib/Compiler.js:487:29)
    at AsyncSeriesHook.eval [as callAsync] (eval at create (/Users/******/Sources/vue-cli-demo/node_modules/tapable/lib/HookCodeFactory.js:24:12), <anonymous>:6:1)
    at AsyncSeriesHook.lazyCompileHook [as _callAsync] (/Users/******/Sources/vue-cli-demo/node_modules/tapable/lib/Hook.js:35:21)
    at Compiler.compile (/Users/******/Sources/vue-cli-demo/node_modules/webpack/lib/Compiler.js:482:28)
    at readRecords.err (/Users/******/Sources/vue-cli-demo/node_modules/webpack/lib/Compiler.js:221:11)
    at Compiler.readRecords (/Users/******/Sources/vue-cli-demo/node_modules/webpack/lib/Compiler.js:349:11)
    at hooks.run.callAsync.err (/Users/******/Sources/vue-cli-demo/node_modules/webpack/lib/Compiler.js:218:10)
    at AsyncSeriesHook.eval [as callAsync] (eval at create (/Users/******/Sources/vue-cli-demo/node_modules/tapable/lib/HookCodeFactory.js:24:12), <anonymous>:6:1)
    at AsyncSeriesHook.lazyCompileHook [as _callAsync] (/Users/******/Sources/vue-cli-demo/node_modules/tapable/lib/Hook.js:35:21)
    at hooks.beforeRun.callAsync.err (/Users/******/Sources/vue-cli-demo/node_modules/webpack/lib/Compiler.js:215:19)
    at AsyncSeriesHook.eval [as callAsync] (eval at create (/Users/******/Sources/vue-cli-demo/node_modules/tapable/lib/HookCodeFactory.js:24:12), <anonymous>:15:1)
    at AsyncSeriesHook.lazyCompileHook [as _callAsync] (/Users/******/Sources/vue-cli-demo/node_modules/tapable/lib/Hook.js:35:21)
```