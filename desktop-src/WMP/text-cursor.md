---
title: TEXT. cursor
description: El atributo cursor especifica o recupera un valor que indica qué cursor aparece cuando el mouse está sobre el control de texto.
ms.assetid: 360d4ed1-9c4f-4210-8e77-2dfbe7573869
keywords:
- TEXT. cursor Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8cf7b135ed0a99b5c65f760a08e4e7083234674
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718649"
---
# <a name="textcursor"></a><span data-ttu-id="dad8a-104">TEXT. cursor</span><span class="sxs-lookup"><span data-stu-id="dad8a-104">TEXT.cursor</span></span>

<span data-ttu-id="dad8a-105">El atributo **cursor** especifica o recupera un valor que indica qué cursor aparece cuando el mouse está sobre el control de texto.</span><span class="sxs-lookup"><span data-stu-id="dad8a-105">The **cursor** attribute specifies or retrieves a value indicating which cursor appears when the mouse is over the Text control.</span></span>

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a><span data-ttu-id="dad8a-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="dad8a-106">Possible Values</span></span>

<span data-ttu-id="dad8a-107">Este atributo es una **cadena** de lectura/escritura.</span><span class="sxs-lookup"><span data-stu-id="dad8a-107">This attribute is a read/write **String**.</span></span>



| <span data-ttu-id="dad8a-108">Value</span><span class="sxs-lookup"><span data-stu-id="dad8a-108">Value</span></span>            | <span data-ttu-id="dad8a-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="dad8a-109">Description</span></span>                                                                                 |
|------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="dad8a-110">sistema</span><span class="sxs-lookup"><span data-stu-id="dad8a-110">system</span></span>           | <span data-ttu-id="dad8a-111">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="dad8a-111">Default.</span></span> <span data-ttu-id="dad8a-112">Cursor dependiente de la plataforma (normalmente una flecha).</span><span class="sxs-lookup"><span data-stu-id="dad8a-112">Platform-dependent cursor (usually an arrow).</span></span>                                      |
| <span data-ttu-id="dad8a-113">casilla</span><span class="sxs-lookup"><span data-stu-id="dad8a-113">hand</span></span>             | <span data-ttu-id="dad8a-114">Casilla.</span><span class="sxs-lookup"><span data-stu-id="dad8a-114">Hand.</span></span>                                                                                       |
| <span data-ttu-id="dad8a-115">help</span><span class="sxs-lookup"><span data-stu-id="dad8a-115">help</span></span>             | <span data-ttu-id="dad8a-116">Flecha con signo de interrogación que indica que la ayuda está disponible.</span><span class="sxs-lookup"><span data-stu-id="dad8a-116">Arrow with question mark indicating Help is available.</span></span>                                      |
| <span data-ttu-id="dad8a-117">sizeall</span><span class="sxs-lookup"><span data-stu-id="dad8a-117">sizeall</span></span>          | <span data-ttu-id="dad8a-118">Flecha de cuatro puntas que señala al norte, sur, este y oeste.</span><span class="sxs-lookup"><span data-stu-id="dad8a-118">Four-pointed arrow pointing north, south, east, and west.</span></span>                                   |
| <span data-ttu-id="dad8a-119">sizenesw</span><span class="sxs-lookup"><span data-stu-id="dad8a-119">sizenesw</span></span>         | <span data-ttu-id="dad8a-120">Flecha de doble punta que apunta al noreste y al suroeste.</span><span class="sxs-lookup"><span data-stu-id="dad8a-120">Double-pointed arrow pointing northeast and southwest.</span></span>                                      |
| <span data-ttu-id="dad8a-121">tamaños de</span><span class="sxs-lookup"><span data-stu-id="dad8a-121">sizens</span></span>           | <span data-ttu-id="dad8a-122">Flecha de dos puntas que apunta al norte y al sur.</span><span class="sxs-lookup"><span data-stu-id="dad8a-122">Double-pointed arrow pointing north and south.</span></span>                                              |
| <span data-ttu-id="dad8a-123">sizenwse</span><span class="sxs-lookup"><span data-stu-id="dad8a-123">sizenwse</span></span>         | <span data-ttu-id="dad8a-124">Flecha de dos puntas que apunta al noroeste y al sudeste.</span><span class="sxs-lookup"><span data-stu-id="dad8a-124">Double-pointed arrow pointing northwest and southeast.</span></span>                                      |
| <span data-ttu-id="dad8a-125">sizewe</span><span class="sxs-lookup"><span data-stu-id="dad8a-125">sizewe</span></span>           | <span data-ttu-id="dad8a-126">Flecha de dos puntas que apunta al oeste y al este.</span><span class="sxs-lookup"><span data-stu-id="dad8a-126">Double-pointed arrow pointing west and east.</span></span>                                                |
| <span data-ttu-id="dad8a-127">flecha arriba</span><span class="sxs-lookup"><span data-stu-id="dad8a-127">uparrow</span></span>          | <span data-ttu-id="dad8a-128">Flecha vertical que señala hacia arriba.</span><span class="sxs-lookup"><span data-stu-id="dad8a-128">Vertical arrow pointing upward.</span></span>                                                             |
| <span data-ttu-id="dad8a-129">\*. ani o \* . cur</span><span class="sxs-lookup"><span data-stu-id="dad8a-129">\*.ani or \*.cur</span></span> | <span data-ttu-id="dad8a-130">Cualquier archivo. ani o. cur (debe estar en el mismo directorio que el archivo. WMS o en el archivo. WMZ).</span><span class="sxs-lookup"><span data-stu-id="dad8a-130">Any .ani or .cur file (must be in the same directory as the .wms file or in the .wmz file).</span></span> |



 

<span data-ttu-id="dad8a-131">Vea el atributo [Value](text-value.md) para ver un ejemplo que muestra cómo se utilizan los atributos del elemento de **texto** .</span><span class="sxs-lookup"><span data-stu-id="dad8a-131">See the [value](text-value.md) attribute for a sample illustrating how the attributes of the **TEXT** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="dad8a-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dad8a-132">Requirements</span></span>



| <span data-ttu-id="dad8a-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="dad8a-133">Requirement</span></span> | <span data-ttu-id="dad8a-134">Value</span><span class="sxs-lookup"><span data-stu-id="dad8a-134">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="dad8a-135">Versión</span><span class="sxs-lookup"><span data-stu-id="dad8a-135">Version</span></span><br/> | <span data-ttu-id="dad8a-136">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="dad8a-136">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="dad8a-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="dad8a-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dad8a-138">**Elemento TEXT**</span><span class="sxs-lookup"><span data-stu-id="dad8a-138">**TEXT Element**</span></span>](text-element.md)
</dt> </dl>

 

 





