---
title: Error de accesibilidad del teclado del rol de contenedor ARIA
description: Error de accesibilidad del teclado del rol de contenedor ARIA
ms.assetid: 364F26D7-7B65-418B-9DA5-F3B7B59284F7
keywords:
- AriaContainerKeyboardAccessibilityErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 591098ba6e38836f1f39d13e72495bc1d7a3d5f9fe088873661e3dd3a7e65d4a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122405"
---
# <a name="aria-container-role-keyboard-accessibility-error"></a>Error de accesibilidad del teclado del rol de contenedor ARIA

## <a name="text"></a>Texto

Element es un contenedor con funcionalidad de mouse personalizada y descendiente activa, pero sin la funcionalidad de teclado correspondiente: controladores de eventos de JavaScript para **OnKeyDown** **o OnKeyPress.**

## <a name="type"></a>Tipo

Error

## <a name="description"></a>Descripción

Este error se aplica a los elementos que tienen el **atributo aria-activedescendant.** Estos elementos tienen uno o varios controladores de eventos de mouse **(mousemove,** **mousedown** o **mouseup),** pero faltan los controladores de eventos de teclado equivalentes **(keydown,** **keyup** o **keypress**). Los controladores de eventos de teclado son necesarios para asegurarse de que el usuario puede invocar la funcionalidad del elemento mediante el teclado y para asegurarse de que el elemento mantiene el atributo **aria-activedescendant.**

Para corregir este error, implemente uno de los controladores de eventos de teclado.

## <a name="example"></a>Ejemplo


```HTML
<div role="listbox" id="listbox1" tabindex="0" aria-activedescendant="listbox1-1"> 
  <div role="option" id="listbox1-1" class="selected">Item 1</div>
  <div role="option" id="listbox1-2">Item 2</div>
  <div role="option" id="listbox1-3">Item 3</div>
</div>

<script>

   ...

  listbox1.addEventListener('keyup', function(e) {
    var itm = document.getElementById(this.getAttribute('aria-activedescendant'));
    var prev = itm.previousElementSibling;
    var next = itm.nextElementSibling;
    
    if ( e.keyCode  38 && prev ) {
      // Arrow up to move active descendant to the previous item
      itm.removeAttribute('class’);
      prev.setAttribute("class", "selected");
      this.setAttribute ('aria-activedescendant', prev.id)
    } 

    else if ( e.keyCode == 40 && next) {
      // Arrow down to move focus to the next item
      itm.removeAttribute('class’);
      next.setAttribute("class", "selected");
      this.setAttribute ('aria-activedescendant', next.id)
    }
  });      

</script>
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Error de accesibilidad del teclado del rol de contenedor ARIA (sin descendiente activo)](aria-container--no-active-descendants--keyboard-events.md)
</dt> </dl>

 

 




