---
title: BOTÓN. cursor
description: El atributo cursor especifica o recupera el cursor que aparece cuando se mantiene el puntero del mouse sobre el botón.
ms.assetid: 19bdbb23-00e2-45cf-b67d-9ada036b9c3b
keywords:
- BOTÓN. cursor Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2641491a5a73498da2c43fd74d4187b5594e177
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699568"
---
# <a name="buttoncursor"></a><span data-ttu-id="a55a4-104">BOTÓN. cursor</span><span class="sxs-lookup"><span data-stu-id="a55a4-104">BUTTON.cursor</span></span>

<span data-ttu-id="a55a4-105">El atributo **cursor** especifica o recupera el cursor que aparece cuando se mantiene el puntero del mouse sobre el **botón**.</span><span class="sxs-lookup"><span data-stu-id="a55a4-105">The **cursor** attribute specifies or retrieves the cursor that appears when the mouse pointer hovers over the **BUTTON**.</span></span>

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a><span data-ttu-id="a55a4-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="a55a4-106">Possible Values</span></span>

<span data-ttu-id="a55a4-107">Este atributo es una **cadena** de lectura/escritura.</span><span class="sxs-lookup"><span data-stu-id="a55a4-107">This attribute is a read/write **String**.</span></span>



| <span data-ttu-id="a55a4-108">Value</span><span class="sxs-lookup"><span data-stu-id="a55a4-108">Value</span></span>            | <span data-ttu-id="a55a4-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="a55a4-109">Description</span></span>                                                                                |
|------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="a55a4-110">sistema</span><span class="sxs-lookup"><span data-stu-id="a55a4-110">system</span></span>           | <span data-ttu-id="a55a4-111">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="a55a4-111">Default.</span></span> <span data-ttu-id="a55a4-112">Cursor dependiente de la plataforma (normalmente una flecha).</span><span class="sxs-lookup"><span data-stu-id="a55a4-112">Platform-dependent cursor (usually an arrow).</span></span>                                     |
| <span data-ttu-id="a55a4-113">casilla</span><span class="sxs-lookup"><span data-stu-id="a55a4-113">hand</span></span>             | <span data-ttu-id="a55a4-114">Casilla.</span><span class="sxs-lookup"><span data-stu-id="a55a4-114">Hand.</span></span>                                                                                      |
| <span data-ttu-id="a55a4-115">help</span><span class="sxs-lookup"><span data-stu-id="a55a4-115">help</span></span>             | <span data-ttu-id="a55a4-116">Flecha con signo de interrogación que indica que la ayuda está disponible.</span><span class="sxs-lookup"><span data-stu-id="a55a4-116">Arrow with question mark indicating Help is available.</span></span>                                     |
| <span data-ttu-id="a55a4-117">sizeall</span><span class="sxs-lookup"><span data-stu-id="a55a4-117">sizeall</span></span>          | <span data-ttu-id="a55a4-118">Flecha de cuatro puntas que señala al norte, sur, este y oeste.</span><span class="sxs-lookup"><span data-stu-id="a55a4-118">Four-pointed arrow pointing north, south, east, and west.</span></span>                                  |
| <span data-ttu-id="a55a4-119">sizenesw</span><span class="sxs-lookup"><span data-stu-id="a55a4-119">sizenesw</span></span>         | <span data-ttu-id="a55a4-120">Flecha de doble punta que apunta al noreste y al suroeste.</span><span class="sxs-lookup"><span data-stu-id="a55a4-120">Double-pointed arrow pointing northeast and southwest.</span></span>                                     |
| <span data-ttu-id="a55a4-121">tamaños de</span><span class="sxs-lookup"><span data-stu-id="a55a4-121">sizens</span></span>           | <span data-ttu-id="a55a4-122">Flecha de dos puntas que apunta al norte y al sur.</span><span class="sxs-lookup"><span data-stu-id="a55a4-122">Double-pointed arrow pointing north and south.</span></span>                                             |
| <span data-ttu-id="a55a4-123">sizenwse</span><span class="sxs-lookup"><span data-stu-id="a55a4-123">sizenwse</span></span>         | <span data-ttu-id="a55a4-124">Flecha de dos puntas que apunta al noroeste y al sudeste.</span><span class="sxs-lookup"><span data-stu-id="a55a4-124">Double-pointed arrow pointing northwest and southeast.</span></span>                                     |
| <span data-ttu-id="a55a4-125">sizewe</span><span class="sxs-lookup"><span data-stu-id="a55a4-125">sizewe</span></span>           | <span data-ttu-id="a55a4-126">Flecha de dos puntas que apunta al oeste y al este.</span><span class="sxs-lookup"><span data-stu-id="a55a4-126">Double-pointed arrow pointing west and east.</span></span>                                               |
| <span data-ttu-id="a55a4-127">flecha arriba</span><span class="sxs-lookup"><span data-stu-id="a55a4-127">uparrow</span></span>          | <span data-ttu-id="a55a4-128">Flecha vertical que señala hacia arriba.</span><span class="sxs-lookup"><span data-stu-id="a55a4-128">Vertical arrow pointing upward.</span></span>                                                            |
| <span data-ttu-id="a55a4-129">\*. ani o \* . cur</span><span class="sxs-lookup"><span data-stu-id="a55a4-129">\*.ani or \*.cur</span></span> | <span data-ttu-id="a55a4-130">Cualquier archivo. ani o. cur (debe estar en el mismo directorio que el archivo. WMS o en el archivo. WMZ)</span><span class="sxs-lookup"><span data-stu-id="a55a4-130">Any .ani or .cur file (must be in the same directory as the .wms file or in the .wmz file)</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="a55a4-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a55a4-131">Remarks</span></span>

<span data-ttu-id="a55a4-132">Si el sistema no reconoce el valor de cursor especificado, el valor del cursor permanece en el valor establecido anteriormente.</span><span class="sxs-lookup"><span data-stu-id="a55a4-132">If the system does not recognize the cursor value specified, the cursor value remains at the previously set value.</span></span>

<span data-ttu-id="a55a4-133">Las rutas de acceso de nombre de archivo de cursor se omiten, por lo que el archivo de cursor debe residir en el directorio predeterminado.</span><span class="sxs-lookup"><span data-stu-id="a55a4-133">Cursor file name paths are ignored, so the cursor file must reside in the default directory.</span></span>

## <a name="requirements"></a><span data-ttu-id="a55a4-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a55a4-134">Requirements</span></span>



| <span data-ttu-id="a55a4-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="a55a4-135">Requirement</span></span> | <span data-ttu-id="a55a4-136">Value</span><span class="sxs-lookup"><span data-stu-id="a55a4-136">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="a55a4-137">Versión</span><span class="sxs-lookup"><span data-stu-id="a55a4-137">Version</span></span><br/> | <span data-ttu-id="a55a4-138">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="a55a4-138">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a55a4-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="a55a4-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a55a4-140">**Elemento BUTTON**</span><span class="sxs-lookup"><span data-stu-id="a55a4-140">**BUTTON Element**</span></span>](button-element.md)
</dt> </dl>

 

 





