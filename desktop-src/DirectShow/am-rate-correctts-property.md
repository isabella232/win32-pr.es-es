---
description: El navegador de DVD usa esta propiedad para informar al descodificador de que el navegador está estableciendo las marcas de tiempo correctas en los ejemplos que entrega al descodificador.
ms.assetid: f04e8291-734f-483e-b756-5362beb68d9c
title: AM_RATE_CorrectTS propiedad (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15c65b613f892708dc210af2ca2a05efb74785fb
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910303"
---
# <a name="am_rate_correctts-property"></a><span data-ttu-id="e44e8-103">Propiedad AM \_ RATE \_ CorrectTS</span><span class="sxs-lookup"><span data-stu-id="e44e8-103">AM\_RATE\_CorrectTS Property</span></span>

<span data-ttu-id="e44e8-104">El navegador de DVD usa esta propiedad para informar al descodificador de que el navegador está estableciendo las marcas de tiempo correctas en los ejemplos que entrega al descodificador.</span><span class="sxs-lookup"><span data-stu-id="e44e8-104">The DVD Navigator uses this property to inform the decoder that the Navigator is setting the correct time stamps on the samples it delivers to the decoder.</span></span>



| <span data-ttu-id="e44e8-105">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="e44e8-105">Label</span></span> | <span data-ttu-id="e44e8-106">Value</span><span class="sxs-lookup"><span data-stu-id="e44e8-106">Value</span></span> |
|-------------------|-------------------------------|
| <span data-ttu-id="e44e8-107">GUID del conjunto de propiedades</span><span class="sxs-lookup"><span data-stu-id="e44e8-107">Property Set GUID</span></span> | <span data-ttu-id="e44e8-108">AM \_ KSPROPSETID \_ TSRateChange</span><span class="sxs-lookup"><span data-stu-id="e44e8-108">AM\_KSPROPSETID\_TSRateChange</span></span> |
| <span data-ttu-id="e44e8-109">Id. de propiedad</span><span class="sxs-lookup"><span data-stu-id="e44e8-109">Property ID</span></span>       | <span data-ttu-id="e44e8-110">AM \_ RATE \_ CorrectTS</span><span class="sxs-lookup"><span data-stu-id="e44e8-110">AM\_RATE\_CorrectTS</span></span>           |
| <span data-ttu-id="e44e8-111">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="e44e8-111">Data Type</span></span>         | <span data-ttu-id="e44e8-112">**LONG**</span><span class="sxs-lookup"><span data-stu-id="e44e8-112">**LONG**</span></span>                      |



 

## <a name="remarks"></a><span data-ttu-id="e44e8-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e44e8-113">Remarks</span></span>

<span data-ttu-id="e44e8-114">Las versiones anteriores del navegador de DVD no establecen las marcas de tiempo correctas cuando la velocidad de reproducción era distinta de la 1.0.</span><span class="sxs-lookup"><span data-stu-id="e44e8-114">Earlier versions of the DVD Navigator did not set the correct time stamps when the playback rate was something other than 1.0.</span></span> <span data-ttu-id="e44e8-115">Muchos descodificadores funcionan para solucionar este problema omitiendo las marcas de tiempo durante el rebobinado o el avance rápido, y calculando los tiempos de presentación correctos.</span><span class="sxs-lookup"><span data-stu-id="e44e8-115">Many decoders work around this problem by ignoring the time stamps during rewind or fast forward, and estimating the correct presentation times.</span></span>

<span data-ttu-id="e44e8-116">Estos problemas se han corregido en la versión actual del navegador de DVD.</span><span class="sxs-lookup"><span data-stu-id="e44e8-116">These problems have been corrected in the current version of the DVD Navigator.</span></span> <span data-ttu-id="e44e8-117">Para la compatibilidad con versiones anteriores con los descodificadores existentes, el navegador de DVD indica que las marcas de tiempo son correctas estableciendo la propiedad AM RATE CorrectTS en el descodificador con el \_ \_ valor **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="e44e8-117">For backward compatibility with existing decoders, the DVD Navigator indicates that the time stamps are correct by setting the AM\_RATE\_CorrectTS property on the decoder with the value **TRUE**.</span></span> <span data-ttu-id="e44e8-118">Cuando se establece esta propiedad, el descodificador debe usar las marcas de tiempo reales, en lugar de calcular los tiempos de presentación.</span><span class="sxs-lookup"><span data-stu-id="e44e8-118">When this property is set, the decoder should use the actual time stamps, instead of estimating the presentation times.</span></span>

## <a name="requirements"></a><span data-ttu-id="e44e8-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e44e8-119">Requirements</span></span>



| <span data-ttu-id="e44e8-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e44e8-120">Requirement</span></span> | <span data-ttu-id="e44e8-121">Value</span><span class="sxs-lookup"><span data-stu-id="e44e8-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e44e8-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e44e8-122">Header</span></span><br/> | <dl> <span data-ttu-id="e44e8-123"><dt>Dvdmedia.h</dt></span><span class="sxs-lookup"><span data-stu-id="e44e8-123"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e44e8-124">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e44e8-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e44e8-125">**Conjunto de propiedades de cambio de velocidad**</span><span class="sxs-lookup"><span data-stu-id="e44e8-125">**Rate Change Property Set**</span></span>](rate-change-property-set.md)
</dt> </dl>

 

 




