---
description: Esta propiedad consulta al descodificador la velocidad máxima de fotogramas completos que admite el descodificador. El tipo de datos de esta propiedad es una estructura \_ QueryRate de AM.
ms.assetid: 98808ed4-6d34-437b-9729-9cc805bc81f0
title: AM_RATE_QueryFullFrameRate propiedad (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70bc096e5b68737ca877a037571223d673284dab
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910283"
---
# <a name="am_rate_queryfullframerate-property"></a><span data-ttu-id="9b509-104">Propiedad \_ \_ QueryFullFrameRate de AM RATE</span><span class="sxs-lookup"><span data-stu-id="9b509-104">AM\_RATE\_QueryFullFrameRate Property</span></span>

<span data-ttu-id="9b509-105">Esta propiedad consulta al descodificador la velocidad máxima de fotogramas completos que admite el descodificador.</span><span class="sxs-lookup"><span data-stu-id="9b509-105">This property queries the decoder for the maximum full-frame rate that the decoder supports.</span></span> <span data-ttu-id="9b509-106">El tipo de datos de esta propiedad es una **estructura \_ QueryRate de AM.**</span><span class="sxs-lookup"><span data-stu-id="9b509-106">The data type for this property is an **AM\_QueryRate** structure.</span></span>

<span data-ttu-id="9b509-107">Esta propiedad se define para la versión 1.1 de este conjunto de propiedades; vea [**Am \_ RATE \_ UseRateVersion**](am-rate-userateversion-property.md).</span><span class="sxs-lookup"><span data-stu-id="9b509-107">This property is defined for version 1.1 of this property set; see [**AM\_RATE\_UseRateVersion**](am-rate-userateversion-property.md).</span></span>



| <span data-ttu-id="9b509-108">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="9b509-108">Label</span></span> | <span data-ttu-id="9b509-109">Value</span><span class="sxs-lookup"><span data-stu-id="9b509-109">Value</span></span> |
|-------------------|---------------------------------------|
| <span data-ttu-id="9b509-110">GUID del conjunto de propiedades</span><span class="sxs-lookup"><span data-stu-id="9b509-110">Property Set GUID</span></span> | <span data-ttu-id="9b509-111">AM \_ KSPROPSETID \_ TSRateChange</span><span class="sxs-lookup"><span data-stu-id="9b509-111">AM\_KSPROPSETID\_TSRateChange</span></span>         |
| <span data-ttu-id="9b509-112">Id. de propiedad</span><span class="sxs-lookup"><span data-stu-id="9b509-112">Property ID</span></span>       | <span data-ttu-id="9b509-113">Propiedad \_ \_ QueryFullFrameRate de AM RATE</span><span class="sxs-lookup"><span data-stu-id="9b509-113">AM\_RATE\_QueryFullFrameRate Property</span></span> |
| <span data-ttu-id="9b509-114">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="9b509-114">Data Type</span></span>         | [<span data-ttu-id="9b509-115">**Velocidad de consulta de AM \_**</span><span class="sxs-lookup"><span data-stu-id="9b509-115">**AM\_QueryRate**</span></span>](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_queryrate) |



 

## <a name="remarks"></a><span data-ttu-id="9b509-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9b509-116">Remarks</span></span>

<span data-ttu-id="9b509-117">Si la velocidad de reproducción supera la velocidad máxima del descodificador, el filtro de origen envía grupos de muestras continuas separadas por discontinuidades.</span><span class="sxs-lookup"><span data-stu-id="9b509-117">If the playback rate exceeds the decoder's maximum rate, the source filter sends groups of continuous samples separated by discontinuities.</span></span> <span data-ttu-id="9b509-118">Las marcas de tiempo saltan entre las discontinuidades.</span><span class="sxs-lookup"><span data-stu-id="9b509-118">The time stamps jump across the discontinuities.</span></span> <span data-ttu-id="9b509-119">El filtro de origen podría hacer esto incluso si la velocidad de reproducción está dentro de la velocidad máxima del descodificador, ya que puede haber otros factores, como la E/S de disco, que limiten la velocidad de reproducción completa.</span><span class="sxs-lookup"><span data-stu-id="9b509-119">The source filter might do this even if the playback rate is within the decoder's maximum rate, because there may be other factors, such as disk IO, that limit the full playback rate.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b509-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9b509-120">Requirements</span></span>



| <span data-ttu-id="9b509-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b509-121">Requirement</span></span> | <span data-ttu-id="9b509-122">Value</span><span class="sxs-lookup"><span data-stu-id="9b509-122">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9b509-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9b509-123">Header</span></span><br/> | <dl> <span data-ttu-id="9b509-124"><dt>Dvdmedia.h</dt></span><span class="sxs-lookup"><span data-stu-id="9b509-124"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b509-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="9b509-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b509-126">**Conjunto de propiedades de cambio de frecuencia**</span><span class="sxs-lookup"><span data-stu-id="9b509-126">**Rate Change Property Set**</span></span>](rate-change-property-set.md)
</dt> </dl>

 

 




