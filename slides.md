---
theme: default
colorSchema: light
background: false
class: text-center
highlighter: shiki
lineNumbers: true
shikiConfig:
  theme: 'balanced-dark'
drawings:
  persist: false
transition: slide-left
title: 小さな自動化をチームで育てるための設計と運用
mdc: true
fonts:
  provider: none
  sans: 'Noto Sans JP'
  mono: ui-monospace
---

<CoverSlide
  title="小さな自動化をチームで育てるための設計と運用を、型定義の生成を例に考える"
  event="イベント名"
  author="fujitani sora"
  background="cyanTop"
/>

<!--
スピーカーノート: ここにプレゼンテーションノートを書きます
-->

---

<ProfileSlide
  name="fujitani sora"
  affiliation="toridori inc engineer"
  x="sorafujitani"
  github="sorafujitani"
  website="https://sorafujitani.me/"
  avatar="https://raw.githubusercontent.com/fs0414/imgs/main/fs0414_dot_image.png"
  :items="[
    { icon: 'calendar', label: '2001 (25)' },
  ]"
/>

---

# 見出しスライド

## サブ見出し

通常のテキストと箇条書きの例です。

- <EmojiText emoji="✨">リスト項目1</EmojiText>
- <EmojiText emoji="🎨">リスト項目2</EmojiText>
  - ネストしたリスト
  - ネストしたリスト2
- <EmojiText emoji="🚀">リスト項目3</EmojiText>

---

# コードハイライト

TypeScript のコード例:

```ts {2-4|6-8|all}
// コードハイライトの例
interface User {
  name: string
  age: number
}

const user: User = {
  name: 'Taro',
  age: 25
}

console.log(user)
```

<v-click>

system monospace で ligature を無効化して表示

</v-click>

---

# compact code block

<div class="code-compact code-tight">

<div class="code-caption">src/generated/config.ts:12</div>

```ts {1-2}
"feature/example"?: RuleNoConfig
  | [Severity, FeatureExampleOptions]
```

</div>

---

# 生成コード紹介

<div class="nested-compact">

- 生成コマンド
  - `bun run generate && bun run build`
- 生成された型定義を短い抜粋で見せる
  - `src/generated/config.ts`

</div>

<div class="code-compact code-tight">

<div class="code-caption">src/generated/config.ts:12</div>

```ts
export interface GeneratedConfig {
  featureExample?: FeatureExampleOptions
}
```

</div>

---
layout: two-cols
---

# 2カラムレイアウト

左側のコンテンツ

- <EmojiText emoji="📝">ポイント1</EmojiText>
- <EmojiText emoji="💡">ポイント2</EmojiText>
- <EmojiText emoji="🎯">ポイント3</EmojiText>

::right::

# 右側

右側のコンテンツ

```js
const greet = (name) => `Hello, ${name}!`
console.log(greet('world'))
```

---

<GradientHeading :animated="true">
  グラデーション見出し
</GradientHeading>

アニメーション付きのグラデーション効果

<v-clicks>

- Purple to Blue のグラデーション
- アニメーションするテキストシャドウ
- oklch color space の活用

</v-clicks>

<div class="code-compact">

```css
.gradient-heading {
  background: linear-gradient(135deg,
    oklch(0.65 0.25 270) 0%,
    oklch(0.7 0.22 240) 50%,
    oklch(0.75 0.2 210) 100%
  );
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}
```

</div>

---

# 画像表示

<CenteredImage
  src="https://placehold.co/800x400"
  alt="サンプル画像"
  width="800px"
  caption="画像のキャプション"
/>

---
layout: center
---

# View Transition対応

<v-click>

<div class="text-6xl emoji">
🎬
</div>

</v-click>

<v-click>

モダンブラウザのView Transition APIに対応しています

</v-click>

---
layout: center
class: text-center
---

<GradientHeading class="text-4xl font-bold">see you later 👋</GradientHeading>
