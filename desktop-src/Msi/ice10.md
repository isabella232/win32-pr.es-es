---
description: ICE10 valida que el estado de anuncio de las características secundarias coincida con el de su característica primaria.
ms.assetid: b0e0d837-245e-4c38-a7c4-06dda0eea25c
title: ICE10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac8f1304f4444a0f087d747328cdea4b3d714ab0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667772"
---
# <a name="ice10"></a><span data-ttu-id="937fd-103">ICE10</span><span class="sxs-lookup"><span data-stu-id="937fd-103">ICE10</span></span>

<span data-ttu-id="937fd-104">ICE10 valida que el estado de anuncio de las características secundarias coincida con el de su característica primaria.</span><span class="sxs-lookup"><span data-stu-id="937fd-104">ICE10 validates that the advertise state of child features matches that of its parent feature.</span></span>

<span data-ttu-id="937fd-105">Es posible que una característica secundaria no permita el anuncio mientras su característica primaria permita el anuncio.</span><span class="sxs-lookup"><span data-stu-id="937fd-105">A child feature may not disallow advertisement while its parent feature allows advertisement.</span></span> <span data-ttu-id="937fd-106">Por lo tanto, la siguiente combinación de atributos primarios y secundarios no es válida.</span><span class="sxs-lookup"><span data-stu-id="937fd-106">The following combination of parent and child attributes is therefore invalid.</span></span>

``` syntax
parent = msidbFeatureAttributesFavorAdvertise 
child = msidbFeatureAttributesDisallowAdvertise
```

<span data-ttu-id="937fd-107">Esta combinación no es válida porque desactivaría el elemento primario cada vez que se supone que se anunciara el elemento primario.</span><span class="sxs-lookup"><span data-stu-id="937fd-107">This combination is invalid because it would turn off the parent whenever the parent was supposed to be advertised.</span></span> <span data-ttu-id="937fd-108">Sin embargo, se permite el orden inverso.</span><span class="sxs-lookup"><span data-stu-id="937fd-108">However, the reverse is allowed.</span></span> <span data-ttu-id="937fd-109">Un elemento secundario se puede marcar para favorecer el anuncio mientras el elemento primario está marcado para no permitir el anuncio.</span><span class="sxs-lookup"><span data-stu-id="937fd-109">A child can be marked to favor advertisement while the parent is marked to disallow advertisement.</span></span>

<span data-ttu-id="937fd-110">La acción personalizada ICE10 determina el estado de las características primarias y secundarias de la columna Attributes de la tabla de [características](feature-table.md) .</span><span class="sxs-lookup"><span data-stu-id="937fd-110">The ICE10 custom action determines the state of parent and child features from the Attributes column of the [Feature](feature-table.md) table.</span></span> <span data-ttu-id="937fd-111">Tenga en cuenta que es válido establecer el estado de una característica en 0 y tener su conjunto primario o secundario establecido en favorecer o deshabilitar el anuncio.</span><span class="sxs-lookup"><span data-stu-id="937fd-111">Note that it is valid to set the state of a feature to 0 and have its parent or child set to favor or disallow advertisement.</span></span>

## <a name="result"></a><span data-ttu-id="937fd-112">Resultado</span><span class="sxs-lookup"><span data-stu-id="937fd-112">Result</span></span>

<span data-ttu-id="937fd-113">ICE10 publica un error si la columna Attributes de la tabla de [características](feature-table.md) contiene una incoherencia en el estado de anuncio.</span><span class="sxs-lookup"><span data-stu-id="937fd-113">ICE10 posts an error if the Attributes column of the [Feature](feature-table.md) table contains a mismatch in the advertise state.</span></span>

## <a name="example"></a><span data-ttu-id="937fd-114">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="937fd-114">Example</span></span>

<span data-ttu-id="937fd-115">ICE10 envía el siguiente mensaje de error para el ejemplo que se muestra.</span><span class="sxs-lookup"><span data-stu-id="937fd-115">ICE10 posts the following error message for the example shown.</span></span>

``` syntax
Conflicting states, one favors, one disallows. Child: Word differs in advertise state 
from Parent: Office.
```

<span data-ttu-id="937fd-116">Tenga en cuenta que en este ejemplo Microsoft Excel y Microsoft Word son características secundarias de Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="937fd-116">Note for this example that Microsoft Excel and Microsoft Word are child features of Microsoft Office.</span></span>

<span data-ttu-id="937fd-117">Tabla de [características](feature-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="937fd-117">[Feature](feature-table.md) table (partial)</span></span>



| <span data-ttu-id="937fd-118">Característica</span><span class="sxs-lookup"><span data-stu-id="937fd-118">Feature</span></span> | <span data-ttu-id="937fd-119">Característica \_ principal</span><span class="sxs-lookup"><span data-stu-id="937fd-119">Feature\_Parent</span></span> | <span data-ttu-id="937fd-120">Atributos</span><span class="sxs-lookup"><span data-stu-id="937fd-120">Attributes</span></span> |
|---------|-----------------|------------|
| <span data-ttu-id="937fd-121">Office</span><span class="sxs-lookup"><span data-stu-id="937fd-121">Office</span></span>  | <span data-ttu-id="937fd-122">Null</span><span class="sxs-lookup"><span data-stu-id="937fd-122">Null</span></span>            | <span data-ttu-id="937fd-123">4</span><span class="sxs-lookup"><span data-stu-id="937fd-123">4</span></span>          |
| <span data-ttu-id="937fd-124">Excel</span><span class="sxs-lookup"><span data-stu-id="937fd-124">Excel</span></span>   | <span data-ttu-id="937fd-125">Office</span><span class="sxs-lookup"><span data-stu-id="937fd-125">Office</span></span>          | <span data-ttu-id="937fd-126">4</span><span class="sxs-lookup"><span data-stu-id="937fd-126">4</span></span>          |
| <span data-ttu-id="937fd-127">Word</span><span class="sxs-lookup"><span data-stu-id="937fd-127">Word</span></span>    | <span data-ttu-id="937fd-128">Office</span><span class="sxs-lookup"><span data-stu-id="937fd-128">Office</span></span>          | <span data-ttu-id="937fd-129">8</span><span class="sxs-lookup"><span data-stu-id="937fd-129">8</span></span>          |



 

<span data-ttu-id="937fd-130">En el ejemplo, Word se establece en no permitir anuncio, lo que entra en conflicto con el estado de anuncio de su elemento primario, Office.</span><span class="sxs-lookup"><span data-stu-id="937fd-130">In the example, Word is set to disallow advertisement, which conflicts with the allow advertisement state of its parent, Office.</span></span>

<span data-ttu-id="937fd-131">En algunos casos, ICE10 envía el siguiente error:</span><span class="sxs-lookup"><span data-stu-id="937fd-131">In some cases ICE10 posts the following error:</span></span>

``` syntax
Parent feature: 'Parent' not found for child feature: 'Child'. This error means 
that for the child feature 'Child', the feature 'Parent' is not listed in the 
Feature table.
```

<span data-ttu-id="937fd-132">Esto hace referencia a una referencia de clave externa no válida.</span><span class="sxs-lookup"><span data-stu-id="937fd-132">This refers to an invalid foreign key reference.</span></span> <span data-ttu-id="937fd-133">La solución consiste en tener el punto "secundario" a su característica primaria correcta o agregar una entrada para la característica primaria "primaria" a la tabla de [características](feature-table.md) .</span><span class="sxs-lookup"><span data-stu-id="937fd-133">The fix is to have 'Child' point to its correct parent feature, or add an entry for the parent feature 'Parent' to the [Feature](feature-table.md) table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="937fd-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="937fd-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="937fd-135">Referencia de ICE</span><span class="sxs-lookup"><span data-stu-id="937fd-135">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



