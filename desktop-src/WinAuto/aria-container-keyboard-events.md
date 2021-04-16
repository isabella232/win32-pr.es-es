---
title: Error de accesibilidad de teclado del rol de contenedor de ARIA
description: Error de accesibilidad de teclado del rol de contenedor de ARIA
ms.assetid: 364F26D7-7B65-418B-9DA5-F3B7B59284F7
keywords:
- AriaContainerKeyboardAccessibilityErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 085591e4f4834e8088b5ca199918d621f518e678
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357339"
---
# <a name="aria-container-role-keyboard-accessibility-error"></a>Error de accesibilidad de teclado del rol de contenedor de ARIA

## <a name="text"></a>Texto

Es un contenedor con funcionalidad de mouse personalizado y descendiente activo, pero sin la funcionalidad de teclado correspondiente: Controladores de eventos de JavaScript para **onkeydown** o **OnKeyPress**.

## <a name="type"></a>Tipo

Error

## <a name="description"></a>Descripción

Este error se aplica a los elementos que tienen el atributo **Aria-activedescendant** . Estos elementos tienen uno o varios controladores de eventos del mouse (**MouseMove**, **MouseDown** o **MouseUp**), pero faltan los controladores de eventos de teclado equivalentes (**KeyDown**, **KeyUp** o **KeyPress**). Los controladores de eventos de teclado son necesarios para asegurarse de que el usuario puede invocar la funcionalidad del elemento mediante el teclado y para asegurarse de que el elemento mantiene el atributo **Aria-activedescendant** .

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

[Rol de contenedor de ARIA (sin descendientes activo) error de accesibilidad de teclado](aria-container--no-active-descendants--keyboard-events.md)
</dt> </dl>

 

 




