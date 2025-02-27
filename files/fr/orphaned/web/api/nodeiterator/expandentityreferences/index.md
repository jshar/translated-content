---
title: NodeIterator.expandEntityReferences
slug: orphaned/Web/API/NodeIterator/expandEntityReferences
tags:
  - API
  - Arborescence
  - DOM
  - Itérateur
  - Noeuds
  - Propriété
translation_of: Web/API/NodeIterator/expandEntityReferences
original_slug: Web/API/NodeIterator/expandEntityReferences
---

{{APIRef("DOM")}} {{deprecated_header}}

La propriété en lecture seule **`NodeIterator.expandEntityReferences`** renvoie un {{domxref("Boolean")}} (_booléen_) indiquant si les enfants des noeuds de référence d'entité sont visibles ou non pour le {{domxref("NodeIterator")}}.

Si cette valeur est `false` (_faux_), les enfants des nœuds de référence d'entité (ainsi que tous leurs descendants) sont rejetés. Cela a préséance sur la valeur de la méthode  {{domxref("NodeIterator.whatToShow")}} et le filtre associé.

## Syntaxe

```js
expand = nodeIterator.expandEntityReferences;
```

## Exemple

```js
var nodeIterator = document.createNodeIterator(
    document.body,
    NodeFilter.SHOW_ELEMENT,
    { acceptNode: function(node) { return NodeFilter.FILTER_ACCEPT; } },
    false
);
expand = nodeIterator.expandEntityReferences;
```

## Spécifications

{{Specifications}}

## Compatibilité des navigateurs

{{Compat}}

## Voir aussi

- L'interface à laquelle cette propriété appartient : {{domxref("NodeIterator")}}.
