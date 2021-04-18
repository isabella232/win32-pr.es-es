---
description: Filtro de representador de flujo de archivo
ms.assetid: e26462bb-e67f-4522-bec2-88378c4ff442
title: Filtro de representador de flujo de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a64c8d8a0c87dab3aa811c8246be24ded8ee04dc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537888"
---
# <a name="file-stream-renderer-filter"></a><span data-ttu-id="64e7d-103">Filtro de representador de flujo de archivo</span><span class="sxs-lookup"><span data-stu-id="64e7d-103">File Stream Renderer Filter</span></span>

<span data-ttu-id="64e7d-104">El filtro de representador de secuencia de archivos representa los nombres de archivo que se analizan mediante el filtro del [analizador de varios archivos](multi-file-parser-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="64e7d-104">The File Stream Renderer filter renders file names that are parsed by the [Multi-File Parser](multi-file-parser-filter.md) filter.</span></span> <span data-ttu-id="64e7d-105">Para obtener más información, consulte la documentación de ese filtro.</span><span class="sxs-lookup"><span data-stu-id="64e7d-105">For more information, see the documentation for that filter.</span></span>

<span data-ttu-id="64e7d-106">El uso de este filtro está en desuso.</span><span class="sxs-lookup"><span data-stu-id="64e7d-106">The use of this filter is deprecated.</span></span> <span data-ttu-id="64e7d-107">Para representar varios archivos en el mismo gráfico de filtros, la aplicación simplemente debe llamar a **RenderFile** o **AddSourceFilter** varias veces.</span><span class="sxs-lookup"><span data-stu-id="64e7d-107">To render multiple files within the same filter graph, the application should simply call **RenderFile** or **AddSourceFilter** multiple times.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="64e7d-108">Interfaces de filtro</span><span class="sxs-lookup"><span data-stu-id="64e7d-108">Filter interfaces</span></span></td>
<td><span data-ttu-id="64e7d-109"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span><span class="sxs-lookup"><span data-stu-id="64e7d-109"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64e7d-110">Tipos de medios de anclaje de entrada</span><span class="sxs-lookup"><span data-stu-id="64e7d-110">Input pin media types</span></span></td>
<td><ul>
<li><span data-ttu-id="64e7d-111">Tipo principal: MEDIATYPE_File</span><span class="sxs-lookup"><span data-stu-id="64e7d-111">Major type: MEDIATYPE_File</span></span></li>
<li><span data-ttu-id="64e7d-112">Subtipo: GUID_NULL</span><span class="sxs-lookup"><span data-stu-id="64e7d-112">Subtype: GUID_NULL</span></span></li>
<li><span data-ttu-id="64e7d-113">Tipo de formato: MEDIATYPE_File</span><span class="sxs-lookup"><span data-stu-id="64e7d-113">Format type: MEDIATYPE_File</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="64e7d-114">Interfaces de PIN de entrada</span><span class="sxs-lookup"><span data-stu-id="64e7d-114">Input pin interfaces</span></span></td>
<td><span data-ttu-id="64e7d-115"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="64e7d-115"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64e7d-116">Tipos de medios de anclaje de salida</span><span class="sxs-lookup"><span data-stu-id="64e7d-116">Output pin media types</span></span></td>
<td><span data-ttu-id="64e7d-117">None</span><span class="sxs-lookup"><span data-stu-id="64e7d-117">None</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="64e7d-118">Interfaces de clavija de salida</span><span class="sxs-lookup"><span data-stu-id="64e7d-118">Output pin interfaces</span></span></td>
<td><span data-ttu-id="64e7d-119"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-istreambuilder"><strong>IStreamBuilder</strong></a></span><span class="sxs-lookup"><span data-stu-id="64e7d-119"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-istreambuilder"><strong>IStreamBuilder</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64e7d-120">Identificador CLSID</span><span class="sxs-lookup"><span data-stu-id="64e7d-120">Filter CLSID</span></span></td>
<td><span data-ttu-id="64e7d-121">CLSID_FileRend</span><span class="sxs-lookup"><span data-stu-id="64e7d-121">CLSID_FileRend</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="64e7d-122">Executable</span><span class="sxs-lookup"><span data-stu-id="64e7d-122">Executable</span></span></td>
<td><span data-ttu-id="64e7d-123">Quartz.dll</span><span class="sxs-lookup"><span data-stu-id="64e7d-123">Quartz.dll</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64e7d-124"><a href="merit.md">Fundament</a></span><span class="sxs-lookup"><span data-stu-id="64e7d-124"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="64e7d-125">MERIT_UNLIKELY</span><span class="sxs-lookup"><span data-stu-id="64e7d-125">MERIT_UNLIKELY</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="64e7d-126"><a href="filter-categories.md">Categoría de filtro</a></span><span class="sxs-lookup"><span data-stu-id="64e7d-126"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="64e7d-127">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="64e7d-127">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="64e7d-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="64e7d-128">Remarks</span></span>

<span data-ttu-id="64e7d-129">El CLSID del filtro no está definido en UUID. h.</span><span class="sxs-lookup"><span data-stu-id="64e7d-129">The filter's CLSID is not defined in Uuids.h.</span></span> <span data-ttu-id="64e7d-130">Use esta macro en su propio archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="64e7d-130">Use this macro in your own header file:</span></span>


```C++
// {D51BD5A5-7548-11cf-A520-0080C77EF58A}
DEFINE_GUID(CLSID_FileRend,
0xd51bd5A5, 0x7548, 0x11cf, 0xa5, 0x20, 0x0, 0x80, 0xc7, 0x7e, 0xf5, 0x8a);
```



## <a name="related-topics"></a><span data-ttu-id="64e7d-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="64e7d-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="64e7d-132">Filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="64e7d-132">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



