## 0.13.1 (2023-03-21)

893e361 refactor!: improve Pre-Bundling #35

## 0.13.0 (2023-03-20)

#### Break!

Since `0.13.0`, Pre-Bundling will be handled automatically within the plugin

#### Main Changed

- 485a516 feat!: Pre-Bundling modules for Electron Renderer process

## 0.12.1 (2023-02-09)

#### Main Changed

9803675 fix(test): the right time
41bff23 fix: `optimizeDeps.exclude` builtin modules #27

## 0.12.0 (2023-02-09)

#### Main Changed

- c97bd16 refactor: better builtins build
- 61e9e05 refactor: better polyfill with `nodeIntegration:false` #24
- 4ef703c feat: lazy load `esbuild`
- 06e7f31 Merge pull request #25 from electron-vite/vitest
- 35bb551 feat(test): integrate vitest

## 0.11.4 (2023-01-04)

- 502f7f2 feat: support Pre-Bundling cache #15

## 0.11.3 (2022-11-18)

- cbab7db fix: insert built-in modules to `optimizeDeps.exclude`

## 0.11.2 (2022-11-18)

1. Pre-Bundling Node.js built-in modules by default.
2. Fixed incorrect loading of static resources *(It does not support custom assetsDir)*.

- ee51908 feat: build built-in modules 🌱
- 51d5287 fix: `assetsDir` default value
- 5d0dfc0 refactor: always Pre-Bundling built-in modules

## 0.11.1 (2022-11-16)

- a8c546b fix: add 'vite-plugin-electron-renderer/electron-renderer' to `optimizeDeps.exclude`.

## 0.11.0 (2022-11-15)

#### Break!

1. All Node.js APIs must be Pre-Bundling via `optimizeDeps` *(the 'electron' module does not need to be built)*, this brings the benefit of being able to use it in Web Worker at the same time.
2. Remove `worker()` plugin.
3. Use Vite to build all source code, and will no longer support importing a plugin separately.

- c9b42be refactor: build with Vite
- d31f314 electron-renderer.js
- 2904e03 feat: `nodeIntegration` in build-config.ts
- 4d292fb feat: `optimizeDeps` support Node.js built-in modules
- 522955c refactor!: remove `worker()`, remove Node.js API support.

## 0.10.4 (2022-11-14)

`optimizerDeps` should not process builtins, builtins will be processed in `use-node.js.ts`.

- 6436b49 fix: avoid built-in modules

## 0.10.3 (2022-11-09)

- `optimizerDeps` generate sourcemap by default vite-plugin-electron#70

---

[v0.9.0~v0.10.2 | CHANGELOG](https://github.com/electron-vite/vite-plugin-electron/blob/v0.10.2/CHANGELOG.md)

## [2022-08-11] v0.8.8

sync `vite-plugin-electron` version

## [2022-08-08] v0.8.5

- 1cc4f40 fix(🌱): support Vite3 - [Uncaught TypeError: Failed to construct 'URL': Invalid URL (vite 3) #44](https://github.com/electron-vite/vite-plugin-electron/issues/44)
- 32f7755 feat(🌱): output ESM format - [TypeError: electron is not a function #45](https://github.com/electron-vite/vite-plugin-electron/issues/45)

## [2022-07-21] v0.8.1

- 33b121a chore(deps): hoist `typescript`
- 9d5fd94 fix(🐞): filter out keywords
- d3c1d7a chore(renderer): update config
- 298e4de refactor(renderer): `electron-renderer/plugins` -> `electron-renderer/src`
- 841cbd1 docs(electron-renderer): update
- 3994b9a chore(electron-renderer): fix link
- 72efa81 docs(electron-renderer): update

## [2022-07-19] v0.6.0

- be80d0c vite-plugin-electron-renderer@0.6.0
- 7e69a7c docs: `vite-plugin-electron-renderer@0.6.0`
- da89e79 remove `electron-renderer/index.d.ts`
- 581ef71 chore(deps): bump vite to 3.0.2
- 716485b refactor vite-plugin-electron-renderer with TypeScript
- baf5e80 refactor use-node.js with TypeScript
- 7e3fd3d refactor polyfill-exports with TypeScript
- 2249834 refactor build-config with TypeScript
- 8dad5e2 refactor(🚨): exclude `dependencies` as external by default
- 0163d12 feat: `scripts.dev`
- 3ad4b41 feat: `scripts.build` `scripts.dev`
- 48a0338 monorepo: add `packages/electron-renderer`

## [2022-07-11] v0.5.7

- 71799c7 fix(🐞): `cwd is not defined`

## [2022-07-11] v0.5.6

- d31f917 refactor: `root: string` instead of `config: UserConfig`

## [2022-07-11] v0.5.5

- 7f5117b chore: types
- 17eab4d fix(🐞): build Electron-Renderer
- f5ea26c remove `plugins/use-node.js/electron-renderer.js`

## [2022-07-10] v0.5.4

- 75b60c2 docs: v0.5.4
- 1b933d2 refactor(🌱): better logic

## [2022-07-07] v0.5.3

- 69eb531 docs: v0.5.3
- cc98ed9 feat: `ResolveModules['options']`  optional
- db03a72 chore: remove `useNodeJs.default = useNodeJs`
- c30dc1b fix(🐞): add `electron` to ` builtins

## [2022-07-07] v0.5.2

- 9dd8d4c feat: export `resolveModules()`
- 609e582 feat: interface `ResolveModules`
- dc6d6f6 docs: update
- 201eb71 docs: 🚨 ESM packages
- c8fe50b docs: `import { ipcRenderer } from 'electron'`

## [2022-07-01] v0.5.1

- ec224db refactor: optimize code
- f0efdfb fix(🐞): exclude ESM package
- f3e6b2c chore: optimize code
- 66df43b docs: update
- e2afb1e docs: `Electron-Renderer(vite serve)` flow chart
- 329056f docs: `dependencies` vs `devDependencies`
- d9734c9 Update README.md

## [2022-06-28] v0.5.0

- 6f3d745 fix(🐞): `require('fs')`
- 53845da feat: `config.build.emptyOutDir=false`
- 7cf9deb electron-renderer.js -> plugins/use-node.js/electron-renderer.js
- 7d537d5 docs: v0.5.0
- 2966399 refactor: standalone plugins
- ac356f2 feat: `vite-plugin-electron-renderer:use-node.js`
- 9798acd feat: `vite-plugin-electron-renderer:polyfill-exports`
- 0948df9 feat: `vite-plugin-electron-renderer:build-config`
- 9fb0e03 docs: update
- b6ec453 Update README.md
- 32acf9a docs: update
- d277390 docs: update

## [2022-06-27] v0.4.1

- a7a41a4 docs: v0.4.1
- 62b7584 feat: try resolve `package.json` from `process.cwd()`

## [2022-06-26] v0.4.0

- 87da81f docs: v0.4.0
- f2b860b remove README.zh-CN.md
- 130dce3 refactor: `resolve()` instead of `dependencies`
- 4a2620d refactor: from v0.3.3
