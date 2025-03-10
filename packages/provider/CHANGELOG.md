# @chakra-ui/provider

## 1.7.0

### Minor Changes

- [#4991](https://github.com/chakra-ui/chakra-ui/pull/4991)
  [`6095eaf9a`](https://github.com/chakra-ui/chakra-ui/commit/6095eaf9ac64a7e4d9f934bcb530bae2a92111a6)
  Thanks [@segunadebayo](https://github.com/segunadebayo)! - Update build system
  we use from a custom babel cli setup to
  [preconstruct](https://preconstruct.tools/).

  The previous build system transpiles the code in `src` directory to `dist/esm`
  and `dist/cjs` keeping the same file structure. The new build system merges
  all files in `src` and transpiles to a single `esm` and `cjs` file.

  **Potential Breaking Change:** The side effect of this is that, if you
  imported any function, component or hook using the **undocumented** approach
  like
  `import { useOutsideClick } from "@chakra-ui/hooks/dist/use-outside-click"`,
  you'll notice that the this doesn't work anymore.

  Here's how to resolve it:

  ```jsx live=false
  // Won't work 🎇
  import { useOutsideClick } from "@chakra-ui/hooks/dist/use-outside-click"

  // Works ✅
  import { useOutsideClick } from "@chakra-ui/hooks"
  ```

  If this affected your project, we recommend that you import hooks, functions
  or components the way it's shown in the documentation. This will help keep
  your project future-proof.

### Patch Changes

- Updated dependencies
  [[`6095eaf9a`](https://github.com/chakra-ui/chakra-ui/commit/6095eaf9ac64a7e4d9f934bcb530bae2a92111a6)]:
  - @chakra-ui/css-reset@1.1.0
  - @chakra-ui/react-env@1.1.0
  - @chakra-ui/hooks@1.7.0
  - @chakra-ui/portal@1.3.0
  - @chakra-ui/system@1.8.0
  - @chakra-ui/utils@1.9.0

## 1.6.11

### Patch Changes

- Updated dependencies []:
  - @chakra-ui/system@1.7.6

## 1.6.10

### Patch Changes

- Updated dependencies
  [[`5fe9b552b`](https://github.com/chakra-ui/chakra-ui/commit/5fe9b552bcae55935d1ab8ffde86b701075e6e6a),
  [`ed79a9cfb`](https://github.com/chakra-ui/chakra-ui/commit/ed79a9cfb35fec67bfe95bbc2a04a11d0d00fbfe),
  [`cd0893c56`](https://github.com/chakra-ui/chakra-ui/commit/cd0893c561d8c72b69db7c03d10adae752468a4f)]:
  - @chakra-ui/hooks@1.6.2
  - @chakra-ui/system@1.7.5
  - @chakra-ui/utils@1.8.4
  - @chakra-ui/portal@1.2.11
  - @chakra-ui/react-env@1.0.8

## 1.6.9

### Patch Changes

- Updated dependencies
  [[`c06d242c6`](https://github.com/chakra-ui/chakra-ui/commit/c06d242c672a10f93fab4dc2321143beae2db669),
  [`a9d1dc4ac`](https://github.com/chakra-ui/chakra-ui/commit/a9d1dc4ac874825f292d874ad4eadaf060fed436),
  [`5b4d8ef24`](https://github.com/chakra-ui/chakra-ui/commit/5b4d8ef24017dab1d69aeb5016b53366bdb3bcfd)]:
  - @chakra-ui/utils@1.8.3
  - @chakra-ui/hooks@1.6.1
  - @chakra-ui/react-env@1.0.7
  - @chakra-ui/portal@1.2.10
  - @chakra-ui/system@1.7.4

## 1.6.8

### Patch Changes

- [`17c84be66`](https://github.com/chakra-ui/chakra-ui/commit/17c84be66fcb68e77a838cbb900315caaaf61d26)
  Thanks [@segunadebayo](https://github.com/segunadebayo)! - - Resolve
  dependency issues caused by previous release
  - Add `ChakraProviderProps` type what was removed in previous release

## 1.6.7

### Patch Changes

- [`52640a1fd`](https://github.com/chakra-ui/chakra-ui/commit/52640a1fd9089e3c0ffc5dc8e42fcfa7a5752904)
  [#4594](https://github.com/chakra-ui/chakra-ui/pull/4594) Thanks
  [@feychenie](https://github.com/feychenie)! - Move ChakraProvider to a
  separate package `@chakra-ui/provider`

- Updated dependencies
  [[`01c913309`](https://github.com/chakra-ui/chakra-ui/commit/01c913309819c342806307291d2d60aea0122ecf),
  [`28af4c030`](https://github.com/chakra-ui/chakra-ui/commit/28af4c0308e234871548c0857e946e33ff18a130)]:
  - @chakra-ui/system@1.7.3
  - @chakra-ui/hooks@1.6.0
