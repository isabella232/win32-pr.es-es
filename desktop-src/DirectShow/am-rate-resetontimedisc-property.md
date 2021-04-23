---
description: Se aplica a Windows Vista y versiones posteriores.
ms.assetid: 3e342219-341e-49a2-9f8f-4188dd7bf719
title: AM_RATE_ResetOnTimeDisc propiedad (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d465329c2c8de1a66f04a830d183b8cba88c0728
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910253"
---
# <a name="am_rate_resetontimedisc-property"></a><span data-ttu-id="f09f7-103">Propiedad \_ \_ RESETOnTimeDisc de AM RATE</span><span class="sxs-lookup"><span data-stu-id="f09f7-103">AM\_RATE\_ResetOnTimeDisc Property</span></span>

<span data-ttu-id="f09f7-104">Se aplica a Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="f09f7-104">Applies to Windows Vista and later.</span></span>

<span data-ttu-id="f09f7-105">Esta propiedad consulta si el descodificador vuelve a sincronizar las marcas de tiempo de salida con las marcas de tiempo de entrada cuando el descodificador recibe una muestra con la marca de discontinuidad.</span><span class="sxs-lookup"><span data-stu-id="f09f7-105">This property queries whether the decoder resynchronizes the output time stamps to the input time stamps when the decoder receives a sample with the discontinuity flag.</span></span>

<span data-ttu-id="f09f7-106">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="f09f7-106">This property is read/write.</span></span>



| <span data-ttu-id="f09f7-107">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="f09f7-107">Label</span></span> | <span data-ttu-id="f09f7-108">Value</span><span class="sxs-lookup"><span data-stu-id="f09f7-108">Value</span></span> |
|-------------------|-------------------------------|
| <span data-ttu-id="f09f7-109">GUID del conjunto de propiedades</span><span class="sxs-lookup"><span data-stu-id="f09f7-109">Property Set GUID</span></span> | <span data-ttu-id="f09f7-110">AM \_ KSPROPSETID \_ TSRateChange</span><span class="sxs-lookup"><span data-stu-id="f09f7-110">AM\_KSPROPSETID\_TSRateChange</span></span> |
| <span data-ttu-id="f09f7-111">Id. de propiedad</span><span class="sxs-lookup"><span data-stu-id="f09f7-111">Property ID</span></span>       | <span data-ttu-id="f09f7-112">AM \_ RATE \_ ResetOnTimeDisc</span><span class="sxs-lookup"><span data-stu-id="f09f7-112">AM\_RATE\_ResetOnTimeDisc</span></span>     |
| <span data-ttu-id="f09f7-113">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="f09f7-113">Data Type</span></span>         | <span data-ttu-id="f09f7-114">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="f09f7-114">**DWORD**</span></span>                     |



 

## <a name="remarks"></a><span data-ttu-id="f09f7-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f09f7-115">Remarks</span></span>

<span data-ttu-id="f09f7-116">Esta propiedad admite cambios de velocidad fluida.</span><span class="sxs-lookup"><span data-stu-id="f09f7-116">This property supports smooth rate changes.</span></span> <span data-ttu-id="f09f7-117">Si el valor de esta propiedad es **TRUE** y el descodificador recibe un ejemplo de entrada con la marca \_ AM SAMPLE TIMEDISCONTINUITY, el marco descodificado debe tener la misma marca de tiempo que el marco de \_ entrada.</span><span class="sxs-lookup"><span data-stu-id="f09f7-117">If the value of this property is **TRUE** and the decoder receives an input sample with the AM\_SAMPLE\_TIMEDISCONTINUITY flag, the decoded frame should have the same time stamp as the input frame.</span></span>

<span data-ttu-id="f09f7-118">Para recuperar la marca \_ AM SAMPLE \_ TIMEDISCONTINUITY, llame a [**IMediaSample2::GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) en el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="f09f7-118">To retrieve the AM\_SAMPLE\_TIMEDISCONTINUITY flag, call [**IMediaSample2::GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) on the sample.</span></span> <span data-ttu-id="f09f7-119">La marca se establece en el **miembro dwSampleFlags** de la [**estructura PROPIEDADES DE AM \_ \_ SAMPLE2.**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties)</span><span class="sxs-lookup"><span data-stu-id="f09f7-119">The flag is set in the **dwSampleFlags** member of the [**AM\_SAMPLE2\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) structure.</span></span>

<span data-ttu-id="f09f7-120">Para obtener más información, vea [Dvd Playback Enhancements in Windows Vista (Mejoras](dvd-playback-enhancements-in-windows-vista.md)de reproducción de DVD en Windows Vista).</span><span class="sxs-lookup"><span data-stu-id="f09f7-120">For more information, see [DVD Playback Enhancements in Windows Vista](dvd-playback-enhancements-in-windows-vista.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f09f7-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f09f7-121">Requirements</span></span>



| <span data-ttu-id="f09f7-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="f09f7-122">Requirement</span></span> | <span data-ttu-id="f09f7-123">Value</span><span class="sxs-lookup"><span data-stu-id="f09f7-123">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f09f7-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f09f7-124">Header</span></span><br/> | <dl> <span data-ttu-id="f09f7-125"><dt>Dvdmedia.h</dt></span><span class="sxs-lookup"><span data-stu-id="f09f7-125"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f09f7-126">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f09f7-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f09f7-127">**Conjunto de propiedades de cambio de frecuencia**</span><span class="sxs-lookup"><span data-stu-id="f09f7-127">**Rate Change Property Set**</span></span>](rate-change-property-set.md)
</dt> </dl>

 

 




