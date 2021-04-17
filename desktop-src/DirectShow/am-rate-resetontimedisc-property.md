---
description: Se aplica a Windows Vista y versiones posteriores.
ms.assetid: 3e342219-341e-49a2-9f8f-4188dd7bf719
title: Propiedad AM_RATE_ResetOnTimeDisc (dvdmedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5c26763d32513652a08d38b52bf6fb745d3d321
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690630"
---
# <a name="am_rate_resetontimedisc-property"></a><span data-ttu-id="63ddc-103">\_Propiedad ResetOnTimeDisc de tasa AM \_</span><span class="sxs-lookup"><span data-stu-id="63ddc-103">AM\_RATE\_ResetOnTimeDisc Property</span></span>

<span data-ttu-id="63ddc-104">Se aplica a Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="63ddc-104">Applies to Windows Vista and later.</span></span>

<span data-ttu-id="63ddc-105">Esta propiedad consulta si el descodificador vuelve a sincronizar las marcas de tiempo de salida con las marcas de tiempo de entrada cuando el descodificador recibe un ejemplo con la marca de discontinuidad.</span><span class="sxs-lookup"><span data-stu-id="63ddc-105">This property queries whether the decoder resynchronizes the output time stamps to the input time stamps when the decoder receives a sample with the discontinuity flag.</span></span>

<span data-ttu-id="63ddc-106">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="63ddc-106">This property is read/write.</span></span>



|                   |                               |
|-------------------|-------------------------------|
| <span data-ttu-id="63ddc-107">GUID del conjunto de propiedades</span><span class="sxs-lookup"><span data-stu-id="63ddc-107">Property Set GUID</span></span> | <span data-ttu-id="63ddc-108">\_TSRateChange KSPROPSETID \_ AM</span><span class="sxs-lookup"><span data-stu-id="63ddc-108">AM\_KSPROPSETID\_TSRateChange</span></span> |
| <span data-ttu-id="63ddc-109">Id. de propiedad</span><span class="sxs-lookup"><span data-stu-id="63ddc-109">Property ID</span></span>       | <span data-ttu-id="63ddc-110">Tasa de AM \_ \_ ResetOnTimeDisc</span><span class="sxs-lookup"><span data-stu-id="63ddc-110">AM\_RATE\_ResetOnTimeDisc</span></span>     |
| <span data-ttu-id="63ddc-111">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="63ddc-111">Data Type</span></span>         | <span data-ttu-id="63ddc-112">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="63ddc-112">**DWORD**</span></span>                     |



 

## <a name="remarks"></a><span data-ttu-id="63ddc-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="63ddc-113">Remarks</span></span>

<span data-ttu-id="63ddc-114">Esta propiedad admite cambios de velocidad sin problemas.</span><span class="sxs-lookup"><span data-stu-id="63ddc-114">This property supports smooth rate changes.</span></span> <span data-ttu-id="63ddc-115">Si el valor de esta propiedad es **true** y el descodificador recibe un ejemplo de entrada con la \_ marca TIMEDISCONTINUITY de ejemplo AM \_ , el marco descodificado debe tener la misma marca de tiempo que el marco de entrada.</span><span class="sxs-lookup"><span data-stu-id="63ddc-115">If the value of this property is **TRUE** and the decoder receives an input sample with the AM\_SAMPLE\_TIMEDISCONTINUITY flag, the decoded frame should have the same time stamp as the input frame.</span></span>

<span data-ttu-id="63ddc-116">Para recuperar la \_ marca TIMEDISCONTINUITY de ejemplo AM \_ , llame a [**IMediaSample2:: GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) en el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="63ddc-116">To retrieve the AM\_SAMPLE\_TIMEDISCONTINUITY flag, call [**IMediaSample2::GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) on the sample.</span></span> <span data-ttu-id="63ddc-117">La marca se establece en el miembro **dwSampleFlags** de la estructura de [**\_ \_ propiedades AM SAMPLE2**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) .</span><span class="sxs-lookup"><span data-stu-id="63ddc-117">The flag is set in the **dwSampleFlags** member of the [**AM\_SAMPLE2\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) structure.</span></span>

<span data-ttu-id="63ddc-118">Para obtener más información, consulte [mejoras en la reproducción de DVD en Windows Vista](dvd-playback-enhancements-in-windows-vista.md).</span><span class="sxs-lookup"><span data-stu-id="63ddc-118">For more information, see [DVD Playback Enhancements in Windows Vista](dvd-playback-enhancements-in-windows-vista.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="63ddc-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63ddc-119">Requirements</span></span>



| <span data-ttu-id="63ddc-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="63ddc-120">Requirement</span></span> | <span data-ttu-id="63ddc-121">Value</span><span class="sxs-lookup"><span data-stu-id="63ddc-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="63ddc-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="63ddc-122">Header</span></span><br/> | <dl> <span data-ttu-id="63ddc-123"><dt>Dvdmedia. h</dt></span><span class="sxs-lookup"><span data-stu-id="63ddc-123"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63ddc-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="63ddc-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63ddc-125">**Conjunto de propiedades de cambio de velocidad**</span><span class="sxs-lookup"><span data-stu-id="63ddc-125">**Rate Change Property Set**</span></span>](rate-change-property-set.md)
</dt> </dl>

 

 




