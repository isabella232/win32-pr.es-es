---
title: Rol de contenedor de ARIA (sin descendientes activo) error de accesibilidad de teclado
description: Rol de contenedor de ARIA (sin descendientes activo) error de accesibilidad de teclado
ms.assetid: 15EDD3CC-FC2A-42FC-95DD-B04D9AF3515E
keywords:
- AriaContainerWithoutActiveDescendantKeyboardAccessiblityId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d9e30e0194f156426e2b61aa774ac1f3e0f5b91
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903461"
---
# <a name="aria-container-role-without-active-descendant-keyboard-accessibility-error"></a>Rol de contenedor de ARIA (sin descendientes activo) error de accesibilidad de teclado

## <a name="text"></a>Texto

Es un contenedor que se pueda enfocar sin ningún descendiente activo definido y sin controladores de eventos **onkeydown** / **OnKeyPress** / **onkeyup** (ni en el contenedor ni en uno de los elementos secundarios).

## <a name="type"></a>Tipo

Error

## <a name="description"></a>Descripción

Este error se aplica a los elementos que tienen un rol de contenedor, no tienen un atributo **Aria-activedescendant** y no están deshabilitados. Estos elementos implementan la navegación del teclado entre los elementos secundarios mediante el concepto conocido como *Índice itinerante*. En este concepto, los atributos **TabIndex** de los elementos secundarios se mantienen dinámicamente, asegurándose de que, en todo momento, solo un elemento secundario esté en el orden de tabulación.

Este error indica que un elemento contenedor que no tiene el atributo **Aria-activedescendant** y que no está deshabilitado no es accesible para los usuarios del teclado. El problema existe porque el contenedor no tiene los controladores de eventos de teclado necesarios (**KeyDown**, **KeyUp** o **KeyPress**) y ninguno de los elementos secundarios del contenedor.

Para corregir este error, defina un controlador de eventos **KeyDown**, **KeyUp** o **KeyPress** para el contenedor o uno de sus elementos secundarios.

## <a name="example"></a>Ejemplo


```HTML
<div role="listbox" id="listbox1" >
  <div role="option" id="listbox1-1" tabindex="0" class="selected">Item 1</div>
  <div role="option" id="listbox1-2">Item 2</div>
  <div role="option" id="listbox1-3">Item 3</div>
  ...
<div>

<script>

  ...

  listbox1.addEventListener('keyup', function(e) {
    var itm = e.srcElement;
    var prev = itm.previousElementSibling;
    var next = itm.nextElementSibling;

    if (e.keyCode == 38 && prev) {
      // On arrow up move focus to the previous item.
      itm.setAttribute('tabindex', '-1');
      prev.setAttribute('tabindex','0');
      prev.focus();
    }

    else if (e.keyCode == 40 && next) {
      // On arrow down move focus to the next item.
      itm.setAttribute('tabindex', '-1');
      next.setAttribute('tabindex','0');
      next.focus();
    }
  });

</script>
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Error de accesibilidad de teclado del rol de contenedor de ARIA](aria-container-keyboard-events.md)
</dt> </dl>

 

 




