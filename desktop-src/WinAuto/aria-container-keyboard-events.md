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
# <a name="aria-container-role-keyboard-accessibility-error"></a><span data-ttu-id="adf82-104">Error de accesibilidad de teclado del rol de contenedor de ARIA</span><span class="sxs-lookup"><span data-stu-id="adf82-104">ARIA Container Role Keyboard Accessibility Error</span></span>

## <a name="text"></a><span data-ttu-id="adf82-105">Texto</span><span class="sxs-lookup"><span data-stu-id="adf82-105">Text</span></span>

<span data-ttu-id="adf82-106">Es un contenedor con funcionalidad de mouse personalizado y descendiente activo, pero sin la funcionalidad de teclado correspondiente: Controladores de eventos de JavaScript para **onkeydown** o **OnKeyPress**.</span><span class="sxs-lookup"><span data-stu-id="adf82-106">Element is a container with active descendant and custom mouse functionality but without the corresponding keyboard functionality: JavaScript event handlers for **OnKeyDown** or **OnKeyPress**.</span></span>

## <a name="type"></a><span data-ttu-id="adf82-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="adf82-107">Type</span></span>

<span data-ttu-id="adf82-108">Error</span><span class="sxs-lookup"><span data-stu-id="adf82-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="adf82-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="adf82-109">Description</span></span>

<span data-ttu-id="adf82-110">Este error se aplica a los elementos que tienen el atributo **Aria-activedescendant** .</span><span class="sxs-lookup"><span data-stu-id="adf82-110">This error applies to elements that have the **aria-activedescendant** attribute.</span></span> <span data-ttu-id="adf82-111">Estos elementos tienen uno o varios controladores de eventos del mouse (**MouseMove**, **MouseDown** o **MouseUp**), pero faltan los controladores de eventos de teclado equivalentes (**KeyDown**, **KeyUp** o **KeyPress**).</span><span class="sxs-lookup"><span data-stu-id="adf82-111">These elements have one or more mouse event handlers (**mousemove**, **mousedown** or **mouseup**), but are missing the equivalent keyboard event handlers (**keydown**, **keyup** or **keypress**).</span></span> <span data-ttu-id="adf82-112">Los controladores de eventos de teclado son necesarios para asegurarse de que el usuario puede invocar la funcionalidad del elemento mediante el teclado y para asegurarse de que el elemento mantiene el atributo **Aria-activedescendant** .</span><span class="sxs-lookup"><span data-stu-id="adf82-112">The keyboard event handlers are needed to ensure that the user can invoke the element's functionality by using the keyboard, and to ensure that the element maintains the **aria-activedescendant** attribute.</span></span>

<span data-ttu-id="adf82-113">Para corregir este error, implemente uno de los controladores de eventos de teclado.</span><span class="sxs-lookup"><span data-stu-id="adf82-113">To fix this error, implement one of the keyboard event handlers.</span></span>

## <a name="example"></a><span data-ttu-id="adf82-114">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="adf82-114">Example</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="adf82-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="adf82-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="adf82-116">Rol de contenedor de ARIA (sin descendientes activo) error de accesibilidad de teclado</span><span class="sxs-lookup"><span data-stu-id="adf82-116">ARIA Container Role (without active descendant) Keyboard Accessibility Error</span></span>](aria-container--no-active-descendants--keyboard-events.md)
</dt> </dl>

 

 




