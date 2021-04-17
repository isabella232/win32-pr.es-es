---
title: Control deslizante. cursor
description: El atributo cursor especifica o recupera un valor que indica qué cursor aparece cuando el mouse está encima del control deslizante.
ms.assetid: 5b96a20c-b3a6-4e08-95b2-32937bb15cc6
keywords:
- Control deslizante. cursor Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cbc8f581d7d087545e666565dd03f649112064d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660217"
---
# <a name="slidercursor"></a><span data-ttu-id="8c0c1-104">Control deslizante. cursor</span><span class="sxs-lookup"><span data-stu-id="8c0c1-104">SLIDER.cursor</span></span>

<span data-ttu-id="8c0c1-105">El atributo **cursor** especifica o recupera un valor que indica qué cursor aparece cuando el mouse está encima del control deslizante.</span><span class="sxs-lookup"><span data-stu-id="8c0c1-105">The **cursor** attribute specifies or retrieves a value indicating which cursor appears when the mouse is over the slider control.</span></span>

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a><span data-ttu-id="8c0c1-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="8c0c1-106">Possible Values</span></span>

<span data-ttu-id="8c0c1-107">Este atributo es una **cadena** de lectura/escritura.</span><span class="sxs-lookup"><span data-stu-id="8c0c1-107">This attribute is a read/write **String**.</span></span>



| <span data-ttu-id="8c0c1-108">Value</span><span class="sxs-lookup"><span data-stu-id="8c0c1-108">Value</span></span>            | <span data-ttu-id="8c0c1-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="8c0c1-109">Description</span></span>                                                                                 |
|------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c0c1-110">sistema</span><span class="sxs-lookup"><span data-stu-id="8c0c1-110">system</span></span>           | <span data-ttu-id="8c0c1-111">Cursor dependiente de la plataforma (normalmente una flecha).</span><span class="sxs-lookup"><span data-stu-id="8c0c1-111">Platform-dependent cursor (usually an arrow).</span></span>                                               |
| <span data-ttu-id="8c0c1-112">casilla</span><span class="sxs-lookup"><span data-stu-id="8c0c1-112">hand</span></span>             | <span data-ttu-id="8c0c1-113">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="8c0c1-113">Default.</span></span> <span data-ttu-id="8c0c1-114">Casilla.</span><span class="sxs-lookup"><span data-stu-id="8c0c1-114">Hand.</span></span>                                                                              |
| <span data-ttu-id="8c0c1-115">help</span><span class="sxs-lookup"><span data-stu-id="8c0c1-115">help</span></span>             | <span data-ttu-id="8c0c1-116">Flecha con signo de interrogación que indica que la ayuda está disponible.</span><span class="sxs-lookup"><span data-stu-id="8c0c1-116">Arrow with question mark indicating Help is available.</span></span>                                      |
| <span data-ttu-id="8c0c1-117">sizeall</span><span class="sxs-lookup"><span data-stu-id="8c0c1-117">sizeall</span></span>          | <span data-ttu-id="8c0c1-118">Flecha de cuatro puntas que señala al norte, sur, este y oeste.</span><span class="sxs-lookup"><span data-stu-id="8c0c1-118">Four-pointed arrow pointing north, south, east, and west.</span></span>                                   |
| <span data-ttu-id="8c0c1-119">sizenesw</span><span class="sxs-lookup"><span data-stu-id="8c0c1-119">sizenesw</span></span>         | <span data-ttu-id="8c0c1-120">Flecha de doble punta que apunta al noreste y al suroeste.</span><span class="sxs-lookup"><span data-stu-id="8c0c1-120">Double-pointed arrow pointing northeast and southwest.</span></span>                                      |
| <span data-ttu-id="8c0c1-121">tamaños de</span><span class="sxs-lookup"><span data-stu-id="8c0c1-121">sizens</span></span>           | <span data-ttu-id="8c0c1-122">Flecha de dos puntas que apunta al norte y al sur.</span><span class="sxs-lookup"><span data-stu-id="8c0c1-122">Double-pointed arrow pointing north and south.</span></span>                                              |
| <span data-ttu-id="8c0c1-123">sizenwse</span><span class="sxs-lookup"><span data-stu-id="8c0c1-123">sizenwse</span></span>         | <span data-ttu-id="8c0c1-124">Flecha de dos puntas que apunta al noroeste y al sudeste.</span><span class="sxs-lookup"><span data-stu-id="8c0c1-124">Double-pointed arrow pointing northwest and southeast.</span></span>                                      |
| <span data-ttu-id="8c0c1-125">sizewe</span><span class="sxs-lookup"><span data-stu-id="8c0c1-125">sizewe</span></span>           | <span data-ttu-id="8c0c1-126">Flecha de dos puntas que apunta al oeste y al este.</span><span class="sxs-lookup"><span data-stu-id="8c0c1-126">Double-pointed arrow pointing west and east.</span></span>                                                |
| <span data-ttu-id="8c0c1-127">flecha arriba</span><span class="sxs-lookup"><span data-stu-id="8c0c1-127">uparrow</span></span>          | <span data-ttu-id="8c0c1-128">Flecha vertical que señala hacia arriba.</span><span class="sxs-lookup"><span data-stu-id="8c0c1-128">Vertical arrow pointing upward.</span></span>                                                             |
| <span data-ttu-id="8c0c1-129">\*. ani o \* . cur</span><span class="sxs-lookup"><span data-stu-id="8c0c1-129">\*.ani or \*.cur</span></span> | <span data-ttu-id="8c0c1-130">Cualquier archivo. ani o. cur (debe estar en el mismo directorio que el archivo. WMS o en el archivo. WMZ).</span><span class="sxs-lookup"><span data-stu-id="8c0c1-130">Any .ani or .cur file (must be in the same directory as the .wms file or in the .wmz file).</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="8c0c1-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c0c1-131">Requirements</span></span>



| <span data-ttu-id="8c0c1-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c0c1-132">Requirement</span></span> | <span data-ttu-id="8c0c1-133">Value</span><span class="sxs-lookup"><span data-stu-id="8c0c1-133">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="8c0c1-134">Versión</span><span class="sxs-lookup"><span data-stu-id="8c0c1-134">Version</span></span><br/> | <span data-ttu-id="8c0c1-135">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="8c0c1-135">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8c0c1-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="8c0c1-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c0c1-137">**Elemento SLIDEr**</span><span class="sxs-lookup"><span data-stu-id="8c0c1-137">**SLIDER Element**</span></span>](slider-element.md)
</dt> </dl>

 

 





