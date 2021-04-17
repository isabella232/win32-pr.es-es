---
title: EQUALIZERSETTINGS. encadenado
description: El atributo encadenado especifica o recupera un valor que indica si está habilitado el fundido cruzado.
ms.assetid: 6c5a31f3-982e-4660-80ff-30b7a4290a15
keywords:
- EQUALIZERSETTINGS. encadenado de Windows Media Player
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.crossFade
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0472f90f94b5c4ba56948848476b6585502427c7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700306"
---
# <a name="equalizersettingscrossfade"></a><span data-ttu-id="b806f-104">EQUALIZERSETTINGS. encadenado</span><span class="sxs-lookup"><span data-stu-id="b806f-104">EQUALIZERSETTINGS.crossFade</span></span>

<span data-ttu-id="b806f-105">El atributo **encadenado** especifica o recupera un valor que indica si está habilitado el fundido cruzado.</span><span class="sxs-lookup"><span data-stu-id="b806f-105">The **crossFade** attribute specifies or retrieves a value indicating whether cross-fade is enabled.</span></span>

``` syntax
        elementID.crossFade
```

## <a name="possible-values"></a><span data-ttu-id="b806f-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="b806f-106">Possible Values</span></span>

<span data-ttu-id="b806f-107">Este atributo es un **valor booleano** de lectura/escritura.</span><span class="sxs-lookup"><span data-stu-id="b806f-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="b806f-108">Value</span><span class="sxs-lookup"><span data-stu-id="b806f-108">Value</span></span> | <span data-ttu-id="b806f-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="b806f-109">Description</span></span>                      |
|-------|----------------------------------|
| <span data-ttu-id="b806f-110">true</span><span class="sxs-lookup"><span data-stu-id="b806f-110">true</span></span>  | <span data-ttu-id="b806f-111">La transición transversal está habilitada.</span><span class="sxs-lookup"><span data-stu-id="b806f-111">Cross-fade is enabled.</span></span>           |
| <span data-ttu-id="b806f-112">false</span><span class="sxs-lookup"><span data-stu-id="b806f-112">false</span></span> | <span data-ttu-id="b806f-113">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="b806f-113">Default.</span></span> <span data-ttu-id="b806f-114">La transición transversal está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="b806f-114">Cross-fade is disabled.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="b806f-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b806f-115">Remarks</span></span>

<span data-ttu-id="b806f-116">El fundido cruzado es una característica de procesamiento de audio que reduce gradualmente el volumen de un elemento multimedia cerca del final de la reproducción, al mismo tiempo que inicia la reproducción del siguiente elemento multimedia en el volumen mínimo y lo incrementa gradualmente al volumen normal.</span><span class="sxs-lookup"><span data-stu-id="b806f-116">Cross-fade is an audio processing feature that gradually decreases the volume of one media item near the end of its playback while simultaneously starting playback of the next media item at minimum volume and gradually increasing it to normal volume.</span></span> <span data-ttu-id="b806f-117">El atributo **crossFadeWindow** especifica la superposición entre el inicio del segundo elemento multimedia y el final del primer elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="b806f-117">The overlap between the start of the second media item and the end of the first media item is specified by the **crossFadeWindow** attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="b806f-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b806f-118">Requirements</span></span>



| <span data-ttu-id="b806f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b806f-119">Requirement</span></span> | <span data-ttu-id="b806f-120">Value</span><span class="sxs-lookup"><span data-stu-id="b806f-120">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="b806f-121">Versión</span><span class="sxs-lookup"><span data-stu-id="b806f-121">Version</span></span><br/> | <span data-ttu-id="b806f-122">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="b806f-122">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b806f-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="b806f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b806f-124">**Elemento EQUALIZERSETTINGS**</span><span class="sxs-lookup"><span data-stu-id="b806f-124">**EQUALIZERSETTINGS Element**</span></span>](equalizersettings-element.md)
</dt> <dt>

[<span data-ttu-id="b806f-125">**EQUALIZERSETTINGS.crossFadeWindow**</span><span class="sxs-lookup"><span data-stu-id="b806f-125">**EQUALIZERSETTINGS.crossFadeWindow**</span></span>](equalizersettings-crossfadewindow.md)
</dt> </dl>

 

 





