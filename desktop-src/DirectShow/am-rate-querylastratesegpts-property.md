---
description: Esta propiedad consulta al descodificador la hora de inicio del cambio de velocidad que se ha puesto en cola más recientemente, independientemente de su posición en la cola de cambio de frecuencia.
ms.assetid: 3c7006e7-48fd-4df8-b446-8ee2b024278b
title: AM_RATE_QueryLastRateSegPTS propiedad (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72c6e3e00985ba6e714bf48d349fd5af5c9593b9
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910273"
---
# <a name="am_rate_querylastratesegpts-property"></a><span data-ttu-id="5505f-103">Consulta \_ AM \_ RATELastRateSegPTS Propiedad</span><span class="sxs-lookup"><span data-stu-id="5505f-103">AM\_RATE\_QueryLastRateSegPTS Property</span></span>

<span data-ttu-id="5505f-104">Esta propiedad consulta al descodificador la hora de inicio del cambio de velocidad que se ha puesto en cola más recientemente, independientemente de su posición en la cola de cambio de frecuencia.</span><span class="sxs-lookup"><span data-stu-id="5505f-104">This property queries the decoder for the start time of the rate change that was queued most recently, regardless of its position in the rate-change queue.</span></span>

<span data-ttu-id="5505f-105">Esta propiedad se define para la versión 1.1 de este conjunto de propiedades; vea [**Am \_ RATE \_ UseRateVersion**](am-rate-userateversion-property.md).</span><span class="sxs-lookup"><span data-stu-id="5505f-105">This property is defined for version 1.1 of this property set; see [**AM\_RATE\_UseRateVersion**](am-rate-userateversion-property.md).</span></span>



| <span data-ttu-id="5505f-106">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="5505f-106">Label</span></span> | <span data-ttu-id="5505f-107">Value</span><span class="sxs-lookup"><span data-stu-id="5505f-107">Value</span></span> |
|-------------------|-------------------------------|
| <span data-ttu-id="5505f-108">GUID del conjunto de propiedades</span><span class="sxs-lookup"><span data-stu-id="5505f-108">Property Set GUID</span></span> | <span data-ttu-id="5505f-109">AM \_ KSPROPSETID \_ TSRateChange</span><span class="sxs-lookup"><span data-stu-id="5505f-109">AM\_KSPROPSETID\_TSRateChange</span></span> |
| <span data-ttu-id="5505f-110">Id. de propiedad</span><span class="sxs-lookup"><span data-stu-id="5505f-110">Property ID</span></span>       | <span data-ttu-id="5505f-111">Consulta \_ AM \_ RATELastRateSegPTS</span><span class="sxs-lookup"><span data-stu-id="5505f-111">AM\_RATE\_QueryLastRateSegPTS</span></span> |
| <span data-ttu-id="5505f-112">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="5505f-112">Data Type</span></span>         | <span data-ttu-id="5505f-113">**HORA DE \_ REFERENCIA**</span><span class="sxs-lookup"><span data-stu-id="5505f-113">**REFERENCE\_TIME**</span></span>           |



 

## <a name="remarks"></a><span data-ttu-id="5505f-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5505f-114">Remarks</span></span>

<span data-ttu-id="5505f-115">El filtro de origen puede usar esta propiedad para sincronizar los cambios de velocidad en varias secuencias de audio y vídeo.</span><span class="sxs-lookup"><span data-stu-id="5505f-115">The source filter can use this property to synchronize rate changes across several audio and video streams.</span></span>

## <a name="requirements"></a><span data-ttu-id="5505f-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5505f-116">Requirements</span></span>



| <span data-ttu-id="5505f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="5505f-117">Requirement</span></span> | <span data-ttu-id="5505f-118">Value</span><span class="sxs-lookup"><span data-stu-id="5505f-118">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5505f-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5505f-119">Header</span></span><br/> | <dl> <span data-ttu-id="5505f-120"><dt>Dvdmedia.h</dt></span><span class="sxs-lookup"><span data-stu-id="5505f-120"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5505f-121">Consulte también</span><span class="sxs-lookup"><span data-stu-id="5505f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5505f-122">**Conjunto de propiedades de cambio de frecuencia**</span><span class="sxs-lookup"><span data-stu-id="5505f-122">**Rate Change Property Set**</span></span>](rate-change-property-set.md)
</dt> </dl>

 

 




