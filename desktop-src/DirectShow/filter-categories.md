---
description: En las tablas siguientes se enumeran los CLSID de las categorías de filtros de DirectShow.
ms.assetid: cab4e2c9-eab9-4836-adfc-870490ca5b6b
title: Categorías de filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0c4ccb9443c405abcbd0b9afbd406d6faf2558a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104422768"
---
# <a name="filter-categories"></a><span data-ttu-id="07cdf-103">Categorías de filtro</span><span class="sxs-lookup"><span data-stu-id="07cdf-103">Filter Categories</span></span>

<span data-ttu-id="07cdf-104">En las tablas siguientes se enumeran los CLSID de las categorías de filtros de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="07cdf-104">The following tables list the CLSIDs for the DirectShow filter categories.</span></span>

-   [<span data-ttu-id="07cdf-105">Categorías de filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="07cdf-105">DirectShow Filter Categories</span></span>](#directshow-filter-categories)
-   [<span data-ttu-id="07cdf-106">Otras categorías de filtro</span><span class="sxs-lookup"><span data-stu-id="07cdf-106">Other Filter Categories</span></span>](#other-filter-categories)
-   [<span data-ttu-id="07cdf-107">Metacategoría del filtro de DirectShow</span><span class="sxs-lookup"><span data-stu-id="07cdf-107">DirectShow Filter Meta-Category</span></span>](#directshow-filter-meta-category)
-   [<span data-ttu-id="07cdf-108">Categorías de DMO</span><span class="sxs-lookup"><span data-stu-id="07cdf-108">DMO Categories</span></span>](#dmo-categories)
-   [<span data-ttu-id="07cdf-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="07cdf-109">Related topics</span></span>](#related-topics)

## <a name="directshow-filter-categories"></a><span data-ttu-id="07cdf-110">Categorías de filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="07cdf-110">DirectShow Filter Categories</span></span>

<span data-ttu-id="07cdf-111">Las categorías enumeradas aquí se enumeran mediante el [asignador de filtros](filter-mapper.md).</span><span class="sxs-lookup"><span data-stu-id="07cdf-111">The categories listed here are enumerated by the [Filter Mapper](filter-mapper.md).</span></span> <span data-ttu-id="07cdf-112">Sin embargo, de forma predeterminada, el asignador de filtros omite las categorías con méritos de mérito \_ \_ no \_ usar o menos.</span><span class="sxs-lookup"><span data-stu-id="07cdf-112">By default, however, the Filter Mapper ignores categories with merits of MERIT\_DO\_NOT\_USE or less.</span></span> <span data-ttu-id="07cdf-113">Para obtener más información, vea [**IFilterMapper2:: EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters).</span><span class="sxs-lookup"><span data-stu-id="07cdf-113">For more information, see [**IFilterMapper2::EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters).</span></span> <span data-ttu-id="07cdf-114">Todas las categorías que se enumeran aquí también se pueden enumerar con el [enumerador de dispositivos del sistema](system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="07cdf-114">All of the categories listed here can also be enumerated with the [System Device Enumerator](system-device-enumerator.md).</span></span>

<span data-ttu-id="07cdf-115">Las siguientes categorías se declaran en UUID. h.</span><span class="sxs-lookup"><span data-stu-id="07cdf-115">The following categories are declared in Uuids.h.</span></span> <span data-ttu-id="07cdf-116">Incluya el archivo de encabezado DShow. h.</span><span class="sxs-lookup"><span data-stu-id="07cdf-116">Include the header file Dshow.h.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="07cdf-117">Nombre descriptivo</span><span class="sxs-lookup"><span data-stu-id="07cdf-117">Friendly Name</span></span></th>
<th><span data-ttu-id="07cdf-118">CLSID</span><span class="sxs-lookup"><span data-stu-id="07cdf-118">CLSID</span></span></th>
<th><span data-ttu-id="07cdf-119">Fundament</span><span class="sxs-lookup"><span data-stu-id="07cdf-119">Merit</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="07cdf-120">Orígenes de captura de audio</span><span class="sxs-lookup"><span data-stu-id="07cdf-120">Audio Capture Sources</span></span></td>
<td><span data-ttu-id="07cdf-121"><strong>CLSID_AudioInputDeviceCategory</strong></span><span class="sxs-lookup"><span data-stu-id="07cdf-121"><strong>CLSID_AudioInputDeviceCategory</strong></span></span></td>
<td><span data-ttu-id="07cdf-122"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="07cdf-122"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="07cdf-123">Compresores de audio</span><span class="sxs-lookup"><span data-stu-id="07cdf-123">Audio Compressors</span></span></td>
<td><span data-ttu-id="07cdf-124"><strong>CLSID_AudioCompressorCategory</strong></span><span class="sxs-lookup"><span data-stu-id="07cdf-124"><strong>CLSID_AudioCompressorCategory</strong></span></span></td>
<td><span data-ttu-id="07cdf-125"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="07cdf-125"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="07cdf-126">Representadores de audio</span><span class="sxs-lookup"><span data-stu-id="07cdf-126">Audio Renderers</span></span></td>
<td><span data-ttu-id="07cdf-127"><strong>CLSID_AudioRendererCategory</strong></span><span class="sxs-lookup"><span data-stu-id="07cdf-127"><strong>CLSID_AudioRendererCategory</strong></span></span></td>
<td><span data-ttu-id="07cdf-128"><strong>MERIT_NORMAL</strong></span><span class="sxs-lookup"><span data-stu-id="07cdf-128"><strong>MERIT_NORMAL</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="07cdf-129">Filtros de control de dispositivo</span><span class="sxs-lookup"><span data-stu-id="07cdf-129">Device Control Filters</span></span></td>
<td><span data-ttu-id="07cdf-130"><strong>CLSID_DeviceControlCategory</strong></span><span class="sxs-lookup"><span data-stu-id="07cdf-130"><strong>CLSID_DeviceControlCategory</strong></span></span></td>
<td><span data-ttu-id="07cdf-131"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="07cdf-131"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="07cdf-132">Filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="07cdf-132">DirectShow Filters</span></span></td>
<td><span data-ttu-id="07cdf-133"><strong>CLSID_LegacyAmFilterCategory</strong></span><span class="sxs-lookup"><span data-stu-id="07cdf-133"><strong>CLSID_LegacyAmFilterCategory</strong></span></span></td>
<td><span data-ttu-id="07cdf-134"><strong>MERIT_NORMAL</strong></span><span class="sxs-lookup"><span data-stu-id="07cdf-134"><strong>MERIT_NORMAL</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="07cdf-135">Representadores externos</span><span class="sxs-lookup"><span data-stu-id="07cdf-135">External Renderers</span></span></td>
<td><span data-ttu-id="07cdf-136"><strong>CLSID_TransmitCategory</strong></span><span class="sxs-lookup"><span data-stu-id="07cdf-136"><strong>CLSID_TransmitCategory</strong></span></span></td>
<td><span data-ttu-id="07cdf-137"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="07cdf-137"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="07cdf-138">Representadores MIDI</span><span class="sxs-lookup"><span data-stu-id="07cdf-138">Midi Renderers</span></span></td>
<td><span data-ttu-id="07cdf-139"><strong>CLSID_MidiRendererCategory</strong></span><span class="sxs-lookup"><span data-stu-id="07cdf-139"><strong>CLSID_MidiRendererCategory</strong></span></span></td>
<td><span data-ttu-id="07cdf-140"><strong>MERIT_NORMAL</strong></span><span class="sxs-lookup"><span data-stu-id="07cdf-140"><strong>MERIT_NORMAL</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="07cdf-141">Orígenes de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="07cdf-141">Video Capture Sources</span></span></td>
<td><span data-ttu-id="07cdf-142"><strong>CLSID_VideoInputDeviceCategory</strong></span><span class="sxs-lookup"><span data-stu-id="07cdf-142"><strong>CLSID_VideoInputDeviceCategory</strong></span></span></td>
<td><span data-ttu-id="07cdf-143"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="07cdf-143"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="07cdf-144">Compresores de vídeo</span><span class="sxs-lookup"><span data-stu-id="07cdf-144">Video Compressors</span></span></td>
<td><span data-ttu-id="07cdf-145"><strong>CLSID_VideoCompressorCategory</strong></span><span class="sxs-lookup"><span data-stu-id="07cdf-145"><strong>CLSID_VideoCompressorCategory</strong></span></span></td>
<td><span data-ttu-id="07cdf-146"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="07cdf-146"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="07cdf-147">Dispositivos de descompresión de secuencia WDM</span><span class="sxs-lookup"><span data-stu-id="07cdf-147">WDM Stream Decompression Devices</span></span></td>
<td><span data-ttu-id="07cdf-148"><strong>CLSID_DVDHWDecodersCategory</strong>
</span><span class="sxs-lookup"><span data-stu-id="07cdf-148"><strong>CLSID_DVDHWDecodersCategory</strong>
</span></span><blockquote>
[!Note]<br />
<span data-ttu-id="07cdf-149">Esta categoría contiene descodificadores de DVD de hardware.</span><span class="sxs-lookup"><span data-stu-id="07cdf-149">This category contains hardware DVD decoders.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="07cdf-150"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="07cdf-150"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="07cdf-151">Dispositivos de captura de transmisión por secuencias WDM</span><span class="sxs-lookup"><span data-stu-id="07cdf-151">WDM Streaming Capture Devices</span></span></td>
<td><span data-ttu-id="07cdf-152"><strong>AM_KSCATEGORY_CAPTURE</strong></span><span class="sxs-lookup"><span data-stu-id="07cdf-152"><strong>AM_KSCATEGORY_CAPTURE</strong></span></span></td>
<td><span data-ttu-id="07cdf-153"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="07cdf-153"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="07cdf-154">Dispositivos de barras cruzadas de transmisión por secuencias WDM</span><span class="sxs-lookup"><span data-stu-id="07cdf-154">WDM Streaming Crossbar Devices</span></span></td>
<td><span data-ttu-id="07cdf-155"><strong>AM_KSCATEGORY_CROSSBAR</strong></span><span class="sxs-lookup"><span data-stu-id="07cdf-155"><strong>AM_KSCATEGORY_CROSSBAR</strong></span></span></td>
<td><span data-ttu-id="07cdf-156"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="07cdf-156"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="07cdf-157">Dispositivos de representación de transmisión por secuencias WDM</span><span class="sxs-lookup"><span data-stu-id="07cdf-157">WDM Streaming Rendering Devices</span></span></td>
<td><span data-ttu-id="07cdf-158"><strong>AM_KSCATEGORY_RENDER</strong></span><span class="sxs-lookup"><span data-stu-id="07cdf-158"><strong>AM_KSCATEGORY_RENDER</strong></span></span></td>
<td><span data-ttu-id="07cdf-159"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="07cdf-159"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="07cdf-160">Dispositivos de transmisión por secuencias WDM/divisora</span><span class="sxs-lookup"><span data-stu-id="07cdf-160">WDM Streaming Tee/Splitter Devices</span></span></td>
<td><span data-ttu-id="07cdf-161"><strong>AM_KSCATEGORY_SPLITTER</strong></span><span class="sxs-lookup"><span data-stu-id="07cdf-161"><strong>AM_KSCATEGORY_SPLITTER</strong></span></span></td>
<td><span data-ttu-id="07cdf-162"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="07cdf-162"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="07cdf-163">Dispositivos de audio de TV de transmisión por secuencias WDM</span><span class="sxs-lookup"><span data-stu-id="07cdf-163">WDM Streaming TV Audio Devices</span></span></td>
<td><span data-ttu-id="07cdf-164"><strong>AM_KSCATEGORY_TVAUDIO</strong></span><span class="sxs-lookup"><span data-stu-id="07cdf-164"><strong>AM_KSCATEGORY_TVAUDIO</strong></span></span></td>
<td><span data-ttu-id="07cdf-165"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="07cdf-165"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="07cdf-166">Dispositivos de sintonizador de TV de streaming WDM</span><span class="sxs-lookup"><span data-stu-id="07cdf-166">WDM Streaming TV Tuner Devices</span></span></td>
<td><span data-ttu-id="07cdf-167"><strong>AM_KSCATEGORY_TVTUNER</strong></span><span class="sxs-lookup"><span data-stu-id="07cdf-167"><strong>AM_KSCATEGORY_TVTUNER</strong></span></span></td>
<td><span data-ttu-id="07cdf-168"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="07cdf-168"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="07cdf-169">Códecs de streaming VBI WDM</span><span class="sxs-lookup"><span data-stu-id="07cdf-169">WDM Streaming VBI Codecs</span></span></td>
<td><span data-ttu-id="07cdf-170"><strong>AM_KSCATEGORY_VBICODEC</strong></span><span class="sxs-lookup"><span data-stu-id="07cdf-170"><strong>AM_KSCATEGORY_VBICODEC</strong></span></span></td>
<td><span data-ttu-id="07cdf-171"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="07cdf-171"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="07cdf-172">Las siguientes categorías se declaran en el archivo de encabezado KS. h.</span><span class="sxs-lookup"><span data-stu-id="07cdf-172">The following categories are declared in the header file Ks.h.</span></span>



| <span data-ttu-id="07cdf-173">Nombre descriptivo</span><span class="sxs-lookup"><span data-stu-id="07cdf-173">Friendly Name</span></span>                          | <span data-ttu-id="07cdf-174">CLSID</span><span class="sxs-lookup"><span data-stu-id="07cdf-174">CLSID</span></span>                                   | <span data-ttu-id="07cdf-175">Fundament</span><span class="sxs-lookup"><span data-stu-id="07cdf-175">Merit</span></span>                   |
|----------------------------------------|-----------------------------------------|-------------------------|
| <span data-ttu-id="07cdf-176">Transformaciones de comunicación de transmisión por secuencias WDM</span><span class="sxs-lookup"><span data-stu-id="07cdf-176">WDM Streaming Communication Transforms</span></span> | <span data-ttu-id="07cdf-177">**KSCATEGORY \_ COMMUNICATIONSTRANSFORM**</span><span class="sxs-lookup"><span data-stu-id="07cdf-177">**KSCATEGORY\_COMMUNICATIONSTRANSFORM**</span></span> | <span data-ttu-id="07cdf-178">**MÉRITO \_ \_ no se \_ usa**</span><span class="sxs-lookup"><span data-stu-id="07cdf-178">**MERIT\_DO\_NOT\_USE**</span></span> |
| <span data-ttu-id="07cdf-179">Transformaciones de datos de transmisión por secuencias WDM</span><span class="sxs-lookup"><span data-stu-id="07cdf-179">WDM Streaming Data Transforms</span></span>          | <span data-ttu-id="07cdf-180">**KSCATEGORY ( \_ transformación)**</span><span class="sxs-lookup"><span data-stu-id="07cdf-180">**KSCATEGORY\_DATATRANSFORM**</span></span>           | <span data-ttu-id="07cdf-181">**MÉRITO \_ \_ no se \_ usa**</span><span class="sxs-lookup"><span data-stu-id="07cdf-181">**MERIT\_DO\_NOT\_USE**</span></span> |
| <span data-ttu-id="07cdf-182">Transformaciones de la interfaz de streaming WDM</span><span class="sxs-lookup"><span data-stu-id="07cdf-182">WDM Streaming Interface Transforms</span></span>     | <span data-ttu-id="07cdf-183">**KSCATEGORY \_ INTERFACETRANSFORM**</span><span class="sxs-lookup"><span data-stu-id="07cdf-183">**KSCATEGORY\_INTERFACETRANSFORM**</span></span>      | <span data-ttu-id="07cdf-184">**MÉRITO \_ \_ no se \_ usa**</span><span class="sxs-lookup"><span data-stu-id="07cdf-184">**MERIT\_DO\_NOT\_USE**</span></span> |
| <span data-ttu-id="07cdf-185">Dispositivos de mezclador de transmisión por secuencias WDM</span><span class="sxs-lookup"><span data-stu-id="07cdf-185">WDM Streaming Mixer Devices</span></span>            | <span data-ttu-id="07cdf-186">**\_mezclador KSCATEGORY**</span><span class="sxs-lookup"><span data-stu-id="07cdf-186">**KSCATEGORY\_MIXER**</span></span>                   | <span data-ttu-id="07cdf-187">**MÉRITO \_ \_ no se \_ usa**</span><span class="sxs-lookup"><span data-stu-id="07cdf-187">**MERIT\_DO\_NOT\_USE**</span></span> |



 

<span data-ttu-id="07cdf-188">Las siguientes categorías se declaran en el archivo de encabezado Bdamedia. h.</span><span class="sxs-lookup"><span data-stu-id="07cdf-188">The following categories are declared in the header file Bdamedia.h.</span></span> <span data-ttu-id="07cdf-189">Incluya los archivos de encabezado siguientes: KS. h, ksmedia. h y bdamedia. h.</span><span class="sxs-lookup"><span data-stu-id="07cdf-189">Include the following header files: ks.h, ksmedia.h, and bdamedia.h.</span></span>



| <span data-ttu-id="07cdf-190">Nombre descriptivo</span><span class="sxs-lookup"><span data-stu-id="07cdf-190">Friendly Name</span></span>                       | <span data-ttu-id="07cdf-191">CLSID</span><span class="sxs-lookup"><span data-stu-id="07cdf-191">CLSID</span></span>                                       | <span data-ttu-id="07cdf-192">Fundament</span><span class="sxs-lookup"><span data-stu-id="07cdf-192">Merit</span></span>                   |
|-------------------------------------|---------------------------------------------|-------------------------|
| <span data-ttu-id="07cdf-193">Proveedores de redes BDA</span><span class="sxs-lookup"><span data-stu-id="07cdf-193">BDA Network Providers</span></span>               | <span data-ttu-id="07cdf-194">**\_proveedor de \_ red \_ BDA de KSCATEGORY**</span><span class="sxs-lookup"><span data-stu-id="07cdf-194">**KSCATEGORY\_BDA\_NETWORK\_PROVIDER**</span></span>      | <span data-ttu-id="07cdf-195">**MÉRITO \_ normal**</span><span class="sxs-lookup"><span data-stu-id="07cdf-195">**MERIT\_NORMAL**</span></span>       |
| <span data-ttu-id="07cdf-196">Componentes del receptor de BDA</span><span class="sxs-lookup"><span data-stu-id="07cdf-196">BDA Receiver Components</span></span>             | <span data-ttu-id="07cdf-197">**\_componente de \_ receptor de BDA de KSCATEGORY \_**</span><span class="sxs-lookup"><span data-stu-id="07cdf-197">**KSCATEGORY\_BDA\_RECEIVER\_COMPONENT**</span></span>    | <span data-ttu-id="07cdf-198">**MÉRITO \_ \_ no se \_ usa**</span><span class="sxs-lookup"><span data-stu-id="07cdf-198">**MERIT\_DO\_NOT\_USE**</span></span> |
| <span data-ttu-id="07cdf-199">Filtros de representación de BDA</span><span class="sxs-lookup"><span data-stu-id="07cdf-199">BDA Rendering Filters</span></span>               | <span data-ttu-id="07cdf-200">**\_receptor de IP de KSCATEGORY \_**</span><span class="sxs-lookup"><span data-stu-id="07cdf-200">**KSCATEGORY\_IP\_SINK**</span></span>                    | <span data-ttu-id="07cdf-201">**MÉRITO \_ \_ no se \_ usa**</span><span class="sxs-lookup"><span data-stu-id="07cdf-201">**MERIT\_DO\_NOT\_USE**</span></span> |
| <span data-ttu-id="07cdf-202">Filtros de origen de BDA</span><span class="sxs-lookup"><span data-stu-id="07cdf-202">BDA Source Filters</span></span>                  | <span data-ttu-id="07cdf-203">**\_ \_ sintonizador de red BDA de KSCATEGORY \_**</span><span class="sxs-lookup"><span data-stu-id="07cdf-203">**KSCATEGORY\_BDA\_NETWORK\_TUNER**</span></span>         | <span data-ttu-id="07cdf-204">**MÉRITO \_ \_ no se \_ usa**</span><span class="sxs-lookup"><span data-stu-id="07cdf-204">**MERIT\_DO\_NOT\_USE**</span></span> |
| <span data-ttu-id="07cdf-205">Representadores de información de transporte BDA</span><span class="sxs-lookup"><span data-stu-id="07cdf-205">BDA Transport Information Renderers</span></span> | <span data-ttu-id="07cdf-206">**\_información de \_ transporte de BDA de KSCATEGORY \_**</span><span class="sxs-lookup"><span data-stu-id="07cdf-206">**KSCATEGORY\_BDA\_TRANSPORT\_INFORMATION**</span></span> | <span data-ttu-id="07cdf-207">**MÉRITO \_ normal**</span><span class="sxs-lookup"><span data-stu-id="07cdf-207">**MERIT\_NORMAL**</span></span>       |



 

> [!Note]  
> <span data-ttu-id="07cdf-208">Los descodificadores se registran en la categoría "filtros de DirectShow" (CLSID \_ LegacyAmFilterCategory).</span><span class="sxs-lookup"><span data-stu-id="07cdf-208">Decoders are registered under the "DirectShow Filters" category (CLSID\_LegacyAmFilterCategory).</span></span>

 

## <a name="other-filter-categories"></a><span data-ttu-id="07cdf-209">Otras categorías de filtro</span><span class="sxs-lookup"><span data-stu-id="07cdf-209">Other Filter Categories</span></span>

<span data-ttu-id="07cdf-210">Las categorías que se enumeran aquí se pueden enumerar con el enumerador de dispositivos del sistema, pero no son visibles para el asignador de filtros y la [conexión inteligente](intelligent-connect.md)no las usa.</span><span class="sxs-lookup"><span data-stu-id="07cdf-210">The categories listed here can be enumerated with the System Device Enumerator, but are not visible to the Filter Mapper and are not used by [Intelligent Connect](intelligent-connect.md).</span></span>

<span data-ttu-id="07cdf-211">Las siguientes categorías se declaran en el archivo de encabezado QEDIT. h.</span><span class="sxs-lookup"><span data-stu-id="07cdf-211">The following categories are declared in the header file Qedit.h.</span></span>



| <span data-ttu-id="07cdf-212">Nombre descriptivo</span><span class="sxs-lookup"><span data-stu-id="07cdf-212">Friendly Name</span></span>            | <span data-ttu-id="07cdf-213">CLID</span><span class="sxs-lookup"><span data-stu-id="07cdf-213">CLID</span></span>                             | <span data-ttu-id="07cdf-214">Fundament</span><span class="sxs-lookup"><span data-stu-id="07cdf-214">Merit</span></span>                   |
|--------------------------|----------------------------------|-------------------------|
| <span data-ttu-id="07cdf-215">Efectos de vídeo (1 entrada)</span><span class="sxs-lookup"><span data-stu-id="07cdf-215">Video Effects (1 input)</span></span>  | <span data-ttu-id="07cdf-216">**CLSID \_ VideoEffects1Category**</span><span class="sxs-lookup"><span data-stu-id="07cdf-216">**CLSID\_VideoEffects1Category**</span></span> | <span data-ttu-id="07cdf-217">**MÉRITO \_ \_ no se \_ usa**</span><span class="sxs-lookup"><span data-stu-id="07cdf-217">**MERIT\_DO\_NOT\_USE**</span></span> |
| <span data-ttu-id="07cdf-218">Efectos de vídeo (2 entradas)</span><span class="sxs-lookup"><span data-stu-id="07cdf-218">Video Effects (2 inputs)</span></span> | <span data-ttu-id="07cdf-219">**CLSID \_ VideoEffects2Category**</span><span class="sxs-lookup"><span data-stu-id="07cdf-219">**CLSID\_VideoEffects2Category**</span></span> | <span data-ttu-id="07cdf-220">**MÉRITO \_ \_ no se \_ usa**</span><span class="sxs-lookup"><span data-stu-id="07cdf-220">**MERIT\_DO\_NOT\_USE**</span></span> |



 

<span data-ttu-id="07cdf-221">Estas categorías contienen efectos de vídeo y transiciones para los [servicios de edición de DirectShow](directshow-editing-services.md):</span><span class="sxs-lookup"><span data-stu-id="07cdf-221">These categories contain video effects and transitions for [DirectShow Editing Services](directshow-editing-services.md):</span></span>

-   <span data-ttu-id="07cdf-222">"Efectos de vídeo (1 entrada)" contiene efectos de vídeo.</span><span class="sxs-lookup"><span data-stu-id="07cdf-222">"Video Effects (1 input)" contains video effects.</span></span>
-   <span data-ttu-id="07cdf-223">"Efectos de vídeo (2 entradas)" contiene transiciones de vídeo.</span><span class="sxs-lookup"><span data-stu-id="07cdf-223">"Video Effects (2 input)" contains video transitions.</span></span>

<span data-ttu-id="07cdf-224">Para obtener más información, consulte [enumeración de efectos y transiciones](enumerating-effects-and-transitions.md).</span><span class="sxs-lookup"><span data-stu-id="07cdf-224">For more information, see [Enumerating Effects and Transitions](enumerating-effects-and-transitions.md).</span></span>

<span data-ttu-id="07cdf-225">Las siguientes categorías se declaran en el archivo de encabezado UUID. h.</span><span class="sxs-lookup"><span data-stu-id="07cdf-225">The following categories are declared in the header file Uuids.h.</span></span> <span data-ttu-id="07cdf-226">Incluya el archivo de encabezado DShow. h.</span><span class="sxs-lookup"><span data-stu-id="07cdf-226">Include the header file Dshow.h.</span></span>



| <span data-ttu-id="07cdf-227">Nombre descriptivo</span><span class="sxs-lookup"><span data-stu-id="07cdf-227">Friendly Name</span></span>       | <span data-ttu-id="07cdf-228">CLID</span><span class="sxs-lookup"><span data-stu-id="07cdf-228">CLID</span></span>                                | <span data-ttu-id="07cdf-229">Fundament</span><span class="sxs-lookup"><span data-stu-id="07cdf-229">Merit</span></span>                   |
|---------------------|-------------------------------------|-------------------------|
| <span data-ttu-id="07cdf-230">Codificadores de encapi</span><span class="sxs-lookup"><span data-stu-id="07cdf-230">EncAPI Encoders</span></span>     | <span data-ttu-id="07cdf-231">**CLSID \_ MediaEncoderCategory**</span><span class="sxs-lookup"><span data-stu-id="07cdf-231">**CLSID\_MediaEncoderCategory**</span></span>     | <span data-ttu-id="07cdf-232">**MÉRITO \_ \_ no se \_ usa**</span><span class="sxs-lookup"><span data-stu-id="07cdf-232">**MERIT\_DO\_NOT\_USE**</span></span> |
| <span data-ttu-id="07cdf-233">Multiplexadores de encapi</span><span class="sxs-lookup"><span data-stu-id="07cdf-233">EncAPI Multiplexers</span></span> | <span data-ttu-id="07cdf-234">**CLSID \_ MediaMultiplexerCategory**</span><span class="sxs-lookup"><span data-stu-id="07cdf-234">**CLSID\_MediaMultiplexerCategory**</span></span> | <span data-ttu-id="07cdf-235">**MÉRITO \_ \_ no se \_ usa**</span><span class="sxs-lookup"><span data-stu-id="07cdf-235">**MERIT\_DO\_NOT\_USE**</span></span> |



 

## <a name="directshow-filter-meta-category"></a><span data-ttu-id="07cdf-236">Meta-Category de filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="07cdf-236">DirectShow Filter Meta-Category</span></span>



| <span data-ttu-id="07cdf-237">Nombre descriptivo</span><span class="sxs-lookup"><span data-stu-id="07cdf-237">Friendly Name</span></span>                 | <span data-ttu-id="07cdf-238">CLSID</span><span class="sxs-lookup"><span data-stu-id="07cdf-238">CLSID</span></span>                            | <span data-ttu-id="07cdf-239">Fundament</span><span class="sxs-lookup"><span data-stu-id="07cdf-239">Merit</span></span>          |
|-------------------------------|----------------------------------|----------------|
| <span data-ttu-id="07cdf-240">Categorías de filtro de ActiveMovie</span><span class="sxs-lookup"><span data-stu-id="07cdf-240">ActiveMovie Filter Categories</span></span> | <span data-ttu-id="07cdf-241">**CLSID \_ ActiveMovieCategories**</span><span class="sxs-lookup"><span data-stu-id="07cdf-241">**CLSID\_ActiveMovieCategories**</span></span> | <span data-ttu-id="07cdf-242">No aplicable</span><span class="sxs-lookup"><span data-stu-id="07cdf-242">Not applicable</span></span> |



 

<span data-ttu-id="07cdf-243">Esta metacategoría contiene una lista de categorías de filtro.</span><span class="sxs-lookup"><span data-stu-id="07cdf-243">This meta-category contains a list of filter categories.</span></span> <span data-ttu-id="07cdf-244">Si una categoría de filtro no aparece en esta lista, el [asignador de filtros](filter-mapper.md) omite la categoría, lo que significa que el filtro no está disponible para la [conexión inteligente](intelligent-connect.md).</span><span class="sxs-lookup"><span data-stu-id="07cdf-244">If a filter category does not appear within this list, the [Filter Mapper](filter-mapper.md) ignores the category, which means the filter is not available for [Intelligent Connect](intelligent-connect.md).</span></span>

<span data-ttu-id="07cdf-245">Para enumerar la lista de categorías de filtro, llame a [**ICreateDevEnum:: CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) con el valor CLSID \_ ActiveMovieCategories.</span><span class="sxs-lookup"><span data-stu-id="07cdf-245">To enumerate the list of filter categories, call [**ICreateDevEnum::CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) with the value CLSID\_ActiveMovieCategories.</span></span> <span data-ttu-id="07cdf-246">Los monikers devueltos por este método admiten las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="07cdf-246">The monikers returned by this method support the following properties.</span></span>



| <span data-ttu-id="07cdf-247">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="07cdf-247">Property Name</span></span>  | <span data-ttu-id="07cdf-248">Descripción</span><span class="sxs-lookup"><span data-stu-id="07cdf-248">Description</span></span>                                                                            |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="07cdf-249">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="07cdf-249">"FriendlyName"</span></span> | <span data-ttu-id="07cdf-250">Nombre de categoría (VT \_ BSTR).</span><span class="sxs-lookup"><span data-stu-id="07cdf-250">Category name (VT\_BSTR).</span></span>                                                              |
| <span data-ttu-id="07cdf-251">Fundament</span><span class="sxs-lookup"><span data-stu-id="07cdf-251">"Merit"</span></span>        | <span data-ttu-id="07cdf-252">Mérito de categoría (VT \_ I4).</span><span class="sxs-lookup"><span data-stu-id="07cdf-252">Category merit (VT\_I4).</span></span> <span data-ttu-id="07cdf-253">Si esta propiedad está ausente, trate como **mérito \_ \_ no \_ usar**.</span><span class="sxs-lookup"><span data-stu-id="07cdf-253">If this property is absent, treat as **MERIT\_DO\_NOT\_USE**.</span></span> |
| <span data-ttu-id="07cdf-254">CLSID</span><span class="sxs-lookup"><span data-stu-id="07cdf-254">"CLSID"</span></span>        | <span data-ttu-id="07cdf-255">Categoría CLSID (VT \_ BSTR).</span><span class="sxs-lookup"><span data-stu-id="07cdf-255">Category CLSID (VT\_BSTR).</span></span>                                                             |



 

<span data-ttu-id="07cdf-256">Para agregar una nueva categoría de filtro a esta lista, llame a [**IFilterMapper2:: CreateCategory**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-createcategory).</span><span class="sxs-lookup"><span data-stu-id="07cdf-256">To add a new filter category to this list, call [**IFilterMapper2::CreateCategory**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-createcategory).</span></span>

## <a name="dmo-categories"></a><span data-ttu-id="07cdf-257">Categorías de DMO</span><span class="sxs-lookup"><span data-stu-id="07cdf-257">DMO Categories</span></span>

<span data-ttu-id="07cdf-258">Los objetos multimedia de DirectX (DMOs) usan un mecanismo de enumeración diferente de los filtros de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="07cdf-258">DirectX Media Objects (DMOs) use a different enumeration mechanism from DirectShow filters.</span></span> <span data-ttu-id="07cdf-259">Para obtener más información, consulte [registrar un DMO](registering-a-dmo.md).</span><span class="sxs-lookup"><span data-stu-id="07cdf-259">For more information, see [Registering a DMO](registering-a-dmo.md).</span></span> <span data-ttu-id="07cdf-260">Sin embargo, puede usar el enumerador de dispositivos del sistema para enumerar las categorías de DMO.</span><span class="sxs-lookup"><span data-stu-id="07cdf-260">However, you can use the System Device Enumerator to enumerate DMO categories.</span></span> <span data-ttu-id="07cdf-261">Los monikers se enlazan al [filtro de contenedor de DMO](dmo-wrapper-filter.md) e inicializan automáticamente el filtro con DMO.</span><span class="sxs-lookup"><span data-stu-id="07cdf-261">The monikers bind to the [DMO Wrapper Filter](dmo-wrapper-filter.md) and automatically initialize the filter with the DMO.</span></span>

<span data-ttu-id="07cdf-262">Además, algunas de las categorías de DMO se asignan a las categorías de filtro de DirectShow para la conexión inteligente:</span><span class="sxs-lookup"><span data-stu-id="07cdf-262">In addition, some of the DMO categories are mapped to DirectShow filter categories for the purposes of intelligent connect:</span></span>



| <span data-ttu-id="07cdf-263">Categoría de DMO</span><span class="sxs-lookup"><span data-stu-id="07cdf-263">DMO Category</span></span>                    | <span data-ttu-id="07cdf-264">Equivalente de DirectShow</span><span class="sxs-lookup"><span data-stu-id="07cdf-264">DirectShow Equivalent</span></span>              |
|---------------------------------|------------------------------------|
| <span data-ttu-id="07cdf-265">**\_codificador de audio DMOCATEGORY \_**</span><span class="sxs-lookup"><span data-stu-id="07cdf-265">**DMOCATEGORY\_AUDIO\_ENCODER**</span></span> | <span data-ttu-id="07cdf-266">**CLSID \_ AudioCompressorCategory**</span><span class="sxs-lookup"><span data-stu-id="07cdf-266">**CLSID\_AudioCompressorCategory**</span></span> |
| <span data-ttu-id="07cdf-267">**descodificador de audio de DMOCATEGORY \_ \_**</span><span class="sxs-lookup"><span data-stu-id="07cdf-267">**DMOCATEGORY\_AUDIO\_DECODER**</span></span> | <span data-ttu-id="07cdf-268">**CLSID \_ LegacyAmFilterCategory**</span><span class="sxs-lookup"><span data-stu-id="07cdf-268">**CLSID\_LegacyAmFilterCategory**</span></span>  |
| <span data-ttu-id="07cdf-269">**\_codificador de vídeo de DMOCATEGORY \_**</span><span class="sxs-lookup"><span data-stu-id="07cdf-269">**DMOCATEGORY\_VIDEO\_ENCODER**</span></span> | <span data-ttu-id="07cdf-270">**CLSID \_ VideoCompressorCategory**</span><span class="sxs-lookup"><span data-stu-id="07cdf-270">**CLSID\_VideoCompressorCategory**</span></span> |
| <span data-ttu-id="07cdf-271">**descodificador de vídeo de DMOCATEGORY \_ \_**</span><span class="sxs-lookup"><span data-stu-id="07cdf-271">**DMOCATEGORY\_VIDEO\_DECODER**</span></span> | <span data-ttu-id="07cdf-272">**CLSID \_ LegacyAmFilterCategory**</span><span class="sxs-lookup"><span data-stu-id="07cdf-272">**CLSID\_LegacyAmFilterCategory**</span></span>  |



 

<span data-ttu-id="07cdf-273">Tenga en cuenta que las categorías efecto de vídeo y efecto de audio no están asignadas a ninguna categoría de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="07cdf-273">Note that the video effect and audio effect categories are not mapped to any DirectShow categories.</span></span>

## <a name="related-topics"></a><span data-ttu-id="07cdf-274">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="07cdf-274">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07cdf-275">Constantes y GUID</span><span class="sxs-lookup"><span data-stu-id="07cdf-275">Constants and GUIDs</span></span>](constants-and-guids.md)
</dt> <dt>

[<span data-ttu-id="07cdf-276">Enumerar dispositivos y filtros</span><span class="sxs-lookup"><span data-stu-id="07cdf-276">Enumerating Devices and Filters</span></span>](enumerating-devices-and-filters.md)
</dt> <dt>

[<span data-ttu-id="07cdf-277">Conexión inteligente</span><span class="sxs-lookup"><span data-stu-id="07cdf-277">Intelligent Connect</span></span>](intelligent-connect.md)
</dt> <dt>

[<span data-ttu-id="07cdf-278">Diseño de las claves del registro</span><span class="sxs-lookup"><span data-stu-id="07cdf-278">Layout of the Registry Keys</span></span>](layout-of-the-registry-keys.md)
</dt> <dt>

[<span data-ttu-id="07cdf-279">Usar el asignador de filtros</span><span class="sxs-lookup"><span data-stu-id="07cdf-279">Using the Filter Mapper</span></span>](using-the-filter-mapper.md)
</dt> <dt>

[<span data-ttu-id="07cdf-280">Usar el enumerador de dispositivos del sistema</span><span class="sxs-lookup"><span data-stu-id="07cdf-280">Using the System Device Enumerator</span></span>](using-the-system-device-enumerator.md)
</dt> </dl>

 

 




