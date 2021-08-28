---
title: Error de accesibilidad del teclado del rol de contenedor ARIA (sin descendiente activo)
description: Error de accesibilidad del teclado del rol de contenedor ARIA (sin descendiente activo)
ms.assetid: 15EDD3CC-FC2A-42FC-95DD-B04D9AF3515E
keywords:
- AriaContainerWithoutActiveDescendantKeyboardAccessiblityId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30b653ac3bf2dc8254b25c52a89cdb3503b89b9f05997a3ea9fb4f4ef3a77cb7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071885"
---
# <a name="aria-container-role-without-active-descendant-keyboard-accessibility-error"></a>Error de accesibilidad del teclado del rol de contenedor ARIA (sin descendiente activo)

## <a name="text"></a>Texto

Element es un contenedor que se puede centrar sin el descendiente activo definido y sin controladores de eventos / **OnKeyDown** / **OnKeyPress OnKeyUp** (ni en el contenedor ni en uno de los elementos secundarios).

## <a name="type"></a>Tipo

Error

## <a name="description"></a>Descripción

Este error se aplica a los elementos que tienen un rol de contenedor, no tienen un atributo **aria-activedescendant** y no están deshabilitados. Estos elementos implementan la navegación mediante el teclado entre los elementos secundarios mediante el concepto conocido como *índice itinerante*. En este concepto, los atributos **tabindex** de los elementos secundarios se mantienen dinámicamente, lo que garantiza que en todo momento solo un elemento secundario esté en orden de tabulación.

Este error indica que un elemento contenedor que no tiene el atributo **aria-activedescendant** y que no está deshabilitado no es accesible para los usuarios del teclado. El problema existe porque el contenedor no tiene los controladores de eventos de teclado necesarios **(keydown,** **keyup** o **keypress)** y ninguno de los elementos secundarios del contenedor.

Para corregir este error, defina un controlador de eventos **keydown**, **keyup** o **keypress** para el contenedor o uno de sus elementos secundarios.

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

[Error de accesibilidad del teclado del rol de contenedor ARIA](aria-container-keyboard-events.md)
</dt> </dl>

 

 




