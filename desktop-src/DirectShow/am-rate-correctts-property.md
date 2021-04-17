---
description: El navegador de DVD usa esta propiedad para informar al descodificador de que el navegador está configurando las marcas de tiempo correctas en los ejemplos que entrega al descodificador.
ms.assetid: f04e8291-734f-483e-b756-5362beb68d9c
title: Propiedad AM_RATE_CorrectTS (dvdmedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa410b079d3de63de364662c7d5465c82814d24a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690632"
---
# <a name="am_rate_correctts-property"></a><span data-ttu-id="0a81d-103">Propiedad de la frecuencia de la \_ tasa AM \_</span><span class="sxs-lookup"><span data-stu-id="0a81d-103">AM\_RATE\_CorrectTS Property</span></span>

<span data-ttu-id="0a81d-104">El navegador de DVD usa esta propiedad para informar al descodificador de que el navegador está configurando las marcas de tiempo correctas en los ejemplos que entrega al descodificador.</span><span class="sxs-lookup"><span data-stu-id="0a81d-104">The DVD Navigator uses this property to inform the decoder that the Navigator is setting the correct time stamps on the samples it delivers to the decoder.</span></span>



|                   |                               |
|-------------------|-------------------------------|
| <span data-ttu-id="0a81d-105">GUID del conjunto de propiedades</span><span class="sxs-lookup"><span data-stu-id="0a81d-105">Property Set GUID</span></span> | <span data-ttu-id="0a81d-106">\_TSRateChange KSPROPSETID \_ AM</span><span class="sxs-lookup"><span data-stu-id="0a81d-106">AM\_KSPROPSETID\_TSRateChange</span></span> |
| <span data-ttu-id="0a81d-107">Id. de propiedad</span><span class="sxs-lookup"><span data-stu-id="0a81d-107">Property ID</span></span>       | <span data-ttu-id="0a81d-108">Frecuencia de las \_ \_ correcciones de AM</span><span class="sxs-lookup"><span data-stu-id="0a81d-108">AM\_RATE\_CorrectTS</span></span>           |
| <span data-ttu-id="0a81d-109">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="0a81d-109">Data Type</span></span>         | <span data-ttu-id="0a81d-110">**LONG**</span><span class="sxs-lookup"><span data-stu-id="0a81d-110">**LONG**</span></span>                      |



 

## <a name="remarks"></a><span data-ttu-id="0a81d-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0a81d-111">Remarks</span></span>

<span data-ttu-id="0a81d-112">Las versiones anteriores del navegador de DVD no establecieron las marcas de tiempo correctas cuando la velocidad de reproducción era distinta de 1,0.</span><span class="sxs-lookup"><span data-stu-id="0a81d-112">Earlier versions of the DVD Navigator did not set the correct time stamps when the playback rate was something other than 1.0.</span></span> <span data-ttu-id="0a81d-113">Muchos descodificadores solucionan este problema pasando por alto las marcas de tiempo durante el rebobinado o avance rápido, y calculando los tiempos de presentación correctos.</span><span class="sxs-lookup"><span data-stu-id="0a81d-113">Many decoders work around this problem by ignoring the time stamps during rewind or fast forward, and estimating the correct presentation times.</span></span>

<span data-ttu-id="0a81d-114">Estos problemas se han corregido en la versión actual del navegador de DVD.</span><span class="sxs-lookup"><span data-stu-id="0a81d-114">These problems have been corrected in the current version of the DVD Navigator.</span></span> <span data-ttu-id="0a81d-115">Para la compatibilidad con versiones anteriores con los descodificadores existentes, el navegador de DVD indica que las marcas de tiempo son correctas al establecer la \_ propiedad AM Rates \_ correct en el descodificador con el valor **true**.</span><span class="sxs-lookup"><span data-stu-id="0a81d-115">For backward compatibility with existing decoders, the DVD Navigator indicates that the time stamps are correct by setting the AM\_RATE\_CorrectTS property on the decoder with the value **TRUE**.</span></span> <span data-ttu-id="0a81d-116">Cuando se establece esta propiedad, el descodificador debe utilizar las marcas de tiempo reales, en lugar de estimar los tiempos de presentación.</span><span class="sxs-lookup"><span data-stu-id="0a81d-116">When this property is set, the decoder should use the actual time stamps, instead of estimating the presentation times.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a81d-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0a81d-117">Requirements</span></span>



| <span data-ttu-id="0a81d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a81d-118">Requirement</span></span> | <span data-ttu-id="0a81d-119">Value</span><span class="sxs-lookup"><span data-stu-id="0a81d-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0a81d-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0a81d-120">Header</span></span><br/> | <dl> <span data-ttu-id="0a81d-121"><dt>Dvdmedia. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a81d-121"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a81d-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="0a81d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a81d-123">**Conjunto de propiedades de cambio de velocidad**</span><span class="sxs-lookup"><span data-stu-id="0a81d-123">**Rate Change Property Set**</span></span>](rate-change-property-set.md)
</dt> </dl>

 

 




