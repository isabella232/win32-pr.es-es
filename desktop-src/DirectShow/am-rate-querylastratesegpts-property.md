---
description: Esta propiedad consulta el descodificador para la hora de inicio del cambio de frecuencia que se puso en cola más recientemente, independientemente de su posición en la cola de cambio de velocidad.
ms.assetid: 3c7006e7-48fd-4df8-b446-8ee2b024278b
title: Propiedad AM_RATE_QueryLastRateSegPTS (dvdmedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 024ac26d8307dc9b8ff8e16603dfcc61b0704390
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660952"
---
# <a name="am_rate_querylastratesegpts-property"></a><span data-ttu-id="e83fb-103">\_Propiedad QueryLastRateSegPTS de tasa AM \_</span><span class="sxs-lookup"><span data-stu-id="e83fb-103">AM\_RATE\_QueryLastRateSegPTS Property</span></span>

<span data-ttu-id="e83fb-104">Esta propiedad consulta el descodificador para la hora de inicio del cambio de frecuencia que se puso en cola más recientemente, independientemente de su posición en la cola de cambio de velocidad.</span><span class="sxs-lookup"><span data-stu-id="e83fb-104">This property queries the decoder for the start time of the rate change that was queued most recently, regardless of its position in the rate-change queue.</span></span>

<span data-ttu-id="e83fb-105">Esta propiedad se define para la versión 1,1 de este conjunto de propiedades; vea [**\_ tasa AM \_ UseRateVersion**](am-rate-userateversion-property.md).</span><span class="sxs-lookup"><span data-stu-id="e83fb-105">This property is defined for version 1.1 of this property set; see [**AM\_RATE\_UseRateVersion**](am-rate-userateversion-property.md).</span></span>



|                   |                               |
|-------------------|-------------------------------|
| <span data-ttu-id="e83fb-106">GUID del conjunto de propiedades</span><span class="sxs-lookup"><span data-stu-id="e83fb-106">Property Set GUID</span></span> | <span data-ttu-id="e83fb-107">\_TSRateChange KSPROPSETID \_ AM</span><span class="sxs-lookup"><span data-stu-id="e83fb-107">AM\_KSPROPSETID\_TSRateChange</span></span> |
| <span data-ttu-id="e83fb-108">Id. de propiedad</span><span class="sxs-lookup"><span data-stu-id="e83fb-108">Property ID</span></span>       | <span data-ttu-id="e83fb-109">Tasa de AM \_ \_ QueryLastRateSegPTS</span><span class="sxs-lookup"><span data-stu-id="e83fb-109">AM\_RATE\_QueryLastRateSegPTS</span></span> |
| <span data-ttu-id="e83fb-110">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="e83fb-110">Data Type</span></span>         | <span data-ttu-id="e83fb-111">**tiempo de referencia \_**</span><span class="sxs-lookup"><span data-stu-id="e83fb-111">**REFERENCE\_TIME**</span></span>           |



 

## <a name="remarks"></a><span data-ttu-id="e83fb-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e83fb-112">Remarks</span></span>

<span data-ttu-id="e83fb-113">El filtro de origen puede utilizar esta propiedad para sincronizar los cambios de velocidad en varias secuencias de audio y vídeo.</span><span class="sxs-lookup"><span data-stu-id="e83fb-113">The source filter can use this property to synchronize rate changes across several audio and video streams.</span></span>

## <a name="requirements"></a><span data-ttu-id="e83fb-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e83fb-114">Requirements</span></span>



| <span data-ttu-id="e83fb-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e83fb-115">Requirement</span></span> | <span data-ttu-id="e83fb-116">Value</span><span class="sxs-lookup"><span data-stu-id="e83fb-116">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e83fb-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e83fb-117">Header</span></span><br/> | <dl> <span data-ttu-id="e83fb-118"><dt>Dvdmedia. h</dt></span><span class="sxs-lookup"><span data-stu-id="e83fb-118"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e83fb-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="e83fb-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e83fb-120">**Conjunto de propiedades de cambio de velocidad**</span><span class="sxs-lookup"><span data-stu-id="e83fb-120">**Rate Change Property Set**</span></span>](rate-change-property-set.md)
</dt> </dl>

 

 




