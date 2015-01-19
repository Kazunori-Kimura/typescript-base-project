# my TypeScript base project

## 前提

* `node.js` がインストールされていること。
* `tsd` がインストールされていること。

```sh
npm install -g tsd@next
```

## フォルダ構成とか

以下の様なフォルダ構成を想定しています。

    PROJECT_ROOT
    |   .gitignore
    |   package.json
    |   README.md
    |   tsd.json
    |
    +-- lib
    |       index.ts
    |
    +-- node_modules
    |
    `-- typings
            tsd.d.ts

## build方法

`npm run build` で TypeScriptのコンパイルを実施します。

実際には以下のコマンドを実行します。

```
> tsc --sourceMap --noImplicitAny --target es5 --module commonjs --out lib/index.js lib/index.ts
```

