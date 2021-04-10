---
description: El filtro del codificador AC-3 de Microsoft codifica el audio PCM estéreo en un fragmentada Dolby digital.
ms.assetid: 59d46ee2-d45f-4492-938d-39c55a7368e1
title: Codificador AC-3 de Microsoft (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 160b020e07bb3ba4e4dc5636b58dd0e66f581a6f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152335"
---
# <a name="microsoft-ac-3-encoder"></a><span data-ttu-id="c3027-103">Codificador AC-3 de Microsoft</span><span class="sxs-lookup"><span data-stu-id="c3027-103">Microsoft AC-3 Encoder</span></span>

<span data-ttu-id="c3027-104">El filtro del codificador AC-3 de Microsoft codifica el audio PCM estéreo en un fragmentada Dolby digital.</span><span class="sxs-lookup"><span data-stu-id="c3027-104">The Microsoft AC-3 Encoder filter encodes stereo PCM audio to a Dolby Digital bitstream.</span></span>

> [!Note]  
> <span data-ttu-id="c3027-105">La implementación de Microsoft de la tecnología Dolby Digital está restringida en términos del programa de licencias Dolby digital que usarán las aplicaciones de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c3027-105">The Microsoft implementation of the Dolby Digital technology is restricted under terms of the Dolby Digital licensing program to use by Microsoft applications.</span></span>

 

> [!Note]  
> <span data-ttu-id="c3027-106">Este filtro no se admite en las plataformas basadas en IA-64.</span><span class="sxs-lookup"><span data-stu-id="c3027-106">This filter is not supported on IA-64-based platforms.</span></span>

 



<span data-ttu-id="c3027-107">Información de filtro</span><span class="sxs-lookup"><span data-stu-id="c3027-107">Filter Information</span></span>

<span data-ttu-id="c3027-108">Interfaces de filtro</span><span class="sxs-lookup"><span data-stu-id="c3027-108">Filter Interfaces</span></span>

[<span data-ttu-id="c3027-109">**IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="c3027-109">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/>

<span data-ttu-id="c3027-110">Tipos de medios de anclaje de entrada</span><span class="sxs-lookup"><span data-stu-id="c3027-110">Input Pin Media Types</span></span>

<span data-ttu-id="c3027-111">**MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ PCM**</span><span class="sxs-lookup"><span data-stu-id="c3027-111">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_PCM**</span></span><br/> <span data-ttu-id="c3027-112">El tipo de entrada debe ser estéreo de 48 kHz, 16 bits por muestra.</span><span class="sxs-lookup"><span data-stu-id="c3027-112">The input type must be 48-kHz stereo, 16 bits per sample.</span></span><br/>

<span data-ttu-id="c3027-113">Interfaces de PIN de entrada</span><span class="sxs-lookup"><span data-stu-id="c3027-113">Input Pin Interfaces</span></span>

[<span data-ttu-id="c3027-114">**IMemInputPin**</span><span class="sxs-lookup"><span data-stu-id="c3027-114">**IMemInputPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [<span data-ttu-id="c3027-115">**IPin**</span><span class="sxs-lookup"><span data-stu-id="c3027-115">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [<span data-ttu-id="c3027-116">**IQualityControl**</span><span class="sxs-lookup"><span data-stu-id="c3027-116">**IQualityControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

<span data-ttu-id="c3027-117">Tipos de medios de anclaje de salida</span><span class="sxs-lookup"><span data-stu-id="c3027-117">Output Pin Media Types</span></span>

<span data-ttu-id="c3027-118">**MEDIATYPE \_ Audio**, **MEDIASUBTYPE \_ Dolby \_ AC3**</span><span class="sxs-lookup"><span data-stu-id="c3027-118">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_DOLBY\_AC3**</span></span><br/> <span data-ttu-id="c3027-119">**MEDIATYPE \_ Stream**, **MEDIASUBTYPE \_ Dolby \_ AC3**</span><span class="sxs-lookup"><span data-stu-id="c3027-119">**MEDIATYPE\_Stream**, **MEDIASUBTYPE\_DOLBY\_AC3**</span></span><br/>

<span data-ttu-id="c3027-120">Interfaces de clavija de salida</span><span class="sxs-lookup"><span data-stu-id="c3027-120">Output Pin Interfaces</span></span>

[<span data-ttu-id="c3027-121">**IMediaSeeking**</span><span class="sxs-lookup"><span data-stu-id="c3027-121">**IMediaSeeking**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [<span data-ttu-id="c3027-122">**IPin**</span><span class="sxs-lookup"><span data-stu-id="c3027-122">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [<span data-ttu-id="c3027-123">**IQualityControl**</span><span class="sxs-lookup"><span data-stu-id="c3027-123">**IQualityControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

<span data-ttu-id="c3027-124">Identificador CLSID</span><span class="sxs-lookup"><span data-stu-id="c3027-124">Filter CLSID</span></span>

<span data-ttu-id="c3027-125">**CLSID \_ de CMSAC3Enc** (declarado en wmcodecdsp. h)</span><span class="sxs-lookup"><span data-stu-id="c3027-125">**CLSID\_CMSAC3Enc** (declared in wmcodecdsp.h)</span></span>

<span data-ttu-id="c3027-126">Executable</span><span class="sxs-lookup"><span data-stu-id="c3027-126">Executable</span></span>

<span data-ttu-id="c3027-127">msac3enc.dll</span><span class="sxs-lookup"><span data-stu-id="c3027-127">msac3enc.dll</span></span>

[<span data-ttu-id="c3027-128">Fundament</span><span class="sxs-lookup"><span data-stu-id="c3027-128">Merit</span></span>](merit.md)

<span data-ttu-id="c3027-129">**MÉRITO \_ \_ no se \_ usa**</span><span class="sxs-lookup"><span data-stu-id="c3027-129">**MERIT\_DO\_NOT\_USE**</span></span>

[<span data-ttu-id="c3027-130">Categoría de filtro</span><span class="sxs-lookup"><span data-stu-id="c3027-130">Filter Category</span></span>](filter-categories.md)

<span data-ttu-id="c3027-131">**CLSID \_ LegacyAmFilterCategory**</span><span class="sxs-lookup"><span data-stu-id="c3027-131">**CLSID\_LegacyAmFilterCategory**</span></span>



 

## <a name="remarks"></a><span data-ttu-id="c3027-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c3027-132">Remarks</span></span>

<span data-ttu-id="c3027-133">Este filtro no está disponible para aplicaciones de terceros.</span><span class="sxs-lookup"><span data-stu-id="c3027-133">This filter is not available for use by third-party applications.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3027-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3027-134">Requirements</span></span>



| <span data-ttu-id="c3027-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3027-135">Requirement</span></span> | <span data-ttu-id="c3027-136">Value</span><span class="sxs-lookup"><span data-stu-id="c3027-136">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3027-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c3027-137">Minimum supported client</span></span><br/> | <span data-ttu-id="c3027-138">Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 Home Premium, Windows 7 Professional, Windows 7 Enterprise, Windows 7 Ultimate \[ solo aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="c3027-138">Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 Home Premium, Windows 7 Professional, Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="c3027-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c3027-139">Minimum supported server</span></span><br/> | <span data-ttu-id="c3027-140">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="c3027-140">None supported</span></span><br/>                                                                                                                                                     |
| <span data-ttu-id="c3027-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c3027-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3027-142"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3027-142"><dt>Wmcodecdsp.h</dt></span></span> </dl>                                                                                       |



## <a name="see-also"></a><span data-ttu-id="c3027-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="c3027-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3027-144">Filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="c3027-144">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




