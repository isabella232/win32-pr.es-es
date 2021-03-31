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
# <a name="aria-container-role-without-active-descendant-keyboard-accessibility-error"></a><span data-ttu-id="ac8df-104">Rol de contenedor de ARIA (sin descendientes activo) error de accesibilidad de teclado</span><span class="sxs-lookup"><span data-stu-id="ac8df-104">ARIA Container Role (without active descendant) Keyboard Accessibility Error</span></span>

## <a name="text"></a><span data-ttu-id="ac8df-105">Texto</span><span class="sxs-lookup"><span data-stu-id="ac8df-105">Text</span></span>

<span data-ttu-id="ac8df-106">Es un contenedor que se pueda enfocar sin ningún descendiente activo definido y sin controladores de eventos **onkeydown** / **OnKeyPress** / **onkeyup** (ni en el contenedor ni en uno de los elementos secundarios).</span><span class="sxs-lookup"><span data-stu-id="ac8df-106">Element is a focusable container without active descendant defined and without **OnKeyDown**/**OnKeyPress**/**OnKeyUp** event handlers (neither on container nor on one of child elements).</span></span>

## <a name="type"></a><span data-ttu-id="ac8df-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="ac8df-107">Type</span></span>

<span data-ttu-id="ac8df-108">Error</span><span class="sxs-lookup"><span data-stu-id="ac8df-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="ac8df-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="ac8df-109">Description</span></span>

<span data-ttu-id="ac8df-110">Este error se aplica a los elementos que tienen un rol de contenedor, no tienen un atributo **Aria-activedescendant** y no están deshabilitados.</span><span class="sxs-lookup"><span data-stu-id="ac8df-110">This error applies to elements that have a container role, do not have an **aria-activedescendant** attribute, and are not disabled.</span></span> <span data-ttu-id="ac8df-111">Estos elementos implementan la navegación del teclado entre los elementos secundarios mediante el concepto conocido como *Índice itinerante*.</span><span class="sxs-lookup"><span data-stu-id="ac8df-111">These elements implement keyboard navigation among child elements by using the concept known as *roving index*.</span></span> <span data-ttu-id="ac8df-112">En este concepto, los atributos **TabIndex** de los elementos secundarios se mantienen dinámicamente, asegurándose de que, en todo momento, solo un elemento secundario esté en el orden de tabulación.</span><span class="sxs-lookup"><span data-stu-id="ac8df-112">In this concept, the **tabindex** attributes of child elements are maintained dynamically, ensuring that at all times only one child element is in tab order.</span></span>

<span data-ttu-id="ac8df-113">Este error indica que un elemento contenedor que no tiene el atributo **Aria-activedescendant** y que no está deshabilitado no es accesible para los usuarios del teclado.</span><span class="sxs-lookup"><span data-stu-id="ac8df-113">This error indicates that a container element that does not have the **aria-activedescendant** attribute, and that is not disabled, is not accessible to keyboard users.</span></span> <span data-ttu-id="ac8df-114">El problema existe porque el contenedor no tiene los controladores de eventos de teclado necesarios (**KeyDown**, **KeyUp** o **KeyPress**) y ninguno de los elementos secundarios del contenedor.</span><span class="sxs-lookup"><span data-stu-id="ac8df-114">The problem exists because the container does not have the needed keyboard event handlers (**keydown**, **keyup**, or **keypress**), and neither do any of the container's child elements.</span></span>

<span data-ttu-id="ac8df-115">Para corregir este error, defina un controlador de eventos **KeyDown**, **KeyUp** o **KeyPress** para el contenedor o uno de sus elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="ac8df-115">To fix this error, define a **keydown**, **keyup**, or **keypress** event handler for the container or one of its child elements.</span></span>

## <a name="example"></a><span data-ttu-id="ac8df-116">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ac8df-116">Example</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="ac8df-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ac8df-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ac8df-118">Error de accesibilidad de teclado del rol de contenedor de ARIA</span><span class="sxs-lookup"><span data-stu-id="ac8df-118">ARIA Container Role Keyboard Accessibility Error</span></span>](aria-container-keyboard-events.md)
</dt> </dl>

 

 




