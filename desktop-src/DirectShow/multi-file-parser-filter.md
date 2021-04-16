---
description: Filtro de analizador de varios archivos
ms.assetid: 8ef06f49-fda4-49e2-9b07-70453a2e897c
title: Filtro de analizador de varios archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44fc83a56bb12c307b85be875a3a2e7e73b744d9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105686353"
---
# <a name="multi-file-parser-filter"></a><span data-ttu-id="c5aa9-103">Filtro de analizador de varios archivos</span><span class="sxs-lookup"><span data-stu-id="c5aa9-103">Multi-File Parser Filter</span></span>

<span data-ttu-id="c5aa9-104">El filtro de analizador de varios archivos analiza un formato de archivo simple que permite especificar varios nombres de archivo como si fueran un archivo.</span><span class="sxs-lookup"><span data-stu-id="c5aa9-104">The Multi-File Parser filter parses a simple file format that enables multiple file names to be specified as though they were one file.</span></span> <span data-ttu-id="c5aa9-105">Estos archivos tienen el formato que se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="c5aa9-105">These files have the format shown in the following example:</span></span>


```C++
;MULTI
https://server/share/video.mpg
https://server/share/captions.smi
```



<span data-ttu-id="c5aa9-106">El uso de este filtro está en desuso.</span><span class="sxs-lookup"><span data-stu-id="c5aa9-106">The use of this filter is deprecated.</span></span> <span data-ttu-id="c5aa9-107">Para representar varios archivos en el mismo gráfico de filtros, la aplicación simplemente debe llamar a **RenderFile** o **AddSourceFilter** varias veces.</span><span class="sxs-lookup"><span data-stu-id="c5aa9-107">To render multiple files within the same filter graph, the application should simply call **RenderFile** or **AddSourceFilter** multiple times.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c5aa9-108">Interfaces de filtro</span><span class="sxs-lookup"><span data-stu-id="c5aa9-108">Filter interfaces</span></span></td>
<td><span data-ttu-id="c5aa9-109"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span><span class="sxs-lookup"><span data-stu-id="c5aa9-109"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c5aa9-110">Tipos de medios de anclaje de entrada</span><span class="sxs-lookup"><span data-stu-id="c5aa9-110">Input pin media types</span></span></td>
<td><ul>
<li><span data-ttu-id="c5aa9-111">Tipo principal: MEDIATYPE_Stream</span><span class="sxs-lookup"><span data-stu-id="c5aa9-111">Major type: MEDIATYPE_Stream</span></span></li>
<li><span data-ttu-id="c5aa9-112">Subtipo: CLSID_MultFile</span><span class="sxs-lookup"><span data-stu-id="c5aa9-112">Subtype: CLSID_MultFile</span></span></li>
<li><span data-ttu-id="c5aa9-113">Tipo de formato: GUID_NULL</span><span class="sxs-lookup"><span data-stu-id="c5aa9-113">Format type: GUID_NULL</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c5aa9-114">Interfaces de PIN de entrada</span><span class="sxs-lookup"><span data-stu-id="c5aa9-114">Input pin interfaces</span></span></td>
<td><span data-ttu-id="c5aa9-115"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="c5aa9-115"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c5aa9-116">Tipos de medios de anclaje de salida</span><span class="sxs-lookup"><span data-stu-id="c5aa9-116">Output pin media types</span></span></td>
<td><ul>
<li><span data-ttu-id="c5aa9-117">Tipo principal: MEDIATYPE_File</span><span class="sxs-lookup"><span data-stu-id="c5aa9-117">Major type: MEDIATYPE_File</span></span></li>
<li><span data-ttu-id="c5aa9-118">Subtipo: GUID_NULL</span><span class="sxs-lookup"><span data-stu-id="c5aa9-118">Subtype: GUID_NULL</span></span></li>
<li><span data-ttu-id="c5aa9-119">Tipo de formato: MEDIATYPE_File</span><span class="sxs-lookup"><span data-stu-id="c5aa9-119">Format type: MEDIATYPE_File</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c5aa9-120">Interfaces de clavija de salida</span><span class="sxs-lookup"><span data-stu-id="c5aa9-120">Output pin interfaces</span></span></td>
<td><span data-ttu-id="c5aa9-121"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="c5aa9-121"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c5aa9-122">Identificador CLSID</span><span class="sxs-lookup"><span data-stu-id="c5aa9-122">Filter CLSID</span></span></td>
<td><span data-ttu-id="c5aa9-123">CLSID_MultFile</span><span class="sxs-lookup"><span data-stu-id="c5aa9-123">CLSID_MultFile</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c5aa9-124">Executable</span><span class="sxs-lookup"><span data-stu-id="c5aa9-124">Executable</span></span></td>
<td><span data-ttu-id="c5aa9-125">Quartz.dll</span><span class="sxs-lookup"><span data-stu-id="c5aa9-125">Quartz.dll</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c5aa9-126"><a href="merit.md">Fundament</a></span><span class="sxs-lookup"><span data-stu-id="c5aa9-126"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="c5aa9-127">MERIT_UNLIKELY</span><span class="sxs-lookup"><span data-stu-id="c5aa9-127">MERIT_UNLIKELY</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c5aa9-128"><a href="filter-categories.md">Categoría de filtro</a></span><span class="sxs-lookup"><span data-stu-id="c5aa9-128"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="c5aa9-129">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="c5aa9-129">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="c5aa9-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c5aa9-130">Remarks</span></span>

<span data-ttu-id="c5aa9-131">El filtro crea un PIN de salida para cada archivo que aparece en el archivo de código fuente.</span><span class="sxs-lookup"><span data-stu-id="c5aa9-131">The filter creates one output pin for each file listed in the source file.</span></span> <span data-ttu-id="c5aa9-132">El tipo de salida es el \_ archivo MEDIATYPE y el bloque de formato para el tipo de salida es una cadena de caracteres anchos que contiene el nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="c5aa9-132">The output type is MEDIATYPE\_File, and the format block for the output type is a wide-character string that contains the file name.</span></span> <span data-ttu-id="c5aa9-133">Cada pin se conecta a una instancia del filtro de [representador de secuencia de archivos](file-stream-renderer-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="c5aa9-133">Each pin connects to an instance of the [File Stream Renderer](file-stream-renderer-filter.md) filter.</span></span> <span data-ttu-id="c5aa9-134">El filtro de representador de flujo de archivo crea un PIN de salida, que expone la interfaz [**IStreamBuilder**](/windows/desktop/api/Strmif/nn-strmif-istreambuilder) .</span><span class="sxs-lookup"><span data-stu-id="c5aa9-134">The File Stream Renderer filter creates one output pin, which exposes the [**IStreamBuilder**](/windows/desktop/api/Strmif/nn-strmif-istreambuilder) interface.</span></span> <span data-ttu-id="c5aa9-135">El PIN de salida representa el archivo especificado.</span><span class="sxs-lookup"><span data-stu-id="c5aa9-135">The output pin renders the specified file.</span></span> <span data-ttu-id="c5aa9-136">No viajan los datos multimedia entre el analizador de varios archivos y el representador de flujo de archivos.</span><span class="sxs-lookup"><span data-stu-id="c5aa9-136">No media data travels between the Multi-File Parser and the File Stream Renderer.</span></span>

<span data-ttu-id="c5aa9-137">El CLSID del filtro no está definido en UUID. h.</span><span class="sxs-lookup"><span data-stu-id="c5aa9-137">The filter's CLSID is not defined in Uuids.h.</span></span> <span data-ttu-id="c5aa9-138">Use esta macro en su propio archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="c5aa9-138">Use this macro in your own header file:</span></span>


```C++
// {D51BD5A3-7548-11cf-A520-0080C77EF58A}
DEFINE_GUID(CLSID_MultFile,
0xd51bd5a3, 0x7548, 0x11cf, 0xa5, 0x20, 0x0, 0x80, 0xc7, 0x7e, 0xf5, 0x8a);
```



## <a name="related-topics"></a><span data-ttu-id="c5aa9-139">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c5aa9-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5aa9-140">Filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="c5aa9-140">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



