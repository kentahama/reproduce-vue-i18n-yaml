# Vite i18n yaml reproduction

```shellsession
$ yarn
$ yarn dev
```

then opening `http://localhost:5173/` shows an error

```
[plugin:unplugin-vue-i18n] Cannot read properties of undefined (reading 'message')
/home/hamanaka/github/reproduce-vite-i18n-yaml/src/App.vue
    at Object.newOptions.onError (/home/hamanaka/github/reproduce-vite-i18n-yaml/node_modules/@intlify/bundle-utils/lib/codegen.js:102:48)
    at Object.newOptions.onError (/home/hamanaka/github/reproduce-vite-i18n-yaml/node_modules/@intlify/bundle-utils/lib/codegen.js:102:36)
    at newOptions.onError (/home/hamanaka/github/reproduce-vite-i18n-yaml/node_modules/@intlify/bundle-utils/lib/codegen.js:102:36)
    at emitError (/home/hamanaka/github/reproduce-vite-i18n-yaml/node_modules/@intlify/bundle-utils/node_modules/@intlify/message-compiler/dist/message-compiler.cjs:866:13)
    at parseLinked (/home/hamanaka/github/reproduce-vite-i18n-yaml/node_modules/@intlify/bundle-utils/node_modules/@intlify/message-compiler/dist/message-compiler.cjs:966:13)
    at parseMessage (/home/hamanaka/github/reproduce-vite-i18n-yaml/node_modules/@intlify/bundle-utils/node_modules/@intlify/message-compiler/dist/message-compiler.cjs:1057:36)
    at parseResource (/home/hamanaka/github/reproduce-vite-i18n-yaml/node_modules/@intlify/bundle-utils/node_modules/@intlify/message-compiler/dist/message-compiler.cjs:1096:25)
    at Object.parse (/home/hamanaka/github/reproduce-vite-i18n-yaml/node_modules/@intlify/bundle-utils/node_modules/@intlify/message-compiler/dist/message-compiler.cjs:1111:21)
    at baseCompile (/home/hamanaka/github/reproduce-vite-i18n-yaml/node_modules/@intlify/bundle-utils/node_modules/@intlify/message-compiler/dist/message-compiler.cjs:1425:24)
    at generateMessageFunction (/home/hamanaka/github/reproduce-vite-i18n-yaml/node_modules/@intlify/bundle-utils/lib/codegen.js:105:67
Click outside or fix the code to dismiss.
You can also disable this overlay by setting server.hmr.overlay to false in vite.config.js.
```

# The problematic part

https://github.com/kentahama/reproduce-vue-i18n-yaml/blob/main/src/App.vue#L37-L41
