---
description: En esta sección se describe cómo escribir una transformación de Media Foundation personalizada (MFT).
ms.assetid: a95828d3-afc5-4f6b-aedd-5b6a72621e0e
title: Escribir una MFT personalizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d15b9d5ae655ba67d4a526aeb8a82eb9d3912da9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910189"
---
# <a name="writing-a-custom-mft"></a><span data-ttu-id="51b6c-103">Escribir una MFT personalizada</span><span class="sxs-lookup"><span data-stu-id="51b6c-103">Writing a Custom MFT</span></span>

<span data-ttu-id="51b6c-104">En esta sección se describe cómo escribir una transformación de Media Foundation personalizada (MFT).</span><span class="sxs-lookup"><span data-stu-id="51b6c-104">This section describes how to write a custom Media Foundation Transform (MFT).</span></span>

## <a name="mft-checklist"></a><span data-ttu-id="51b6c-105">Lista de comprobación de MFT</span><span class="sxs-lookup"><span data-stu-id="51b6c-105">MFT Checklist</span></span>

<span data-ttu-id="51b6c-106">Cuando implemente un MFT personalizado, use la siguiente lista de comprobación para determinar los requisitos:</span><span class="sxs-lookup"><span data-stu-id="51b6c-106">When you implement a custom MFT, use the following checklist to determine the requirements:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="51b6c-107">Todos los MFTs</span><span class="sxs-lookup"><span data-stu-id="51b6c-107">All MFTs</span></span></td>
<td><span data-ttu-id="51b6c-108">Todos los MFTs deben implementar <a href="/windows/desktop/api/mftransform/nn-mftransform-imftransform"><strong>IMFTransform</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="51b6c-108">All MFTs must implement <a href="/windows/desktop/api/mftransform/nn-mftransform-imftransform"><strong>IMFTransform</strong></a>.</span></span><br/> <span data-ttu-id="51b6c-109">En los temas siguientes se proporciona más información acerca de la implementación de esta interfaz:</span><span class="sxs-lookup"><span data-stu-id="51b6c-109">The following topics give more information about implementing this interface:</span></span>
<ul>
<li><span data-ttu-id="51b6c-110"><a href="basic-mft-processing-model.md">Modelo básico de procesamiento de MFT</a></span><span class="sxs-lookup"><span data-stu-id="51b6c-110"><a href="basic-mft-processing-model.md">Basic MFT Processing Model</a></span></span></li>
<li><span data-ttu-id="51b6c-111"><a href="time-stamps-and-durations.md">Marcas de tiempo y duraciones</a></span><span class="sxs-lookup"><span data-stu-id="51b6c-111"><a href="time-stamps-and-durations.md">Time Stamps and Durations</a></span></span></li>
<li><span data-ttu-id="51b6c-112"><a href="handling-stream-changes.md">Control de los cambios de flujo</a></span><span class="sxs-lookup"><span data-stu-id="51b6c-112"><a href="handling-stream-changes.md">Handling Stream Changes</a></span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="51b6c-113">Codificadores y descodificadores</span><span class="sxs-lookup"><span data-stu-id="51b6c-113">Encoders and decoders</span></span></td>
<td><span data-ttu-id="51b6c-114">Requisitos: vea <a href="implementing-a-codec-mft.md">implementación de un MFT de códec</a>.</span><span class="sxs-lookup"><span data-stu-id="51b6c-114">Requirements: See <a href="implementing-a-codec-mft.md">Implementing a Codec MFT</a>.</span></span><br/> <span data-ttu-id="51b6c-115">Recomendado: implemente <a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise"><strong>IMFQualityAdvise</strong></a> o <a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2"><strong>IMFQualityAdvise2</strong></a>para admitir notificaciones de calidad de servicio (QoS).</span><span class="sxs-lookup"><span data-stu-id="51b6c-115">Recommended: Implement <a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise"><strong>IMFQualityAdvise</strong></a> or <a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2"><strong>IMFQualityAdvise2</strong></a>, to support quality-of-service (QoS) notifications.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="51b6c-116">Descodificadores de vídeo y procesadores de vídeo</span><span class="sxs-lookup"><span data-stu-id="51b6c-116">Video decoders and video processors</span></span></td>
<td><span data-ttu-id="51b6c-117">Opcional: compatibilidad con la aceleración de vídeo de DirectX.</span><span class="sxs-lookup"><span data-stu-id="51b6c-117">Optional: Support DirectX Video Acceleration.</span></span><br/>
<ul>
<li><span data-ttu-id="51b6c-118"><a href="direct3d-aware-mfts.md">MFTs compatible con Direct3D</a></span><span class="sxs-lookup"><span data-stu-id="51b6c-118"><a href="direct3d-aware-mfts.md">Direct3D-Aware MFTs</a></span></span></li>
<li><span data-ttu-id="51b6c-119"><a href="supporting-dxva-2-0-in-media-foundation.md">Compatibilidad con DXVA 2,0 en Media Foundation</a></span><span class="sxs-lookup"><span data-stu-id="51b6c-119"><a href="supporting-dxva-2-0-in-media-foundation.md">Supporting DXVA 2.0 in Media Foundation</a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="51b6c-120">Códecs de hardware</span><span class="sxs-lookup"><span data-stu-id="51b6c-120">Hardware codecs</span></span></td>
<td><span data-ttu-id="51b6c-121">Consulte <a href="hardware-mfts.md">hardware MFTs</a>.</span><span class="sxs-lookup"><span data-stu-id="51b6c-121">See <a href="hardware-mfts.md">Hardware MFTs</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="51b6c-122">Para que las aplicaciones puedan detectar su MFT...</span><span class="sxs-lookup"><span data-stu-id="51b6c-122">To make your MFT discoverable by applications...</span></span></td>
<td><span data-ttu-id="51b6c-123">Consulte <a href="registering-and-enumerating-mfts.md">registro y enumeración de MFTs</a>.</span><span class="sxs-lookup"><span data-stu-id="51b6c-123">See <a href="registering-and-enumerating-mfts.md">Registering and Enumerating MFTs</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="51b6c-124">Procesamiento de datos asincrónicos</span><span class="sxs-lookup"><span data-stu-id="51b6c-124">Asynchronous data processing</span></span></td>
<td><span data-ttu-id="51b6c-125">El modelo de MFT predeterminado usa llamadas sincrónicas (bloqueo) para procesar los datos.</span><span class="sxs-lookup"><span data-stu-id="51b6c-125">The default MFT model uses synchronous (blocking) calls to process data.</span></span> <span data-ttu-id="51b6c-126">En algunos MFTs, el procesamiento asincrónico puede ser más eficaz.</span><span class="sxs-lookup"><span data-stu-id="51b6c-126">For some MFTs, asynchronous processing can be more efficient.</span></span> <span data-ttu-id="51b6c-127">Sin embargo, también es más difícil de implementar.</span><span class="sxs-lookup"><span data-stu-id="51b6c-127">However, it is also more complex to implement.</span></span><br/> <span data-ttu-id="51b6c-128">Para obtener más información, consulte <a href="asynchronous-mfts.md">MFTs asincrónico</a>.</span><span class="sxs-lookup"><span data-stu-id="51b6c-128">For more information, see <a href="asynchronous-mfts.md">Asynchronous MFTs</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="51b6c-129">Control de velocidad, modo de truco o reproducción inversa</span><span class="sxs-lookup"><span data-stu-id="51b6c-129">Rate control, trick mode, or reverse playback</span></span></td>
<td><span data-ttu-id="51b6c-130">Vea <a href="implementing-rate-control.md">implementar el control de tasa</a>.</span><span class="sxs-lookup"><span data-stu-id="51b6c-130">See <a href="implementing-rate-control.md">Implementing Rate Control</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="51b6c-131">Si su MFT crea subprocesos...</span><span class="sxs-lookup"><span data-stu-id="51b6c-131">If your MFT creates threads...</span></span></td>
<td><span data-ttu-id="51b6c-132">Implemente la interfaz <a href="/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient"><strong>IMFRealTimeClient</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="51b6c-132">Implement the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient"><strong>IMFRealTimeClient</strong></a> interface.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="51b6c-133">Si su MFT tiene restricciones de licencia...</span><span class="sxs-lookup"><span data-stu-id="51b6c-133">If your MFT has licensing restrictions...</span></span></td>
<td><span data-ttu-id="51b6c-134">Considere la posibilidad de usar el mecanismo de campo de uso.</span><span class="sxs-lookup"><span data-stu-id="51b6c-134">Consider using the field-of-use mechanism.</span></span> <span data-ttu-id="51b6c-135">Vea el <a href="field-of-use-restrictions.md">campo de restricciones de uso</a>.</span><span class="sxs-lookup"><span data-stu-id="51b6c-135">See <a href="field-of-use-restrictions.md">Field of Use Restrictions</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="51b6c-136">Si va a migrar un objeto multimedia de DirectX existente (DMO)...</span><span class="sxs-lookup"><span data-stu-id="51b6c-136">If you are porting an existing DirectX Media Object (DMO)...</span></span></td>
<td><span data-ttu-id="51b6c-137">Vea <a href="comparison-of-mfts-and-dmos.md">comparación de MFTs y DMOs</a>.</span><span class="sxs-lookup"><span data-stu-id="51b6c-137">See <a href="comparison-of-mfts-and-dmos.md">Comparison of MFTs and DMOs</a>.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="51b6c-138">Esta sección contiene los siguientes temas:</span><span class="sxs-lookup"><span data-stu-id="51b6c-138">This section contains the following topics:</span></span>

-   [<span data-ttu-id="51b6c-139">Marcas de tiempo y duraciones</span><span class="sxs-lookup"><span data-stu-id="51b6c-139">Time Stamps and Durations</span></span>](time-stamps-and-durations.md)
-   [<span data-ttu-id="51b6c-140">Control de los cambios de flujo</span><span class="sxs-lookup"><span data-stu-id="51b6c-140">Handling Stream Changes</span></span>](handling-stream-changes.md)
-   [<span data-ttu-id="51b6c-141">Implementar un MFT de códec</span><span class="sxs-lookup"><span data-stu-id="51b6c-141">Implementing a Codec MFT</span></span>](implementing-a-codec-mft.md)
-   [<span data-ttu-id="51b6c-142">MFTs compatible con Direct3D</span><span class="sxs-lookup"><span data-stu-id="51b6c-142">Direct3D-Aware MFTs</span></span>](direct3d-aware-mfts.md)
-   [<span data-ttu-id="51b6c-143">MFTs de hardware</span><span class="sxs-lookup"><span data-stu-id="51b6c-143">Hardware MFTs</span></span>](hardware-mfts.md)
-   [<span data-ttu-id="51b6c-144">Mérito del códec</span><span class="sxs-lookup"><span data-stu-id="51b6c-144">Codec Merit</span></span>](codec-merit.md)

## <a name="related-topics"></a><span data-ttu-id="51b6c-145">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="51b6c-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="51b6c-146">Media Foundation transformaciones</span><span class="sxs-lookup"><span data-stu-id="51b6c-146">Media Foundation Transforms</span></span>](media-foundation-transforms.md)
</dt> </dl>

 

 




