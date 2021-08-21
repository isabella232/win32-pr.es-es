---
title: Error de tabindex del rol de contenedor ARIA (sin descendiente activo)
description: Error de tabindex del rol de contenedor ARIA (sin descendiente activo)
ms.assetid: E3CCA500-7104-4163-927C-94EA8F1E89D8
keywords:
- AriaContainerWithoutActiveDescendantTabIndexErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6eb2198b5ad28cf8a2dd1c625342fef399eefbe3f93ed5e09f4796e06d16338
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994345"
---
# <a name="aria-container-role-without-active-descendant-tabindex-error"></a>Error de tabindex del rol de contenedor ARIA (sin descendiente activo)

## <a name="text"></a>Texto

Element es un contenedor que se puede centrar sin el descendiente activo definido, pero ningún elemento secundario tiene **tabindex** mayor o igual que 0.

## <a name="type"></a>Tipo

Error

## <a name="description"></a>Descripción

Este error se aplica a los elementos que tienen un rol de contenedor, no tienen un atributo **aria-activedescendant** y no están deshabilitados. Estos elementos implementan la navegación mediante el teclado entre elementos secundarios mediante el concepto conocido como *índice de aprobación.* En este concepto, los atributos **tabindex** de los elementos secundarios se mantienen dinámicamente, lo que garantiza que en todo momento solo un elemento secundario esté en orden de tabulación.

Para corregir este error, establezca el atributo **tabindex** de uno de los elementos secundarios en un valor igual o mayor que 0.

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

[Error de tabindex del contenedor de ARIA](aria-container-tabindex.md)
</dt> </dl>

 

 




