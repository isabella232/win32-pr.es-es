---
title: Error de tabIndex del rol de contenedor de ARIA (sin activos descendientes)
description: Error de tabIndex del rol de contenedor de ARIA (sin activos descendientes)
ms.assetid: E3CCA500-7104-4163-927C-94EA8F1E89D8
keywords:
- AriaContainerWithoutActiveDescendantTabIndexErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a01d3391d93b7e7f146f379bcfecd629e14bce7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268809"
---
# <a name="aria-container-role-without-active-descendant-tabindex-error"></a>Error de tabIndex del rol de contenedor de ARIA (sin activos descendientes)

## <a name="text"></a>Texto

El elemento es un contenedor que se pueda enfocar sin ningún descendiente activo definido, pero ningún elemento secundario tiene **TabIndex** mayor o igual que 0.

## <a name="type"></a>Tipo

Error

## <a name="description"></a>Descripción

Este error se aplica a los elementos que tienen un rol de contenedor, no tienen un atributo **Aria-activedescendant** y no están deshabilitados. Estos elementos implementan la navegación del teclado entre los elementos secundarios mediante el concepto conocido como *Índice itinerante*. En este concepto, los atributos **TabIndex** de los elementos secundarios se mantienen dinámicamente, asegurándose de que, en todo momento, solo un elemento secundario esté en el orden de tabulación.

Para corregir este error, establezca el atributo **TabIndex** de uno de los elementos secundarios en un valor igual o mayor que 0.

## <a name="example"></a>Ejemplo


```HTML
<div id="listbox" role="listbox1">
  <div role="option" id="listbox1-1" tabindex="0" class="selected">Item 1</div>
  <div role="option" id="listbox1-2">Item 2</div>
  <div role="option" id="listbox1-3">Item 3</div>
</div>

<script>

  ...

  listbox1.addEventListener('keyup', function(e) {
    var itm = e.srcElement;
    var prev = itm.previousElementSibling;
    var next = itm.nextElementSibling;

    if (e.keyCode == 38 && prev) {
      // Arrow up to move focus to the previous item.
      itm.setAttribute('tabindex', '-1');
      prev.setAttribute('tabindex','0');
      prev.focus();
    } 

    else if (e.keyCode == 40 && next) {
      // Arrow down to move focus to the next item.
      itm.setAttribute('tabindex', '-1');
      next.setAttribute('tabindex','0');
      next.focus();
    }
  });

</script>
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Error de tabIndex del contenedor de ARIA](aria-container-tabindex.md)
</dt> </dl>

 

 




