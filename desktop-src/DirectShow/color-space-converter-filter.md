---
description: Filtro de convertidor de espacio de colores
ms.assetid: a6765184-43ce-47b8-9eb1-e15af7e11c93
title: Filtro de convertidor de espacio de colores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f054ee03dd65cf619a697d4441b4d09279e7b912
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494639"
---
# <a name="color-space-converter-filter"></a><span data-ttu-id="763e1-103">Filtro de convertidor de espacio de colores</span><span class="sxs-lookup"><span data-stu-id="763e1-103">Color Space Converter Filter</span></span>

<span data-ttu-id="763e1-104">Este filtro de transformación convierte un tipo de color RGB en otro tipo RGB, como entre el color RGB de 24 bits y 8 bits.</span><span class="sxs-lookup"><span data-stu-id="763e1-104">This transform filter converts from one RGB color type to another RGB type, such as between 24-bit and 8-bit RGB color.</span></span> <span data-ttu-id="763e1-105">Puesto que este tipo de conversión normalmente se trata de forma más eficaz dentro de un descompresor de vídeo, el uso principal del convertidor de espacio de colores es cuando el origen de la secuencia consta de fotogramas RGB sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="763e1-105">Since this type of conversion is generally handled more efficiently within a video decompressor, the main use of the Color Space Converter is when the stream source consists of uncompressed RGB frames.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="763e1-106">Interfaces de filtro</span><span class="sxs-lookup"><span data-stu-id="763e1-106">Filter Interfaces</span></span></td>
<td><span data-ttu-id="763e1-107"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span><span class="sxs-lookup"><span data-stu-id="763e1-107"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="763e1-108">Tipos de medios de anclaje de entrada</span><span class="sxs-lookup"><span data-stu-id="763e1-108">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="763e1-109">MEDIATYPE_Video, FORMAT_VideoInfo.</span><span class="sxs-lookup"><span data-stu-id="763e1-109">MEDIATYPE_Video, FORMAT_VideoInfo.</span></span><br/> <span data-ttu-id="763e1-110">Los siguientes subtipos son válidos:</span><span class="sxs-lookup"><span data-stu-id="763e1-110">The following subtypes are valid:</span></span><br/>
<ul>
<li><span data-ttu-id="763e1-111">MEDIASUBTYPE_RGB8</span><span class="sxs-lookup"><span data-stu-id="763e1-111">MEDIASUBTYPE_RGB8</span></span></li>
<li><span data-ttu-id="763e1-112">MEDIASUBTYPE_RGB555</span><span class="sxs-lookup"><span data-stu-id="763e1-112">MEDIASUBTYPE_RGB555</span></span></li>
<li><span data-ttu-id="763e1-113">MEDIASUBTYPE_RGB565</span><span class="sxs-lookup"><span data-stu-id="763e1-113">MEDIASUBTYPE_RGB565</span></span></li>
<li><span data-ttu-id="763e1-114">MEDIASUBTYPE_RGB24</span><span class="sxs-lookup"><span data-stu-id="763e1-114">MEDIASUBTYPE_RGB24</span></span></li>
<li><span data-ttu-id="763e1-115">MEDIASUBTYPE_RGB32</span><span class="sxs-lookup"><span data-stu-id="763e1-115">MEDIASUBTYPE_RGB32</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="763e1-116">Interfaces de PIN de entrada</span><span class="sxs-lookup"><span data-stu-id="763e1-116">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="763e1-117"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="763e1-117"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="763e1-118">Tipos de medios de anclaje de salida</span><span class="sxs-lookup"><span data-stu-id="763e1-118">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="763e1-119">MEDIATYPE_Video, FORMAT_VideoInfo.</span><span class="sxs-lookup"><span data-stu-id="763e1-119">MEDIATYPE_Video, FORMAT_VideoInfo.</span></span><br/> <span data-ttu-id="763e1-120">Los siguientes subtipos son válidos:</span><span class="sxs-lookup"><span data-stu-id="763e1-120">The following subtypes are valid:</span></span><br/>
<ul>
<li><span data-ttu-id="763e1-121">MEDIASUBTYPE_RGB8</span><span class="sxs-lookup"><span data-stu-id="763e1-121">MEDIASUBTYPE_RGB8</span></span></li>
<li><span data-ttu-id="763e1-122">MEDIASUBTYPE_RGB555</span><span class="sxs-lookup"><span data-stu-id="763e1-122">MEDIASUBTYPE_RGB555</span></span></li>
<li><span data-ttu-id="763e1-123">MEDIASUBTYPE_RGB565</span><span class="sxs-lookup"><span data-stu-id="763e1-123">MEDIASUBTYPE_RGB565</span></span></li>
<li><span data-ttu-id="763e1-124">MEDIASUBTYPE_RGB24</span><span class="sxs-lookup"><span data-stu-id="763e1-124">MEDIASUBTYPE_RGB24</span></span></li>
<li><span data-ttu-id="763e1-125">MEDIASUBTYPE_RGB32</span><span class="sxs-lookup"><span data-stu-id="763e1-125">MEDIASUBTYPE_RGB32</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="763e1-126">Interfaces de clavija de salida</span><span class="sxs-lookup"><span data-stu-id="763e1-126">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="763e1-127"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="763e1-127"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="763e1-128">Identificador CLSID</span><span class="sxs-lookup"><span data-stu-id="763e1-128">Filter CLSID</span></span></td>
<td><span data-ttu-id="763e1-129">CLSID_Colour</span><span class="sxs-lookup"><span data-stu-id="763e1-129">CLSID_Colour</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="763e1-130">CLSID de la página de propiedades</span><span class="sxs-lookup"><span data-stu-id="763e1-130">Property Page CLSID</span></span></td>
<td><span data-ttu-id="763e1-131">Ninguna página de propiedades.</span><span class="sxs-lookup"><span data-stu-id="763e1-131">No property page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="763e1-132">Executable</span><span class="sxs-lookup"><span data-stu-id="763e1-132">Executable</span></span></td>
<td><span data-ttu-id="763e1-133">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="763e1-133">quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="763e1-134"><a href="merit.md">Fundament</a></span><span class="sxs-lookup"><span data-stu-id="763e1-134"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="763e1-135">MERIT_UNLIKELY</span><span class="sxs-lookup"><span data-stu-id="763e1-135">MERIT_UNLIKELY</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="763e1-136"><a href="filter-categories.md">Categoría de filtro</a></span><span class="sxs-lookup"><span data-stu-id="763e1-136"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="763e1-137">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="763e1-137">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="763e1-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="763e1-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="763e1-139">Filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="763e1-139">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




