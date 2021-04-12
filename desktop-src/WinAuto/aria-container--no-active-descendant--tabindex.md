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
# <a name="aria-container-role-without-active-descendant-tabindex-error"></a><span data-ttu-id="71cc9-104">Error de tabIndex del rol de contenedor de ARIA (sin activos descendientes)</span><span class="sxs-lookup"><span data-stu-id="71cc9-104">ARIA Container Role (without active descendant) Tabindex Error</span></span>

## <a name="text"></a><span data-ttu-id="71cc9-105">Texto</span><span class="sxs-lookup"><span data-stu-id="71cc9-105">Text</span></span>

<span data-ttu-id="71cc9-106">El elemento es un contenedor que se pueda enfocar sin ningún descendiente activo definido, pero ningún elemento secundario tiene **TabIndex** mayor o igual que 0.</span><span class="sxs-lookup"><span data-stu-id="71cc9-106">Element is a focusable container without active descendant defined, but no child element has **tabindex** greater or equal to 0.</span></span>

## <a name="type"></a><span data-ttu-id="71cc9-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="71cc9-107">Type</span></span>

<span data-ttu-id="71cc9-108">Error</span><span class="sxs-lookup"><span data-stu-id="71cc9-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="71cc9-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="71cc9-109">Description</span></span>

<span data-ttu-id="71cc9-110">Este error se aplica a los elementos que tienen un rol de contenedor, no tienen un atributo **Aria-activedescendant** y no están deshabilitados.</span><span class="sxs-lookup"><span data-stu-id="71cc9-110">This error applies to elements that have a container role, do not have an **aria-activedescendant** attribute, and are not disabled.</span></span> <span data-ttu-id="71cc9-111">Estos elementos implementan la navegación del teclado entre los elementos secundarios mediante el concepto conocido como *Índice itinerante*.</span><span class="sxs-lookup"><span data-stu-id="71cc9-111">These elements implement keyboard navigation among child elements by using the concept known as *roving index*.</span></span> <span data-ttu-id="71cc9-112">En este concepto, los atributos **TabIndex** de los elementos secundarios se mantienen dinámicamente, asegurándose de que, en todo momento, solo un elemento secundario esté en el orden de tabulación.</span><span class="sxs-lookup"><span data-stu-id="71cc9-112">In this concept, the **tabindex** attributes of child elements are maintained dynamically, ensuring that at all times only one child element is in tab order.</span></span>

<span data-ttu-id="71cc9-113">Para corregir este error, establezca el atributo **TabIndex** de uno de los elementos secundarios en un valor igual o mayor que 0.</span><span class="sxs-lookup"><span data-stu-id="71cc9-113">To fix this error, set the **tabindex** attribute of one of the child elements to a value equal to or greater than 0.</span></span>

## <a name="example"></a><span data-ttu-id="71cc9-114">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="71cc9-114">Example</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="71cc9-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="71cc9-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71cc9-116">Error de tabIndex del contenedor de ARIA</span><span class="sxs-lookup"><span data-stu-id="71cc9-116">ARIA Container Tabindex Error</span></span>](aria-container-tabindex.md)
</dt> </dl>

 

 




