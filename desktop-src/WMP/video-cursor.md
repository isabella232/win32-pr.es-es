---
title: VÍDEO. cursor
description: El atributo cursor especifica o recupera el valor del cursor que se utiliza cuando el mouse está sobre un área en la que se hace clic del vídeo.
ms.assetid: 2faaf9cd-47be-47d5-ad4e-8f3bb322d812
keywords:
- VÍDEO. cursor Windows Media Player
topic_type:
- apiref
api_name:
- VIDEO.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c23ab90b974ad5a7f9cfaf9fcc598371cd0697f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709022"
---
# <a name="videocursor"></a><span data-ttu-id="7126e-104">VÍDEO. cursor</span><span class="sxs-lookup"><span data-stu-id="7126e-104">VIDEO.cursor</span></span>

<span data-ttu-id="7126e-105">El atributo **cursor** especifica o recupera el valor del cursor que se utiliza cuando el mouse está sobre un área en la que se hace clic del vídeo.</span><span class="sxs-lookup"><span data-stu-id="7126e-105">The **cursor** attribute specifies or retrieves the cursor value that is used when the mouse is over a clickable area of the video.</span></span>

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a><span data-ttu-id="7126e-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="7126e-106">Possible Values</span></span>

<span data-ttu-id="7126e-107">Este atributo es una **cadena** de lectura/escritura.</span><span class="sxs-lookup"><span data-stu-id="7126e-107">This attribute is a read/write **String**.</span></span>



| <span data-ttu-id="7126e-108">Value</span><span class="sxs-lookup"><span data-stu-id="7126e-108">Value</span></span>            | <span data-ttu-id="7126e-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="7126e-109">Description</span></span>                                                                                 |
|------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="7126e-110">sistema</span><span class="sxs-lookup"><span data-stu-id="7126e-110">system</span></span>           | <span data-ttu-id="7126e-111">Cursor dependiente de la plataforma (normalmente una flecha).</span><span class="sxs-lookup"><span data-stu-id="7126e-111">Platform-dependent cursor (usually an arrow).</span></span>                                               |
| <span data-ttu-id="7126e-112">casilla</span><span class="sxs-lookup"><span data-stu-id="7126e-112">hand</span></span>             | <span data-ttu-id="7126e-113">Casilla.</span><span class="sxs-lookup"><span data-stu-id="7126e-113">Hand.</span></span>                                                                                       |
| <span data-ttu-id="7126e-114">help</span><span class="sxs-lookup"><span data-stu-id="7126e-114">help</span></span>             | <span data-ttu-id="7126e-115">Flecha con signo de interrogación que indica que la ayuda está disponible.</span><span class="sxs-lookup"><span data-stu-id="7126e-115">Arrow with question mark indicating Help is available.</span></span>                                      |
| <span data-ttu-id="7126e-116">sizeall</span><span class="sxs-lookup"><span data-stu-id="7126e-116">sizeall</span></span>          | <span data-ttu-id="7126e-117">Flecha de cuatro puntas que señala al norte, sur, este y oeste.</span><span class="sxs-lookup"><span data-stu-id="7126e-117">Four-pointed arrow pointing north, south, east, and west.</span></span>                                   |
| <span data-ttu-id="7126e-118">sizenesw</span><span class="sxs-lookup"><span data-stu-id="7126e-118">sizenesw</span></span>         | <span data-ttu-id="7126e-119">Flecha de doble punta que apunta al noreste y al suroeste.</span><span class="sxs-lookup"><span data-stu-id="7126e-119">Double-pointed arrow pointing northeast and southwest.</span></span>                                      |
| <span data-ttu-id="7126e-120">tamaños de</span><span class="sxs-lookup"><span data-stu-id="7126e-120">sizens</span></span>           | <span data-ttu-id="7126e-121">Flecha de dos puntas que apunta al norte y al sur.</span><span class="sxs-lookup"><span data-stu-id="7126e-121">Double-pointed arrow pointing north and south.</span></span>                                              |
| <span data-ttu-id="7126e-122">sizenwse</span><span class="sxs-lookup"><span data-stu-id="7126e-122">sizenwse</span></span>         | <span data-ttu-id="7126e-123">Flecha de dos puntas que apunta al noroeste y al sudeste.</span><span class="sxs-lookup"><span data-stu-id="7126e-123">Double-pointed arrow pointing northwest and southeast.</span></span>                                      |
| <span data-ttu-id="7126e-124">sizewe</span><span class="sxs-lookup"><span data-stu-id="7126e-124">sizewe</span></span>           | <span data-ttu-id="7126e-125">Flecha de dos puntas que apunta al oeste y al este.</span><span class="sxs-lookup"><span data-stu-id="7126e-125">Double-pointed arrow pointing west and east.</span></span>                                                |
| <span data-ttu-id="7126e-126">flecha arriba</span><span class="sxs-lookup"><span data-stu-id="7126e-126">uparrow</span></span>          | <span data-ttu-id="7126e-127">Flecha vertical que señala hacia arriba.</span><span class="sxs-lookup"><span data-stu-id="7126e-127">Vertical arrow pointing upward.</span></span>                                                             |
| <span data-ttu-id="7126e-128">\*. ani o \* . cur</span><span class="sxs-lookup"><span data-stu-id="7126e-128">\*.ani or \*.cur</span></span> | <span data-ttu-id="7126e-129">Cualquier archivo. ani o. cur (debe estar en el mismo directorio que el archivo. WMS o en el archivo. WMZ).</span><span class="sxs-lookup"><span data-stu-id="7126e-129">Any .ani or .cur file (must be in the same directory as the .wms file or in the .wmz file).</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="7126e-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7126e-130">Remarks</span></span>

<span data-ttu-id="7126e-131">Para fines de representación, el sistema es el cursor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="7126e-131">For rendering purposes, system is the default cursor.</span></span> <span data-ttu-id="7126e-132">El valor predeterminado recuperado de este atributo es "" (cadena vacía).</span><span class="sxs-lookup"><span data-stu-id="7126e-132">The default value retrieved from this attribute is "" (empty string).</span></span>

## <a name="requirements"></a><span data-ttu-id="7126e-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7126e-133">Requirements</span></span>



| <span data-ttu-id="7126e-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="7126e-134">Requirement</span></span> | <span data-ttu-id="7126e-135">Value</span><span class="sxs-lookup"><span data-stu-id="7126e-135">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="7126e-136">Versión</span><span class="sxs-lookup"><span data-stu-id="7126e-136">Version</span></span><br/> | <span data-ttu-id="7126e-137">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="7126e-137">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7126e-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="7126e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7126e-139">**Elemento de vídeo**</span><span class="sxs-lookup"><span data-stu-id="7126e-139">**VIDEO Element**</span></span>](video-element.md)
</dt> </dl>

 

 





