---
description: Filtro de descodificador de línea 21
ms.assetid: 48fa5484-1f8c-4133-b2e1-888cb1834402
title: Filtro de descodificador de línea 21
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 839a6ff8e77f4815b74f5de65b8f0e2a565cdc2a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677051"
---
# <a name="line-21-decoder-filter"></a><span data-ttu-id="aff5a-103">Filtro de descodificador de línea 21</span><span class="sxs-lookup"><span data-stu-id="aff5a-103">Line 21 Decoder Filter</span></span>

<span data-ttu-id="aff5a-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="aff5a-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="aff5a-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="aff5a-105">It may be altered or unavailable in subsequent versions.</span></span>

<span data-ttu-id="aff5a-106">Este filtro de descodificador de línea 21 descodifica los datos de línea 21 y dibuja el texto de la leyenda en mapas de bits.</span><span class="sxs-lookup"><span data-stu-id="aff5a-106">This Line 21 Decoder filter decodes line 21 data and draws the caption text onto bitmaps.</span></span>

<span data-ttu-id="aff5a-107">El PIN de entrada se conecta a cualquier proveedor de datos de línea 21, normalmente un descodificador de vídeo de DVD o el filtro del [descodificador de CC](cc-decoder-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="aff5a-107">The input pin connects to any line 21 data provider, typically either a DVD video decoder or the [CC Decoder](cc-decoder-filter.md) filter.</span></span> <span data-ttu-id="aff5a-108">El descodificador de CC proporciona datos de línea 21 procedentes de los VBI de una señal de televisión analógica.</span><span class="sxs-lookup"><span data-stu-id="aff5a-108">The CC Decoder provides line 21 data from the VBI of an analog television signal.</span></span> <span data-ttu-id="aff5a-109">El PIN de salida se conecta a un PIN secundario en el [mezclador de superposición](overlay-mixer-filter.md) o a otro representador de vídeo, como VMR.</span><span class="sxs-lookup"><span data-stu-id="aff5a-109">The output pin connects to a secondary pin on the [Overlay Mixer](overlay-mixer-filter.md) or to another video renderer, such as the VMR.</span></span>

<span data-ttu-id="aff5a-110">Este filtro acepta datos de la línea 21 en el formato de par de bytes estándar o, para DVD, como un paquete para todo el grupo de imágenes (GOP).</span><span class="sxs-lookup"><span data-stu-id="aff5a-110">This filter accepts line 21 data in the standard byte-pair format or, for DVD, as a packet for the whole group of pictures (GOP).</span></span> <span data-ttu-id="aff5a-111">Para cada GOP del flujo de vídeo de DVD, puede haber un paquete de datos de usuario que tenga la información de encabezado y la línea 21 de un GOP concreto.</span><span class="sxs-lookup"><span data-stu-id="aff5a-111">For every GOP in the DVD video stream, there can be a user data packet that has that particular GOP's header information and line 21 data.</span></span> <span data-ttu-id="aff5a-112">El formato de los pares de bytes se define en el estándar EIA/CEA-no-B; Consulte ese estándar para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="aff5a-112">The format of the byte pairs is defined in the EIA/CEA-608-B standard; please refer to that standard for more information.</span></span>

<span data-ttu-id="aff5a-113">Hay disponibles dos versiones de este filtro:</span><span class="sxs-lookup"><span data-stu-id="aff5a-113">Two versions of this filter are available:</span></span>



| <span data-ttu-id="aff5a-114">Filter</span><span class="sxs-lookup"><span data-stu-id="aff5a-114">Filter</span></span>            | <span data-ttu-id="aff5a-115">CLSID</span><span class="sxs-lookup"><span data-stu-id="aff5a-115">CLSID</span></span>                 |
|-------------------|-----------------------|
| <span data-ttu-id="aff5a-116">Descodificador de línea 21</span><span class="sxs-lookup"><span data-stu-id="aff5a-116">Line 21 Decoder</span></span>   | <span data-ttu-id="aff5a-117">CLSID \_ Line21Decoder</span><span class="sxs-lookup"><span data-stu-id="aff5a-117">CLSID\_Line21Decoder</span></span>  |
| <span data-ttu-id="aff5a-118">Descodificador de línea 21 2</span><span class="sxs-lookup"><span data-stu-id="aff5a-118">Line 21 Decoder 2</span></span> | <span data-ttu-id="aff5a-119">CLSID \_ Line21Decoder2</span><span class="sxs-lookup"><span data-stu-id="aff5a-119">CLSID\_Line21Decoder2</span></span> |



 

<span data-ttu-id="aff5a-120">El filtro de la versión 1 se usa en las plataformas de Microsoft® Windows® 95/98/me y Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="aff5a-120">The version 1 filter is used on Microsoft® Windows® 95/98/Me and Windows 2000 platforms.</span></span> <span data-ttu-id="aff5a-121">El filtro de la versión 2 está disponible en Microsoft Windows XP y versiones posteriores, y se usa siempre que el representador de mezcla de vídeo está en el gráfico.</span><span class="sxs-lookup"><span data-stu-id="aff5a-121">The version 2 filter is available in Microsoft Windows XP and later, and is used whenever the Video Mixing Renderer is in the graph.</span></span>

<span data-ttu-id="aff5a-122">La información de la tabla siguiente se aplica a ambas versiones del filtro:</span><span class="sxs-lookup"><span data-stu-id="aff5a-122">The information in the following table applies to both versions of the filter:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="aff5a-123">Interfaces de filtro</span><span class="sxs-lookup"><span data-stu-id="aff5a-123">Filter Interfaces</span></span></td>
<td><span data-ttu-id="aff5a-124"><a href="/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder"><strong>IAMLine21Decoder</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"> <strong>IBaseFilter</strong></a></span><span class="sxs-lookup"><span data-stu-id="aff5a-124"><a href="/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder"><strong>IAMLine21Decoder</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aff5a-125">Tipos de medios de anclaje de entrada</span><span class="sxs-lookup"><span data-stu-id="aff5a-125">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="aff5a-126">Tipo principal: MEDIATYPE_AUXLine21DataSubtype:</span><span class="sxs-lookup"><span data-stu-id="aff5a-126">Major Type: MEDIATYPE_AUXLine21DataSubtype:</span></span><br/>
<ul>
<li><span data-ttu-id="aff5a-127">MEDIASUBTYPE_Line21_BytePair (línea 21 estándar)</span><span class="sxs-lookup"><span data-stu-id="aff5a-127">MEDIASUBTYPE_Line21_BytePair (standard line 21)</span></span></li>
<li><span data-ttu-id="aff5a-128">MEDIASUBTYPE_Line21_GOPPacket (línea 21 de DVD)</span><span class="sxs-lookup"><span data-stu-id="aff5a-128">MEDIASUBTYPE_Line21_GOPPacket (DVD line 21)</span></span></li>
</ul>
<span data-ttu-id="aff5a-129">Tipo de formato: FORMAT_VideoInfo o GUID_NULL</span><span class="sxs-lookup"><span data-stu-id="aff5a-129">Format Type: FORMAT_VideoInfo or GUID_NULL</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aff5a-130">Interfaces de PIN de entrada</span><span class="sxs-lookup"><span data-stu-id="aff5a-130">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="aff5a-131"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="aff5a-131"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aff5a-132">Tipos de medios de anclaje de salida</span><span class="sxs-lookup"><span data-stu-id="aff5a-132">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="aff5a-133">Tipo principal: MEDIATYPE_VideoSubtype:</span><span class="sxs-lookup"><span data-stu-id="aff5a-133">Major type: MEDIATYPE_VideoSubtype:</span></span><br/>
<ul>
<li><span data-ttu-id="aff5a-134">MEDIASUBTYPE_RGB8</span><span class="sxs-lookup"><span data-stu-id="aff5a-134">MEDIASUBTYPE_RGB8</span></span></li>
<li><span data-ttu-id="aff5a-135">MEDIASUBTYPE_RGB555</span><span class="sxs-lookup"><span data-stu-id="aff5a-135">MEDIASUBTYPE_RGB555</span></span></li>
<li><span data-ttu-id="aff5a-136">MEDIASUBTYPE_RGB565</span><span class="sxs-lookup"><span data-stu-id="aff5a-136">MEDIASUBTYPE_RGB565</span></span></li>
<li><span data-ttu-id="aff5a-137">MEDIASUBTYPE_RGB24</span><span class="sxs-lookup"><span data-stu-id="aff5a-137">MEDIASUBTYPE_RGB24</span></span></li>
<li><span data-ttu-id="aff5a-138">MEDIASUBTYPE_RGB32</span><span class="sxs-lookup"><span data-stu-id="aff5a-138">MEDIASUBTYPE_RGB32</span></span></li>
</ul>
<span data-ttu-id="aff5a-139">Tipo de formato: FORMAT_VideoInfo</span><span class="sxs-lookup"><span data-stu-id="aff5a-139">Format Type: FORMAT_VideoInfo</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aff5a-140">Interfaces de clavija de salida</span><span class="sxs-lookup"><span data-stu-id="aff5a-140">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="aff5a-141"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="aff5a-141"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aff5a-142">Identificador CLSID</span><span class="sxs-lookup"><span data-stu-id="aff5a-142">Filter CLSID</span></span></td>
<td><span data-ttu-id="aff5a-143">Vea la tabla anterior</span><span class="sxs-lookup"><span data-stu-id="aff5a-143">See previous table</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aff5a-144">CLSID de la página de propiedades</span><span class="sxs-lookup"><span data-stu-id="aff5a-144">Property Page CLSID</span></span></td>
<td><span data-ttu-id="aff5a-145">None</span><span class="sxs-lookup"><span data-stu-id="aff5a-145">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aff5a-146">Executable</span><span class="sxs-lookup"><span data-stu-id="aff5a-146">Executable</span></span></td>
<td><span data-ttu-id="aff5a-147">qdvd.dll</span><span class="sxs-lookup"><span data-stu-id="aff5a-147">qdvd.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aff5a-148"><a href="merit.md">Fundament</a></span><span class="sxs-lookup"><span data-stu-id="aff5a-148"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="aff5a-149">Descodificador de línea 21: MERIT_NORMALLine 21 descodificador 2: MERIT_NORMAL + 2</span><span class="sxs-lookup"><span data-stu-id="aff5a-149">Line 21 Decoder: MERIT_NORMALLine 21 Decoder 2: MERIT_NORMAL + 2</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aff5a-150"><a href="filter-categories.md">Categoría de filtro</a></span><span class="sxs-lookup"><span data-stu-id="aff5a-150"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="aff5a-151">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="aff5a-151">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="aff5a-152">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="aff5a-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aff5a-153">Filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="aff5a-153">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="aff5a-154">Subtítulos y teletexto</span><span class="sxs-lookup"><span data-stu-id="aff5a-154">Closed Captions and Teletext</span></span>](closed-captions-and-teletext.md)
</dt> <dt>

[<span data-ttu-id="aff5a-155">Configuración del gráfico de filtros de DVD</span><span class="sxs-lookup"><span data-stu-id="aff5a-155">DVD Filter Graph Configuration</span></span>](dvd-filter-graph-configuration.md)
</dt> </dl>

 

 




