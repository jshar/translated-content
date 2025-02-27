---
title: CSSStyleDeclaration.cssFloat
slug: Web/API/CSSStyleDeclaration/cssFloat
tags:
  - API
  - CSSOM
  - CSSStyleDeclaration
  - Reference
translation_of: Web/API/CSSStyleDeclaration/cssFloat
browser-compat: api.CSSStyleDeclaration.cssFloat
---
{{APIRef("CSSOM")}}

**`cssFloat`** は {{domxref("CSSStyleDeclaration")}} インターフェイスのプロパティで、 {{DOMxRef("CSSStyleDeclaration.getPropertyValue()")}} を `float` を引数として呼び出したときの結果を返します。

設定したときは、 {{DOMxRef("CSSStyleDeclaration.setProperty()")}} を `float` を第一引数、指定された値を第二引数として呼び出します。指定された値は {{cssxref("float")}} プロパティで有効な値でなければなりません。

## 構文

```js
var float = CSSStyleDeclaration.cssFloat();
CSSStyleDeclaration.cssFloat = "right"
```

### 値

{{domxref('CSSOMString')}} です。

## 例

以下の例では、スタイルシートには、 1 つだけのルール `.box` に {{cssxref("float")}} プロパティの値が `left` と設定されています。この値は `cssFloat` から返されます。次に、 `cssFloat` を使用して値を "right" に設定し、新しい値を返します。

```css
.box {
  float: left;
  inline-size: 300px;
}
```

```js
let myRules = document.styleSheets[0].cssRules;
let rule = myRules[0];
console.log(rule.style.cssFloat); // "left"
rule.style.cssFloat = "right";
console.log(rule.style.cssFloat); //right
```

## 仕様書

{{Specifications}}

## ブラウザーの互換性

{{Compat}}
