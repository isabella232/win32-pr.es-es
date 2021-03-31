---
description: El origen de archivo MP3 analiza los archivos MP3.
ms.assetid: 37362642-1b8a-4fb3-950d-ed1afe3696e5
title: Origen de archivo MP3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2241e3b99d5a1918be8ff0182a9eca8939c12ce2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155344"
---
# <a name="mp3-file-source"></a><span data-ttu-id="9dfea-103">Origen de archivo MP3</span><span class="sxs-lookup"><span data-stu-id="9dfea-103">MP3 File Source</span></span>

<span data-ttu-id="9dfea-104">El origen de archivo MP3 analiza los archivos MP3.</span><span class="sxs-lookup"><span data-stu-id="9dfea-104">The MP3 file source parses MP3 files.</span></span>

<span data-ttu-id="9dfea-105">El origen de archivo MP3 genera búferes que contienen fotogramas de audio MPEG-1.</span><span class="sxs-lookup"><span data-stu-id="9dfea-105">The MP3 file source outputs buffers that contain MPEG-1 audio frames.</span></span> <span data-ttu-id="9dfea-106">No descodifica el audio.</span><span class="sxs-lookup"><span data-stu-id="9dfea-106">It does not decode the audio.</span></span>

## <a name="file-extensions-and-mime-types"></a><span data-ttu-id="9dfea-107">Extensiones de archivo y tipos MIME</span><span class="sxs-lookup"><span data-stu-id="9dfea-107">File Extensions and MIME Types</span></span>

<span data-ttu-id="9dfea-108">El origen de archivo MP3 es el origen de medios predeterminado para la siguiente extensión de nombre de archivo:</span><span class="sxs-lookup"><span data-stu-id="9dfea-108">The MP3 file source is the default media source for the following file name extension:</span></span>

-   <span data-ttu-id="9dfea-109">.mp3</span><span class="sxs-lookup"><span data-stu-id="9dfea-109">.mp3</span></span>

<span data-ttu-id="9dfea-110">También es el origen de medios predeterminado para los siguientes tipos MIME.</span><span class="sxs-lookup"><span data-stu-id="9dfea-110">It is also the default media source for the following MIME types.</span></span>

-   <span data-ttu-id="9dfea-111">audio/MPEG</span><span class="sxs-lookup"><span data-stu-id="9dfea-111">audio/mpeg</span></span>
-   <span data-ttu-id="9dfea-112">audio/x-mp3</span><span class="sxs-lookup"><span data-stu-id="9dfea-112">audio/x-mp3</span></span>
-   <span data-ttu-id="9dfea-113">audio/x-MPEG</span><span class="sxs-lookup"><span data-stu-id="9dfea-113">audio/x-mpeg</span></span>

## <a name="media-types"></a><span data-ttu-id="9dfea-114">Tipos de medios</span><span class="sxs-lookup"><span data-stu-id="9dfea-114">Media Types</span></span>

<span data-ttu-id="9dfea-115">El tipo de medio que ofrece el origen de archivos MP3 contiene los siguientes atributos.</span><span class="sxs-lookup"><span data-stu-id="9dfea-115">The media type offered by the MP3 file source contains the following attributes.</span></span>



| <span data-ttu-id="9dfea-116">Atributo</span><span class="sxs-lookup"><span data-stu-id="9dfea-116">Attribute</span></span>                                                                                    | <span data-ttu-id="9dfea-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="9dfea-117">Description</span></span>                                                                                                                                        |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9dfea-118">**\_ \_ tipo principal MF \_ MT**</span><span class="sxs-lookup"><span data-stu-id="9dfea-118">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md)                                    | <span data-ttu-id="9dfea-119">Igual a **MFMediaType \_ audio**.</span><span class="sxs-lookup"><span data-stu-id="9dfea-119">Equal to **MFMediaType\_Audio**.</span></span>                                                                                                                   |
| [<span data-ttu-id="9dfea-120">**subtipo MF \_ MT \_**</span><span class="sxs-lookup"><span data-stu-id="9dfea-120">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)                                           | <span data-ttu-id="9dfea-121">Igual a **MFAudioFormat \_ mp3** o **MFAudioFormat \_ MPEG**.</span><span class="sxs-lookup"><span data-stu-id="9dfea-121">Equal to **MFAudioFormat\_MP3** or **MFAudioFormat\_MPEG**.</span></span>                                                                                        |
| [<span data-ttu-id="9dfea-122">**\_promedio de \_ bytes de audio MF MT \_ \_ \_ por \_ segundo**</span><span class="sxs-lookup"><span data-stu-id="9dfea-122">**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md) | <span data-ttu-id="9dfea-123">Número promedio de bytes por segundo.</span><span class="sxs-lookup"><span data-stu-id="9dfea-123">Average number of bytes per second.</span></span>                                                                                                                |
| [<span data-ttu-id="9dfea-124">**\_alineación del \_ bloque de audio MF MT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9dfea-124">**MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT**</span></span>](mf-mt-audio-block-alignment-attribute.md)             | <span data-ttu-id="9dfea-125">Igual a 1.</span><span class="sxs-lookup"><span data-stu-id="9dfea-125">Equal to 1.</span></span>                                                                                                                                        |
| [<span data-ttu-id="9dfea-126">**\_canales de \_ número de audio MF MT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9dfea-126">**MF\_MT\_AUDIO\_NUM\_CHANNELS**</span></span>](mf-mt-audio-num-channels-attribute.md)                   | <span data-ttu-id="9dfea-127">Número de canales de audio.</span><span class="sxs-lookup"><span data-stu-id="9dfea-127">Number of audio channels.</span></span>                                                                                                                          |
| [<span data-ttu-id="9dfea-128">**\_muestras de audio MF MT \_ \_ \_ por \_ segundo**</span><span class="sxs-lookup"><span data-stu-id="9dfea-128">**MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND**</span></span>](mf-mt-audio-samples-per-second-attribute.md)      | <span data-ttu-id="9dfea-129">Número de muestras de audio por segundo.</span><span class="sxs-lookup"><span data-stu-id="9dfea-129">Number of audio samples per second.</span></span>                                                                                                                |
| [<span data-ttu-id="9dfea-130">**datos de usuario de MF \_ MT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9dfea-130">**MF\_MT\_USER\_DATA**</span></span>](mf-mt-user-data-attribute.md)                                      | <span data-ttu-id="9dfea-131">Contiene la parte de una estructura [**MPEGLAYER3WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-mpeglayer3waveformat) que aparece después del miembro de **WFX** de la estructura.</span><span class="sxs-lookup"><span data-stu-id="9dfea-131">Contains the portion of a [**MPEGLAYER3WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-mpeglayer3waveformat) structure that appears after the **wfx** member of the structure.</span></span> |



 

## <a name="interfaces"></a><span data-ttu-id="9dfea-132">Interfaces</span><span class="sxs-lookup"><span data-stu-id="9dfea-132">Interfaces</span></span>

<span data-ttu-id="9dfea-133">El origen de archivo MP3 expone las siguientes interfaces a través de [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)):</span><span class="sxs-lookup"><span data-stu-id="9dfea-133">The MP3 file source exposes the following interfaces through [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)):</span></span>

-   [<span data-ttu-id="9dfea-134">**IMFGetService**</span><span class="sxs-lookup"><span data-stu-id="9dfea-134">**IMFGetService**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [<span data-ttu-id="9dfea-135">**IMFMediaEventGenerator**</span><span class="sxs-lookup"><span data-stu-id="9dfea-135">**IMFMediaEventGenerator**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)
-   [<span data-ttu-id="9dfea-136">**IMFMediaSource**</span><span class="sxs-lookup"><span data-stu-id="9dfea-136">**IMFMediaSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)

<span data-ttu-id="9dfea-137">Además, expone las siguientes interfaces a través de [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice):</span><span class="sxs-lookup"><span data-stu-id="9dfea-137">In addition, it exposes the following interfaces through [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice):</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9dfea-138">GUID de servicio</span><span class="sxs-lookup"><span data-stu-id="9dfea-138">Service GUID</span></span></th>
<th><span data-ttu-id="9dfea-139">Interfaz</span><span class="sxs-lookup"><span data-stu-id="9dfea-139">Interface</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9dfea-140"><strong>MF_METADATA_PROVIDER_SERVICE</strong></span><span class="sxs-lookup"><span data-stu-id="9dfea-140"><strong>MF_METADATA_PROVIDER_SERVICE</strong></span></span></td>
<td><span data-ttu-id="9dfea-141"><a href="/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider"><strong>IMFMetadataProvider</strong></a></span><span class="sxs-lookup"><span data-stu-id="9dfea-141"><a href="/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider"><strong>IMFMetadataProvider</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9dfea-142"><strong>MF_PROPERTY_HANDLER_SERVICE</strong></span><span class="sxs-lookup"><span data-stu-id="9dfea-142"><strong>MF_PROPERTY_HANDLER_SERVICE</strong></span></span></td>
<td><span data-ttu-id="9dfea-143"><a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>IPropertyStore</strong></a>
</span><span class="sxs-lookup"><span data-stu-id="9dfea-143"><a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>IPropertyStore</strong></a>
</span></span><blockquote>
[!Note]<br />
<span data-ttu-id="9dfea-144">Consulte <a href="shell-metadata-providers.md">proveedores de metadatos de Shell</a>.</span><span class="sxs-lookup"><span data-stu-id="9dfea-144">See <a href="shell-metadata-providers.md">Shell Metadata Providers</a>.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9dfea-145"><strong>MF_RATE_CONTROL_SERVICE</strong></span><span class="sxs-lookup"><span data-stu-id="9dfea-145"><strong>MF_RATE_CONTROL_SERVICE</strong></span></span></td>
<td><span data-ttu-id="9dfea-146"><a href="/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol"><strong>IMFRateControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="9dfea-146"><a href="/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol"><strong>IMFRateControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9dfea-147"><strong>MF_RATE_CONTROL_SERVICE</strong></span><span class="sxs-lookup"><span data-stu-id="9dfea-147"><strong>MF_RATE_CONTROL_SERVICE</strong></span></span></td>
<td><span data-ttu-id="9dfea-148"><a href="/windows/desktop/api/mfidl/nn-mfidl-imfratesupport"><strong>IMFRateSupport</strong></a></span><span class="sxs-lookup"><span data-stu-id="9dfea-148"><a href="/windows/desktop/api/mfidl/nn-mfidl-imfratesupport"><strong>IMFRateSupport</strong></a></span></span></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="9dfea-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9dfea-149">Requirements</span></span>



| <span data-ttu-id="9dfea-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="9dfea-150">Requirement</span></span> | <span data-ttu-id="9dfea-151">Value</span><span class="sxs-lookup"><span data-stu-id="9dfea-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="9dfea-152">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9dfea-152">Minimum supported client</span></span><br/> | <span data-ttu-id="9dfea-153">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="9dfea-153">Windows 7 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9dfea-154">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9dfea-154">Minimum supported server</span></span><br/> | <span data-ttu-id="9dfea-155">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="9dfea-155">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="9dfea-156">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9dfea-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9dfea-157"><dt>Mf.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9dfea-157"><dt>Mf.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9dfea-158">Vea también</span><span class="sxs-lookup"><span data-stu-id="9dfea-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9dfea-159">Orígenes y receptores de medios</span><span class="sxs-lookup"><span data-stu-id="9dfea-159">Media Sources and Sinks</span></span>](media-sources-and-sinks.md)
</dt> <dt>

[<span data-ttu-id="9dfea-160">Orígenes multimedia</span><span class="sxs-lookup"><span data-stu-id="9dfea-160">Media Sources</span></span>](media-sources.md)
</dt> <dt>

[<span data-ttu-id="9dfea-161">Solucionador de origen</span><span class="sxs-lookup"><span data-stu-id="9dfea-161">Source Resolver</span></span>](source-resolver.md)
</dt> <dt>

[<span data-ttu-id="9dfea-162">Formatos de medios admitidos en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9dfea-162">Supported Media Formats in Media Foundation</span></span>](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

 
