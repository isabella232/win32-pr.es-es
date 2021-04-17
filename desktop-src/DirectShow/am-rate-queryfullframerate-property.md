---
description: Esta propiedad consulta el descodificador para la velocidad máxima de fotogramas completa que admite el descodificador. El tipo de datos de esta propiedad es una \_ estructura AM QueryRate.
ms.assetid: 98808ed4-6d34-437b-9729-9cc805bc81f0
title: Propiedad AM_RATE_QueryFullFrameRate (dvdmedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab2c99564caa09253198b101a3e2467ec88c7e34
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690631"
---
# <a name="am_rate_queryfullframerate-property"></a><span data-ttu-id="e6e16-104">\_Propiedad QueryFullFrameRate de tasa AM \_</span><span class="sxs-lookup"><span data-stu-id="e6e16-104">AM\_RATE\_QueryFullFrameRate Property</span></span>

<span data-ttu-id="e6e16-105">Esta propiedad consulta el descodificador para la velocidad máxima de fotogramas completa que admite el descodificador.</span><span class="sxs-lookup"><span data-stu-id="e6e16-105">This property queries the decoder for the maximum full-frame rate that the decoder supports.</span></span> <span data-ttu-id="e6e16-106">El tipo de datos de esta propiedad es una estructura **AM \_ QueryRate** .</span><span class="sxs-lookup"><span data-stu-id="e6e16-106">The data type for this property is an **AM\_QueryRate** structure.</span></span>

<span data-ttu-id="e6e16-107">Esta propiedad se define para la versión 1,1 de este conjunto de propiedades; vea [**\_ tasa AM \_ UseRateVersion**](am-rate-userateversion-property.md).</span><span class="sxs-lookup"><span data-stu-id="e6e16-107">This property is defined for version 1.1 of this property set; see [**AM\_RATE\_UseRateVersion**](am-rate-userateversion-property.md).</span></span>



|                   |                                       |
|-------------------|---------------------------------------|
| <span data-ttu-id="e6e16-108">GUID del conjunto de propiedades</span><span class="sxs-lookup"><span data-stu-id="e6e16-108">Property Set GUID</span></span> | <span data-ttu-id="e6e16-109">\_TSRateChange KSPROPSETID \_ AM</span><span class="sxs-lookup"><span data-stu-id="e6e16-109">AM\_KSPROPSETID\_TSRateChange</span></span>         |
| <span data-ttu-id="e6e16-110">Id. de propiedad</span><span class="sxs-lookup"><span data-stu-id="e6e16-110">Property ID</span></span>       | <span data-ttu-id="e6e16-111">\_Propiedad QueryFullFrameRate de tasa AM \_</span><span class="sxs-lookup"><span data-stu-id="e6e16-111">AM\_RATE\_QueryFullFrameRate Property</span></span> |
| <span data-ttu-id="e6e16-112">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="e6e16-112">Data Type</span></span>         | [<span data-ttu-id="e6e16-113">**\_QUERYRATE AM**</span><span class="sxs-lookup"><span data-stu-id="e6e16-113">**AM\_QueryRate**</span></span>](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_queryrate) |



 

## <a name="remarks"></a><span data-ttu-id="e6e16-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e6e16-114">Remarks</span></span>

<span data-ttu-id="e6e16-115">Si la velocidad de reproducción supera la tasa máxima del descodificador, el filtro de origen envía grupos de muestras continuas separadas por discontinuidades.</span><span class="sxs-lookup"><span data-stu-id="e6e16-115">If the playback rate exceeds the decoder's maximum rate, the source filter sends groups of continuous samples separated by discontinuities.</span></span> <span data-ttu-id="e6e16-116">Las marcas de tiempo saltan entre las discontinuidades.</span><span class="sxs-lookup"><span data-stu-id="e6e16-116">The time stamps jump across the discontinuities.</span></span> <span data-ttu-id="e6e16-117">El filtro de origen puede hacer esto incluso si la velocidad de reproducción está dentro de la velocidad máxima del descodificador, porque puede haber otros factores, como la e/s de disco, que limitan la velocidad de reproducción completa.</span><span class="sxs-lookup"><span data-stu-id="e6e16-117">The source filter might do this even if the playback rate is within the decoder's maximum rate, because there may be other factors, such as disk IO, that limit the full playback rate.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6e16-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e6e16-118">Requirements</span></span>



| <span data-ttu-id="e6e16-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6e16-119">Requirement</span></span> | <span data-ttu-id="e6e16-120">Value</span><span class="sxs-lookup"><span data-stu-id="e6e16-120">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e6e16-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e6e16-121">Header</span></span><br/> | <dl> <span data-ttu-id="e6e16-122"><dt>Dvdmedia. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6e16-122"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6e16-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="e6e16-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6e16-124">**Conjunto de propiedades de cambio de velocidad**</span><span class="sxs-lookup"><span data-stu-id="e6e16-124">**Rate Change Property Set**</span></span>](rate-change-property-set.md)
</dt> </dl>

 

 




