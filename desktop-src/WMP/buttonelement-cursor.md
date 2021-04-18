---
title: BUTTONELEMENT. cursor
description: El atributo cursor especifica o recupera el valor del cursor BUTTONELEMENT que aparece cuando el mouse está sobre BUTTONELEMENT.
ms.assetid: 29e7fadb-30d8-40e4-9a64-6b6f45eac80a
keywords:
- BUTTONELEMENT. cursor Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONELEMENT.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f267cd54c36ad8f89a7242d7f428fd0d52b75fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700383"
---
# <a name="buttonelementcursor"></a><span data-ttu-id="167ad-104">BUTTONELEMENT. cursor</span><span class="sxs-lookup"><span data-stu-id="167ad-104">BUTTONELEMENT.cursor</span></span>

<span data-ttu-id="167ad-105">El atributo **cursor** especifica o recupera el valor del cursor **BUTTONELEMENT** que aparece cuando el mouse está sobre **BUTTONELEMENT**.</span><span class="sxs-lookup"><span data-stu-id="167ad-105">The **cursor** attribute specifies or retrieves the value of the **BUTTONELEMENT** cursor that appears when the mouse is over the **BUTTONELEMENT**.</span></span>

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a><span data-ttu-id="167ad-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="167ad-106">Possible Values</span></span>

<span data-ttu-id="167ad-107">Este atributo es una **cadena** de lectura/escritura.</span><span class="sxs-lookup"><span data-stu-id="167ad-107">This attribute is a read/write **String**.</span></span>



| <span data-ttu-id="167ad-108">Value</span><span class="sxs-lookup"><span data-stu-id="167ad-108">Value</span></span>            | <span data-ttu-id="167ad-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="167ad-109">Description</span></span>                                                                                 |
|------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="167ad-110">sistema</span><span class="sxs-lookup"><span data-stu-id="167ad-110">system</span></span>           | <span data-ttu-id="167ad-111">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="167ad-111">Default.</span></span> <span data-ttu-id="167ad-112">Cursor dependiente de la plataforma (normalmente una flecha).</span><span class="sxs-lookup"><span data-stu-id="167ad-112">Platform-dependent cursor (usually an arrow).</span></span>                                      |
| <span data-ttu-id="167ad-113">casilla</span><span class="sxs-lookup"><span data-stu-id="167ad-113">hand</span></span>             | <span data-ttu-id="167ad-114">Casilla.</span><span class="sxs-lookup"><span data-stu-id="167ad-114">Hand.</span></span>                                                                                       |
| <span data-ttu-id="167ad-115">help</span><span class="sxs-lookup"><span data-stu-id="167ad-115">help</span></span>             | <span data-ttu-id="167ad-116">Flecha con signo de interrogación que indica que la ayuda está disponible.</span><span class="sxs-lookup"><span data-stu-id="167ad-116">Arrow with question mark indicating Help is available.</span></span>                                      |
| <span data-ttu-id="167ad-117">sizeall</span><span class="sxs-lookup"><span data-stu-id="167ad-117">sizeall</span></span>          | <span data-ttu-id="167ad-118">Flecha de cuatro puntas que señala al norte, sur, este y oeste.</span><span class="sxs-lookup"><span data-stu-id="167ad-118">Four-pointed arrow pointing north, south, east, and west.</span></span>                                   |
| <span data-ttu-id="167ad-119">sizenesw</span><span class="sxs-lookup"><span data-stu-id="167ad-119">sizenesw</span></span>         | <span data-ttu-id="167ad-120">Flecha de doble punta que apunta al noreste y al suroeste.</span><span class="sxs-lookup"><span data-stu-id="167ad-120">Double-pointed arrow pointing northeast and southwest.</span></span>                                      |
| <span data-ttu-id="167ad-121">tamaños de</span><span class="sxs-lookup"><span data-stu-id="167ad-121">sizens</span></span>           | <span data-ttu-id="167ad-122">Flecha de dos puntas que apunta al norte y al sur.</span><span class="sxs-lookup"><span data-stu-id="167ad-122">Double-pointed arrow pointing north and south.</span></span>                                              |
| <span data-ttu-id="167ad-123">sizenwse</span><span class="sxs-lookup"><span data-stu-id="167ad-123">sizenwse</span></span>         | <span data-ttu-id="167ad-124">Flecha de dos puntas que apunta al noroeste y al sudeste.</span><span class="sxs-lookup"><span data-stu-id="167ad-124">Double-pointed arrow pointing northwest and southeast.</span></span>                                      |
| <span data-ttu-id="167ad-125">sizewe</span><span class="sxs-lookup"><span data-stu-id="167ad-125">sizewe</span></span>           | <span data-ttu-id="167ad-126">Flecha de dos puntas que apunta al oeste y al este.</span><span class="sxs-lookup"><span data-stu-id="167ad-126">Double-pointed arrow pointing west and east.</span></span>                                                |
| <span data-ttu-id="167ad-127">flecha arriba</span><span class="sxs-lookup"><span data-stu-id="167ad-127">uparrow</span></span>          | <span data-ttu-id="167ad-128">Flecha vertical que señala hacia arriba.</span><span class="sxs-lookup"><span data-stu-id="167ad-128">Vertical arrow pointing upward.</span></span>                                                             |
| <span data-ttu-id="167ad-129">\*. ani o \* . cur</span><span class="sxs-lookup"><span data-stu-id="167ad-129">\*.ani or \*.cur</span></span> | <span data-ttu-id="167ad-130">Cualquier archivo. ani o. cur (debe estar en el mismo directorio que el archivo. WMS o en el archivo. WMZ).</span><span class="sxs-lookup"><span data-stu-id="167ad-130">Any .ani or .cur file (must be in the same directory as the .wms file or in the .wmz file).</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="167ad-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="167ad-131">Remarks</span></span>

<span data-ttu-id="167ad-132">Si se especifica un valor no válido, se mantiene el valor anterior.</span><span class="sxs-lookup"><span data-stu-id="167ad-132">If an invalid value is specified, the previous value is maintained.</span></span>

<span data-ttu-id="167ad-133">Las rutas de acceso de nombre de archivo de cursor se omiten, por lo que el archivo de cursor debe residir en el directorio predeterminado.</span><span class="sxs-lookup"><span data-stu-id="167ad-133">Cursor file name paths are ignored, so the cursor file must reside in the default directory.</span></span>

## <a name="requirements"></a><span data-ttu-id="167ad-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="167ad-134">Requirements</span></span>



| <span data-ttu-id="167ad-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="167ad-135">Requirement</span></span> | <span data-ttu-id="167ad-136">Value</span><span class="sxs-lookup"><span data-stu-id="167ad-136">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="167ad-137">Versión</span><span class="sxs-lookup"><span data-stu-id="167ad-137">Version</span></span><br/> | <span data-ttu-id="167ad-138">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="167ad-138">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="167ad-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="167ad-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="167ad-140">**BUTTONELEMENT (elemento)**</span><span class="sxs-lookup"><span data-stu-id="167ad-140">**BUTTONELEMENT Element**</span></span>](buttonelement-element.md)
</dt> </dl>

 

 





