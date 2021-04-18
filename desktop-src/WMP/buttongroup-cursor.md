---
title: BUTTONGROUP. cursor
description: El atributo cursor especifica o recupera el tipo de cursor que aparece cuando el mouse está encima de un botón en BUTTONGROUP.
ms.assetid: c1b7e3e1-862b-48c1-bd2d-d9abd9ada14c
keywords:
- BUTTONGROUP. cursor Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONGROUP.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7b3de12950aed383f48dcde5d8978724037f86e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699798"
---
# <a name="buttongroupcursor"></a><span data-ttu-id="c4898-104">BUTTONGROUP. cursor</span><span class="sxs-lookup"><span data-stu-id="c4898-104">BUTTONGROUP.cursor</span></span>

<span data-ttu-id="c4898-105">El atributo **cursor** especifica o recupera el tipo de cursor que aparece cuando el mouse está encima de un botón en **BUTTONGROUP**.</span><span class="sxs-lookup"><span data-stu-id="c4898-105">The **cursor** attribute specifies or retrieves the type of cursor that appears when the mouse is over a button in the **BUTTONGROUP**.</span></span>

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a><span data-ttu-id="c4898-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="c4898-106">Possible Values</span></span>

<span data-ttu-id="c4898-107">Este atributo es una **cadena** de lectura/escritura que contiene uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="c4898-107">This attribute is a read/write **String** containing one of the following values.</span></span>



| <span data-ttu-id="c4898-108">Value</span><span class="sxs-lookup"><span data-stu-id="c4898-108">Value</span></span>            | <span data-ttu-id="c4898-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="c4898-109">Description</span></span>                                                                                 |
|------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4898-110">sistema</span><span class="sxs-lookup"><span data-stu-id="c4898-110">system</span></span>           | <span data-ttu-id="c4898-111">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="c4898-111">Default.</span></span> <span data-ttu-id="c4898-112">Cursor dependiente de la plataforma (normalmente una flecha).</span><span class="sxs-lookup"><span data-stu-id="c4898-112">Platform-dependent cursor (usually an arrow).</span></span>                                      |
| <span data-ttu-id="c4898-113">casilla</span><span class="sxs-lookup"><span data-stu-id="c4898-113">hand</span></span>             | <span data-ttu-id="c4898-114">Casilla.</span><span class="sxs-lookup"><span data-stu-id="c4898-114">Hand.</span></span>                                                                                       |
| <span data-ttu-id="c4898-115">help</span><span class="sxs-lookup"><span data-stu-id="c4898-115">help</span></span>             | <span data-ttu-id="c4898-116">Flecha con signo de interrogación que indica que la ayuda está disponible.</span><span class="sxs-lookup"><span data-stu-id="c4898-116">Arrow with question mark indicating Help is available.</span></span>                                      |
| <span data-ttu-id="c4898-117">sizeall</span><span class="sxs-lookup"><span data-stu-id="c4898-117">sizeall</span></span>          | <span data-ttu-id="c4898-118">Flecha de cuatro puntas que señala al norte, sur, este y oeste.</span><span class="sxs-lookup"><span data-stu-id="c4898-118">Four-pointed arrow pointing north, south, east, and west.</span></span>                                   |
| <span data-ttu-id="c4898-119">sizenesw</span><span class="sxs-lookup"><span data-stu-id="c4898-119">sizenesw</span></span>         | <span data-ttu-id="c4898-120">Flecha de doble punta que apunta al noreste y al suroeste.</span><span class="sxs-lookup"><span data-stu-id="c4898-120">Double-pointed arrow pointing northeast and southwest.</span></span>                                      |
| <span data-ttu-id="c4898-121">tamaños de</span><span class="sxs-lookup"><span data-stu-id="c4898-121">sizens</span></span>           | <span data-ttu-id="c4898-122">Flecha de dos puntas que apunta al norte y al sur.</span><span class="sxs-lookup"><span data-stu-id="c4898-122">Double-pointed arrow pointing north and south.</span></span>                                              |
| <span data-ttu-id="c4898-123">sizenwse</span><span class="sxs-lookup"><span data-stu-id="c4898-123">sizenwse</span></span>         | <span data-ttu-id="c4898-124">Flecha de dos puntas que apunta al noroeste y al sudeste.</span><span class="sxs-lookup"><span data-stu-id="c4898-124">Double-pointed arrow pointing northwest and southeast.</span></span>                                      |
| <span data-ttu-id="c4898-125">sizewe</span><span class="sxs-lookup"><span data-stu-id="c4898-125">sizewe</span></span>           | <span data-ttu-id="c4898-126">Flecha de dos puntas que apunta al oeste y al este.</span><span class="sxs-lookup"><span data-stu-id="c4898-126">Double-pointed arrow pointing west and east.</span></span>                                                |
| <span data-ttu-id="c4898-127">flecha arriba</span><span class="sxs-lookup"><span data-stu-id="c4898-127">uparrow</span></span>          | <span data-ttu-id="c4898-128">Flecha vertical que señala hacia arriba.</span><span class="sxs-lookup"><span data-stu-id="c4898-128">Vertical arrow pointing upward.</span></span>                                                             |
| <span data-ttu-id="c4898-129">\*. ani o \* . cur</span><span class="sxs-lookup"><span data-stu-id="c4898-129">\*.ani or \*.cur</span></span> | <span data-ttu-id="c4898-130">Cualquier archivo. ani o. cur (debe estar en el mismo directorio que el archivo. WMS o en el archivo. WMZ).</span><span class="sxs-lookup"><span data-stu-id="c4898-130">Any .ani or .cur file (must be in the same directory as the .wms file or in the .wmz file).</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="c4898-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c4898-131">Remarks</span></span>

<span data-ttu-id="c4898-132">El cursor especificado se aplica a todos los botones de **BUTTONGROUP**.</span><span class="sxs-lookup"><span data-stu-id="c4898-132">The cursor specified applies to all buttons in the **BUTTONGROUP**.</span></span>

<span data-ttu-id="c4898-133">Si especifica un valor de cursor no válido, permanece en el valor establecido anteriormente.</span><span class="sxs-lookup"><span data-stu-id="c4898-133">If you specify an invalid cursor value, it remains at the previously set value.</span></span>

<span data-ttu-id="c4898-134">Las rutas de acceso de nombre de archivo de cursor se omiten, por lo que el archivo de cursor debe residir en el directorio predeterminado.</span><span class="sxs-lookup"><span data-stu-id="c4898-134">Cursor file name paths are ignored, so the cursor file must reside in the default directory.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4898-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c4898-135">Requirements</span></span>



| <span data-ttu-id="c4898-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4898-136">Requirement</span></span> | <span data-ttu-id="c4898-137">Value</span><span class="sxs-lookup"><span data-stu-id="c4898-137">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="c4898-138">Versión</span><span class="sxs-lookup"><span data-stu-id="c4898-138">Version</span></span><br/> | <span data-ttu-id="c4898-139">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="c4898-139">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c4898-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="c4898-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4898-141">**Elemento BUTTONGROUP**</span><span class="sxs-lookup"><span data-stu-id="c4898-141">**BUTTONGROUP Element**</span></span>](buttongroup-element.md)
</dt> </dl>

 

 





