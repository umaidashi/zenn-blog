---
title: "Ant Designは夢のUIテーマパークだった"
emoji: "🎡"
type: "tech" # tech: 技術記事 / idea: アイデア
topics: ["antd", "uiux", "react"]
published: true
---

おいどん。です
最近、「Ant Design」というUIフレームワークを知り、用意されているコンポーネントが夢のようだったので記録しました

# Ant Designとは（以下antd）

- MUIやChakraUIのようなUIフレームワークの一つ
- Reactで使えるUIフレームワーク（vueでも使えないことはない）
- TypeScriptおっけー
- 複数言語サポート
- 強力なテーマのカスタマイズ
- Next.js(v13も), Vite, Umi 対応


# 感動ポイント

## トップページの背景も触れる！？

antdトップページのHero画像の部分にあるコンポーネント郡がさわれるようになっていました
始め画像かと思っていましたが、vimiumでボタンが押せるようになっていたので気づきました

https://ant.design/

## 豊富なコンポーネントの種類

antdにはmuiなどほかのUIフレームワークにないコンポーネントがいくつもあります

### Color Picker

https://ant.design/components/color-picker

muiやchakraUIにはないカラーピッカーがあります

htmlタグの`<input type="color">`で表示される一般的なカラーピッカーに加えて、よりリッチなUIが用意されていたり、presetを自由に設定できます
トリガーもボタンなどに変更できるので、自由にUIを組めます

reactライブラリの`react-color`や`githubPicker`あたりの機能を含有しています

### QRCode

https://ant.design/components/qr-code

QRCodeを生成してくれるコンポーネントも用意されています

文字列をリアルタイムにQRコードにしてくれます
`errorLevel`を設定できたり、アイコンを埋め込んだりできます
ダウンロードのロジックは自作する必要があるみたいです

### Tour

いわゆるチュートリアル的な機能を実装できます
一度ページ開いて試してみるとわかりやすいと思います

https://ant.design/components/tour

`ref`を指定した要素に順番にフォーカスし、吹き出しを表示することができます。
webアプリなど作る際に導入すると、UXバク上がりですね

以下のようなライブラリが必要なくなります
- Intro.js
- React Joyride
- React Shepherd.js
- Reactour


### Anchor

https://ant.design/components/anchor

要素にidを指定するだけで、要素の表示位置に応じてZennやQiitaの目次のようなものを表示できます
読み物系のページであれば便利ですね

### Image

https://ant.design/components/image

AvatorでもなくImageコンポーネントです
antdのpreview機能がすごいです
上下反転、左右反転、回転、拡大縮小がデフォでついてます
ツールバーもカスタマイズできる仕様です

---

使えるコンポーネントが多いと、ライブラリ幾つも入れたりせずに、テーマも統一間持たせられるのでいいですね
上記以外にも、DatePicker, TImePicker, Uploader, Cascader, Carousel, Calendarなどたくさんあるので、ドキュメント見てみて下さい
楽しいです

https://ant.design/components/overview/



# 使い方

https://ant.design/docs/react/use-with-create-react-app

公式ドキュメントがわかりやすいので↑を見てみて下さい

Next.jsの場合は↓です
https://ant.design/docs/react/use-with-next

## 注意！Next.jsでTailwindと共存させたい場合

next.jsでtailwindを使いつつantdを使いたい場合、公式ドキュメントの設定方法ではボタンの背景が透けてしまいます
以下を`tailwind.config.ts`に追記してください

```tailwind.config.ts
corePlugins: {
  preflight: false,
},
```
参考
https://zenn.dev/teba_eleven/articles/b4bb429e87859e

# おわりに

antdをまだしっかり使っていないのですが、使いたくてワクワクしています
まるで夢のテーマパークですね

