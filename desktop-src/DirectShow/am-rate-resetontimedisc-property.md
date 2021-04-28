---
description: 'AM_RATE_ResetOnTimeDisc propiedad: se aplica a Windows Vista y versiones posteriores.'
ms.assetid: 3e342219-341e-49a2-9f8f-4188dd7bf719
title: AM_RATE_ResetOnTimeDisc propiedad (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e867bff1f344e80ffd06c9c40276515f2cd4920c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096613"
---
# <a name="am_rate_resetontimedisc-property"></a><span data-ttu-id="e5201-103">Propiedad \_ \_ ResetOnTimeDisc de AM RATE</span><span class="sxs-lookup"><span data-stu-id="e5201-103">AM\_RATE\_ResetOnTimeDisc Property</span></span>

<span data-ttu-id="e5201-104">Se aplica a Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="e5201-104">Applies to Windows Vista and later.</span></span>

<span data-ttu-id="e5201-105">Esta propiedad consulta si el descodificador vuelve a sincronizar las marcas de tiempo de salida con las marcas de tiempo de entrada cuando el descodificador recibe una muestra con la marca de discontinuidad.</span><span class="sxs-lookup"><span data-stu-id="e5201-105">This property queries whether the decoder resynchronizes the output time stamps to the input time stamps when the decoder receives a sample with the discontinuity flag.</span></span>

<span data-ttu-id="e5201-106">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="e5201-106">This property is read/write.</span></span>



| <span data-ttu-id="e5201-107">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="e5201-107">Label</span></span> | <span data-ttu-id="e5201-108">Valor</span><span class="sxs-lookup"><span data-stu-id="e5201-108">Value</span></span> |
|-------------------|-------------------------------|
| <span data-ttu-id="e5201-109">GUID del conjunto de propiedades</span><span class="sxs-lookup"><span data-stu-id="e5201-109">Property Set GUID</span></span> | <span data-ttu-id="e5201-110">AM \_ KSPROPSETID \_ TSRateChange</span><span class="sxs-lookup"><span data-stu-id="e5201-110">AM\_KSPROPSETID\_TSRateChange</span></span> |
| <span data-ttu-id="e5201-111">Id. de propiedad</span><span class="sxs-lookup"><span data-stu-id="e5201-111">Property ID</span></span>       | <span data-ttu-id="e5201-112">AM \_ RATE \_ ResetOnTimeDisc</span><span class="sxs-lookup"><span data-stu-id="e5201-112">AM\_RATE\_ResetOnTimeDisc</span></span>     |
| <span data-ttu-id="e5201-113">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="e5201-113">Data Type</span></span>         | <span data-ttu-id="e5201-114">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="e5201-114">**DWORD**</span></span>                     |



 

## <a name="remarks"></a><span data-ttu-id="e5201-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e5201-115">Remarks</span></span>

<span data-ttu-id="e5201-116">Esta propiedad admite cambios de velocidad sin problemas.</span><span class="sxs-lookup"><span data-stu-id="e5201-116">This property supports smooth rate changes.</span></span> <span data-ttu-id="e5201-117">Si el valor de esta propiedad es **TRUE** y el descodificador recibe un ejemplo de entrada con la marca \_ AM SAMPLE TIMEDISCONTINUITY, el marco descodificado debe tener la misma marca de tiempo que el marco de \_ entrada.</span><span class="sxs-lookup"><span data-stu-id="e5201-117">If the value of this property is **TRUE** and the decoder receives an input sample with the AM\_SAMPLE\_TIMEDISCONTINUITY flag, the decoded frame should have the same time stamp as the input frame.</span></span>

<span data-ttu-id="e5201-118">Para recuperar la marca \_ AM SAMPLE \_ TIMEDISCONTINUITY, llame a [**IMediaSample2::GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) en el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="e5201-118">To retrieve the AM\_SAMPLE\_TIMEDISCONTINUITY flag, call [**IMediaSample2::GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) on the sample.</span></span> <span data-ttu-id="e5201-119">La marca se establece en el **miembro dwSampleFlags** de la [**estructura PROPIEDADES DE AM \_ \_ SAMPLE2.**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties)</span><span class="sxs-lookup"><span data-stu-id="e5201-119">The flag is set in the **dwSampleFlags** member of the [**AM\_SAMPLE2\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) structure.</span></span>

<span data-ttu-id="e5201-120">Para obtener más información, vea [Mejoras de reproducción de DVD en Windows Vista.](dvd-playback-enhancements-in-windows-vista.md)</span><span class="sxs-lookup"><span data-stu-id="e5201-120">For more information, see [DVD Playback Enhancements in Windows Vista](dvd-playback-enhancements-in-windows-vista.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e5201-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e5201-121">Requirements</span></span>



| <span data-ttu-id="e5201-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5201-122">Requirement</span></span> | <span data-ttu-id="e5201-123">Value</span><span class="sxs-lookup"><span data-stu-id="e5201-123">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e5201-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e5201-124">Header</span></span><br/> | <dl> <span data-ttu-id="e5201-125"><dt>Dvdmedia.h</dt></span><span class="sxs-lookup"><span data-stu-id="e5201-125"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5201-126">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e5201-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5201-127">**Conjunto de propiedades de cambio de velocidad**</span><span class="sxs-lookup"><span data-stu-id="e5201-127">**Rate Change Property Set**</span></span>](rate-change-property-set.md)
</dt> </dl>

 

 




