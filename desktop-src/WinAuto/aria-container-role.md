---
title: Error de rol de contenedor de ARIA
description: Error de rol de contenedor de ARIA
ms.assetid: AF207293-1172-43D0-B92C-C3070876DF54
keywords:
- AriaContainerRoleErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d02554c868816c05981fa9f008c8f79f0a3eb0f8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994536"
---
# <a name="aria-container-role-error"></a><span data-ttu-id="e5da9-104">Error de rol de contenedor de ARIA</span><span class="sxs-lookup"><span data-stu-id="e5da9-104">ARIA Container Role Error</span></span>

## <a name="text"></a><span data-ttu-id="e5da9-105">Texto</span><span class="sxs-lookup"><span data-stu-id="e5da9-105">Text</span></span>

<span data-ttu-id="e5da9-106">El elemento con el **descendiente activo** definido no tiene un rol de contenedor (**ComboBox**, **Grid**, **ListBox**, **Menu**, **MenuBar**, **RadioGroup**, **Tree**, **treegrid**, **Tablist**, **Row**).</span><span class="sxs-lookup"><span data-stu-id="e5da9-106">Element with **active-descendant** defined does not have a container role (**combobox**, **grid**, **listbox**, **menu**, **menubar**, **radiogroup**, **tree**, **treegrid**, **tablist**, **row**).</span></span>

## <a name="type"></a><span data-ttu-id="e5da9-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="e5da9-107">Type</span></span>

<span data-ttu-id="e5da9-108">Error</span><span class="sxs-lookup"><span data-stu-id="e5da9-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="e5da9-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="e5da9-109">Description</span></span>

<span data-ttu-id="e5da9-110">Este error se aplica a los elementos que tienen el atributo **Aria-activedescendant** .</span><span class="sxs-lookup"><span data-stu-id="e5da9-110">This error applies to elements that have the **aria-activedescendant** attribute.</span></span>

<span data-ttu-id="e5da9-111">Un elemento parece ser un contenedor que tiene establecido el atributo **Aria-activedescendant** , pero el atributo role del elemento no tiene un valor válido para un contenedor.</span><span class="sxs-lookup"><span data-stu-id="e5da9-111">An element appears to be a container that has the **aria-activedescendant** attribute set, but the element's role attribute doesn’t have a value that is valid for a container.</span></span>

<span data-ttu-id="e5da9-112">Para corregir este error, establezca el atributo **role** en un valor de rol de aplicaciones de Internet enriquecidas accesible desde una iniciativa de accesibilidad web (WAI-ARIA) que sea válido para un elemento contenedor: **ComboBox**, **Grid**, **ListBox**, **Menu**, **MenuBar**, **RadioGroup**, **Tablist**, **Tree** o **treegrid**.</span><span class="sxs-lookup"><span data-stu-id="e5da9-112">To fix this error, set the **role** attribute to a Web Accessibility Initiative - Accessible Rich Internet Applications (WAI-ARIA) role value that is valid for a container element: **combobox**, **grid**, **listbox**, **menu**, **menubar**, **radiogroup**, **tablist**, **tree**, or **treegrid**.</span></span>

## <a name="example"></a><span data-ttu-id="e5da9-113">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e5da9-113">Example</span></span>


```HTML
<div role="listbox" id="listbox1" tabindex="0" aria-activedescendant="listbox1-1">
  <div role="option" id="listbox1-1" class="selected">Item 1</div>
  <div role="option" id="listbox1-2">Item 2</div>
  <div role="option" id="listbox1-3">Item 3</div>
  ...
<div>
```



## <a name="related-topics"></a><span data-ttu-id="e5da9-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e5da9-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5da9-115">Error de rol de ARIA</span><span class="sxs-lookup"><span data-stu-id="e5da9-115">ARIA Role Error</span></span>](aria-role-invalid.md)
</dt> </dl>

 

 




