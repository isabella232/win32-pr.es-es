---
description: Muestra cómo obtener una vista previa de vídeo desde un dispositivo de captura de vídeo mediante la API de MFPlay.
ms.assetid: 6e2b1636-9d24-40e6-9ed4-e17d1af6a044
title: Ejemplo de SimpleCapture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da6fd255ad4c69254eb6ff64bdb99731e0c5ba9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275812"
---
# <a name="simplecapture-sample"></a><span data-ttu-id="7b361-103">Ejemplo de SimpleCapture</span><span class="sxs-lookup"><span data-stu-id="7b361-103">SimpleCapture Sample</span></span>

<span data-ttu-id="7b361-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="7b361-104">\[Deprecated.</span></span> <span data-ttu-id="7b361-105">La API de MFPlay se puede quitar de las versiones futuras de Windows.</span><span class="sxs-lookup"><span data-stu-id="7b361-105">The MFPlay API may be removed from future releases of Windows.</span></span> <span data-ttu-id="7b361-106">Las aplicaciones deben usar el [lector de origen](source-reader.md) para la captura de vídeo.\]</span><span class="sxs-lookup"><span data-stu-id="7b361-106">Applications should use the [Source Reader](source-reader.md) for video capture.\]</span></span>

<span data-ttu-id="7b361-107">Muestra cómo obtener una vista previa de vídeo desde un dispositivo de captura de vídeo mediante la API de MFPlay.</span><span class="sxs-lookup"><span data-stu-id="7b361-107">Shows how to preview video from a video capture device, using the MFPlay API.</span></span>

## <a name="apis-demonstrated"></a><span data-ttu-id="7b361-108">API mostradas</span><span class="sxs-lookup"><span data-stu-id="7b361-108">APIs Demonstrated</span></span>

<span data-ttu-id="7b361-109">Este ejemplo muestra las siguientes interfaces de Microsoft Media Foundation:</span><span class="sxs-lookup"><span data-stu-id="7b361-109">This sample demonstrates the following Microsoft Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="7b361-110">**IMFMediaSource**</span><span class="sxs-lookup"><span data-stu-id="7b361-110">**IMFMediaSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)
-   [<span data-ttu-id="7b361-111">**IMFPMediaItem**</span><span class="sxs-lookup"><span data-stu-id="7b361-111">**IMFPMediaItem**</span></span>](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem)
-   [<span data-ttu-id="7b361-112">**IMFPMediaPlayer**</span><span class="sxs-lookup"><span data-stu-id="7b361-112">**IMFPMediaPlayer**</span></span>](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer)
-   [<span data-ttu-id="7b361-113">**IMFPMediaPlayerCallback**</span><span class="sxs-lookup"><span data-stu-id="7b361-113">**IMFPMediaPlayerCallback**</span></span>](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback)

## <a name="requirements"></a><span data-ttu-id="7b361-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7b361-114">Requirements</span></span>



| <span data-ttu-id="7b361-115">Producto</span><span class="sxs-lookup"><span data-stu-id="7b361-115">Product</span></span>                                                        | <span data-ttu-id="7b361-116">Versión</span><span class="sxs-lookup"><span data-stu-id="7b361-116">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="7b361-117">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="7b361-117">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="7b361-118">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7b361-118">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="7b361-119">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="7b361-119">Downloading the Sample</span></span>

<span data-ttu-id="7b361-120">Este ejemplo está disponible en el [repositorio de github de ejemplos de Windows clásico](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/SimpleCapture).</span><span class="sxs-lookup"><span data-stu-id="7b361-120">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/SimpleCapture).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7b361-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7b361-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b361-122">Captura de audio y vídeo</span><span class="sxs-lookup"><span data-stu-id="7b361-122">Audio/Video Capture</span></span>](audio-video-capture.md)
</dt> <dt>

[<span data-ttu-id="7b361-123">Muestras de SDK de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7b361-123">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> </dl>

 

 



