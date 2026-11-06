# VueQuilly

A tiny Vue 3 component for building [Quill 2](https://quilljs.com/) editors in Vue and Nuxt apps.

**[Docs](https://vue-quilly-docs.vercel.app/)** · **[Live demo](https://vue-quilly.vercel.app/)** · **[npm](https://www.npmjs.com/package/vue-quilly)**

```bash
npm install vue-quilly quill@2
```

```vue
<script setup lang="ts">
import { ref } from 'vue'
import { QuillyEditor } from 'vue-quilly'
import 'quill/dist/quill.snow.css'

const content = ref('<p>Hello Quilly!</p>')
const loadQuill = () => import('quill')
</script>

<template>
  <QuillyEditor v-model="content" :options="{ theme: 'snow' }" :quill-class="loadQuill" />
</template>
```

## Why VueQuilly

You want a text editor that works, not a fight with configs.

- **Tiny.** About 1.3 KB gzipped. Quill loads after mount, in its own chunk.
- **Plain Quill.** Quill's own options, themes and plugins, and the Quill instance when you need it. No styles of its own.
- **HTML and Delta.** `v-model` with HTML or semantic HTML, and the Quill API for Delta.
- **Nuxt ready.** Works with SSR, without `<ClientOnly>`.
- **Component or composable.** `QuillyEditor`, or `useQuilly` on markup you render yourself.
- **TypeScript.** Typed props, events and composable.

Coming from VueQuill? See the [comparison](https://vue-quilly-docs.vercel.app/guide/vs-vuequill.html).

## What's new

- **1.3.0:** the `quill-class` prop. Pass the Quill class or a loader, and the editor sets itself up after mount, with no `initialize()` call. A loader keeps Quill out of the page bundle and off the server.
- **1.2.0:** the `useQuilly` composable.
- **Docs:** updated for 1.3.0, with guides for [plugins](https://vue-quilly-docs.vercel.app/guide/basic-usage.html#plugins-and-formats), [smaller bundles](https://vue-quilly-docs.vercel.app/guide/basic-usage.html#smaller-bundle-with-quill-core) and [Nuxt](https://vue-quilly-docs.vercel.app/guide/getting-started.html#nuxt-and-ssr).

## Repositories

| Repository | Contents |
| --- | --- |
| [vue-quilly](https://github.com/vue-quilly/vue-quilly) | The library and a Nuxt 4 example |
| [docs](https://github.com/vue-quilly/docs) | The [documentation site](https://vue-quilly-docs.vercel.app/) |
| [website](https://github.com/vue-quilly/website) | The [live demo](https://vue-quilly.vercel.app/) |

## Contributing

Ideas, issues and PRs are welcome 🙂 For bugs and feature ideas, open an [issue in vue-quilly](https://github.com/vue-quilly/vue-quilly/issues).

## Support

If you like it, give [vue-quilly](https://github.com/vue-quilly/vue-quilly) a ⭐ or back it on [Open Collective](https://opencollective.com/vuequilly). You can also [support the author](https://donatello.to/OleksandrShevchuk) directly.
