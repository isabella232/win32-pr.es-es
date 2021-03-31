---
description: Con MFTrace, puede filtrar los resultados de seguimiento especificando una lista de palabras clave.
ms.assetid: e7c382cb-94ac-4f90-a3dd-32f94c538396
title: Palabras clave de MFTrace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6d18a91aede8692209b9d5b7a2759c460e44043
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155345"
---
# <a name="mftrace-keywords"></a><span data-ttu-id="8e776-103">Palabras clave de MFTrace</span><span class="sxs-lookup"><span data-stu-id="8e776-103">MFTrace Keywords</span></span>

<span data-ttu-id="8e776-104">Con [MFTrace](mftrace.md), puede filtrar los resultados de seguimiento especificando una lista de palabras clave.</span><span class="sxs-lookup"><span data-stu-id="8e776-104">Using [MFTrace](mftrace.md), you can filter the trace results by specifying a list of keywords.</span></span> <span data-ttu-id="8e776-105">En la línea de comandos, use el argumento de línea **de comandos-k** .</span><span class="sxs-lookup"><span data-stu-id="8e776-105">At the command line, use the **-k** command-line argument.</span></span> <span data-ttu-id="8e776-106">También puede especificar el elemento de [**palabra clave**](keyword.md) en el archivo de configuración.</span><span class="sxs-lookup"><span data-stu-id="8e776-106">Alternatively, specify the [**keyword**](keyword.md) element in the configuration file.</span></span> <span data-ttu-id="8e776-107">Para obtener más información, vea [usar MFTrace](using-mftrace.md).</span><span class="sxs-lookup"><span data-stu-id="8e776-107">For more information, see [Using MFTrace](using-mftrace.md).</span></span>

<span data-ttu-id="8e776-108">MFTrace admite las siguientes palabras clave.</span><span class="sxs-lookup"><span data-stu-id="8e776-108">MFTrace supports the following keywords.</span></span> <span data-ttu-id="8e776-109">La mayoría hace referencia a interfaces o exportaciones de biblioteca determinadas.</span><span class="sxs-lookup"><span data-stu-id="8e776-109">Most refer to particular interfaces or library exports.</span></span>

-   <span data-ttu-id="8e776-110">"All"</span><span class="sxs-lookup"><span data-stu-id="8e776-110">"All"</span></span>
-   <span data-ttu-id="8e776-111">Predeterminada</span><span class="sxs-lookup"><span data-stu-id="8e776-111">"Default"</span></span>
-   <span data-ttu-id="8e776-112">Desvíos</span><span class="sxs-lookup"><span data-stu-id="8e776-112">"Detours"</span></span>
-   <span data-ttu-id="8e776-113">"IFilterGraph"</span><span class="sxs-lookup"><span data-stu-id="8e776-113">"IFilterGraph"</span></span>
-   <span data-ttu-id="8e776-114">"IGraphBuilder"</span><span class="sxs-lookup"><span data-stu-id="8e776-114">"IGraphBuilder"</span></span>
-   <span data-ttu-id="8e776-115">IMediaControl</span><span class="sxs-lookup"><span data-stu-id="8e776-115">"IMediaControl"</span></span>
-   <span data-ttu-id="8e776-116">"IMediaObject"</span><span class="sxs-lookup"><span data-stu-id="8e776-116">"IMediaObject"</span></span>
-   <span data-ttu-id="8e776-117">"IMemInputPin"</span><span class="sxs-lookup"><span data-stu-id="8e776-117">"IMemInputPin"</span></span>
-   <span data-ttu-id="8e776-118">"IMFActivate"</span><span class="sxs-lookup"><span data-stu-id="8e776-118">"IMFActivate"</span></span>
-   <span data-ttu-id="8e776-119">"IMFAttributes"</span><span class="sxs-lookup"><span data-stu-id="8e776-119">"IMFAttributes"</span></span>
-   <span data-ttu-id="8e776-120">"IMFByteStream"</span><span class="sxs-lookup"><span data-stu-id="8e776-120">"IMFByteStream"</span></span>
-   <span data-ttu-id="8e776-121">"IMFByteStreamHandler"</span><span class="sxs-lookup"><span data-stu-id="8e776-121">"IMFByteStreamHandler"</span></span>
-   <span data-ttu-id="8e776-122">"IMFClock"</span><span class="sxs-lookup"><span data-stu-id="8e776-122">"IMFClock"</span></span>
-   <span data-ttu-id="8e776-123">"IMFMediaEventGenerator"</span><span class="sxs-lookup"><span data-stu-id="8e776-123">"IMFMediaEventGenerator"</span></span>
-   <span data-ttu-id="8e776-124">"IMFMediaSession"</span><span class="sxs-lookup"><span data-stu-id="8e776-124">"IMFMediaSession"</span></span>
-   <span data-ttu-id="8e776-125">"IMFMediaSink"</span><span class="sxs-lookup"><span data-stu-id="8e776-125">"IMFMediaSink"</span></span>
-   <span data-ttu-id="8e776-126">"IMFMediaSource"</span><span class="sxs-lookup"><span data-stu-id="8e776-126">"IMFMediaSource"</span></span>
-   <span data-ttu-id="8e776-127">"IMFMediaStream"</span><span class="sxs-lookup"><span data-stu-id="8e776-127">"IMFMediaStream"</span></span>
-   <span data-ttu-id="8e776-128">"IMFPMediaItem"</span><span class="sxs-lookup"><span data-stu-id="8e776-128">"IMFPMediaItem"</span></span>
-   <span data-ttu-id="8e776-129">"IMFPMediaPlayer"</span><span class="sxs-lookup"><span data-stu-id="8e776-129">"IMFPMediaPlayer"</span></span>
-   <span data-ttu-id="8e776-130">"IMFPMediaPlayerCallback"</span><span class="sxs-lookup"><span data-stu-id="8e776-130">"IMFPMediaPlayerCallback"</span></span>
-   <span data-ttu-id="8e776-131">"IMFPresentationClock"</span><span class="sxs-lookup"><span data-stu-id="8e776-131">"IMFPresentationClock"</span></span>
-   <span data-ttu-id="8e776-132">"IMFQualityAdvise"</span><span class="sxs-lookup"><span data-stu-id="8e776-132">"IMFQualityAdvise"</span></span>
-   <span data-ttu-id="8e776-133">"IMFQualityAdvise2"</span><span class="sxs-lookup"><span data-stu-id="8e776-133">"IMFQualityAdvise2"</span></span>
-   <span data-ttu-id="8e776-134">"IMFQualityManager"</span><span class="sxs-lookup"><span data-stu-id="8e776-134">"IMFQualityManager"</span></span>
-   <span data-ttu-id="8e776-135">"IMFReadWriteClassFactory"</span><span class="sxs-lookup"><span data-stu-id="8e776-135">"IMFReadWriteClassFactory"</span></span>
-   <span data-ttu-id="8e776-136">"IMFSample"</span><span class="sxs-lookup"><span data-stu-id="8e776-136">"IMFSample"</span></span>
-   <span data-ttu-id="8e776-137">"IMFSchemeHandler"</span><span class="sxs-lookup"><span data-stu-id="8e776-137">"IMFSchemeHandler"</span></span>
-   <span data-ttu-id="8e776-138">"IMFSinkWriter"</span><span class="sxs-lookup"><span data-stu-id="8e776-138">"IMFSinkWriter"</span></span>
-   <span data-ttu-id="8e776-139">"IMFSourceReader"</span><span class="sxs-lookup"><span data-stu-id="8e776-139">"IMFSourceReader"</span></span>
-   <span data-ttu-id="8e776-140">"IMFSourceReaderCallback"</span><span class="sxs-lookup"><span data-stu-id="8e776-140">"IMFSourceReaderCallback"</span></span>
-   <span data-ttu-id="8e776-141">"IMFSourceResolver"</span><span class="sxs-lookup"><span data-stu-id="8e776-141">"IMFSourceResolver"</span></span>
-   <span data-ttu-id="8e776-142">"IMFStreamSink"</span><span class="sxs-lookup"><span data-stu-id="8e776-142">"IMFStreamSink"</span></span>
-   <span data-ttu-id="8e776-143">"IMFTopoLoader"</span><span class="sxs-lookup"><span data-stu-id="8e776-143">"IMFTopoLoader"</span></span>
-   <span data-ttu-id="8e776-144">"IMFTopology"</span><span class="sxs-lookup"><span data-stu-id="8e776-144">"IMFTopology"</span></span>
-   <span data-ttu-id="8e776-145">"IMFTopologyNode"</span><span class="sxs-lookup"><span data-stu-id="8e776-145">"IMFTopologyNode"</span></span>
-   <span data-ttu-id="8e776-146">"IMFTransform"</span><span class="sxs-lookup"><span data-stu-id="8e776-146">"IMFTransform"</span></span>
-   <span data-ttu-id="8e776-147">"IWMReader"</span><span class="sxs-lookup"><span data-stu-id="8e776-147">"IWMReader"</span></span>
-   <span data-ttu-id="8e776-148">"Kernel32Export"</span><span class="sxs-lookup"><span data-stu-id="8e776-148">"Kernel32Export"</span></span>
-   <span data-ttu-id="8e776-149">"MFExport"</span><span class="sxs-lookup"><span data-stu-id="8e776-149">"MFExport"</span></span>
-   <span data-ttu-id="8e776-150">"MFPlatExport"</span><span class="sxs-lookup"><span data-stu-id="8e776-150">"MFPlatExport"</span></span>
-   <span data-ttu-id="8e776-151">"MFPlayExport"</span><span class="sxs-lookup"><span data-stu-id="8e776-151">"MFPlayExport"</span></span>
-   <span data-ttu-id="8e776-152">"MFPublic"</span><span class="sxs-lookup"><span data-stu-id="8e776-152">"MFPublic"</span></span>
-   <span data-ttu-id="8e776-153">"MFReadWriteExport"</span><span class="sxs-lookup"><span data-stu-id="8e776-153">"MFReadWriteExport"</span></span>
-   <span data-ttu-id="8e776-154">"Ole32Export"</span><span class="sxs-lookup"><span data-stu-id="8e776-154">"Ole32Export"</span></span>
-   <span data-ttu-id="8e776-155">"wmvCoreExport"</span><span class="sxs-lookup"><span data-stu-id="8e776-155">"wmvCoreExport"</span></span>

## <a name="related-topics"></a><span data-ttu-id="8e776-156">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8e776-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8e776-157">MFTrace</span><span class="sxs-lookup"><span data-stu-id="8e776-157">MFTrace</span></span>](mftrace.md)
</dt> <dt>

[<span data-ttu-id="8e776-158">Usar MFTrace</span><span class="sxs-lookup"><span data-stu-id="8e776-158">Using MFTrace</span></span>](using-mftrace.md)
</dt> </dl>

 

 



