---
description: En esta sección se describe cómo implementar la reproducción de audio y vídeo en la aplicación mediante Microsoft Media Foundation.
ms.assetid: 6efadfe6-013a-4942-9df5-bed557d9af8b
title: Reproducción de audio y vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6781c531bc7e5c595125d5353a381cc44c08fd5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696184"
---
# <a name="audiovideo-playback"></a><span data-ttu-id="27dee-103">Reproducción de audio y vídeo</span><span class="sxs-lookup"><span data-stu-id="27dee-103">Audio/Video Playback</span></span>

<span data-ttu-id="27dee-104">En esta sección se describe cómo implementar la reproducción de audio y vídeo en la aplicación mediante Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="27dee-104">This section describes how to implement audio/video playback in your application, using Microsoft Media Foundation.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="27dee-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="27dee-105">In this section</span></span>



| <span data-ttu-id="27dee-106">Tema</span><span class="sxs-lookup"><span data-stu-id="27dee-106">Topic</span></span>                                                                                               | <span data-ttu-id="27dee-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="27dee-107">Description</span></span>                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="27dee-108">Cómo reproducir archivos multimedia con Media Foundation</span><span class="sxs-lookup"><span data-stu-id="27dee-108">How to Play Media Files with Media Foundation</span></span>](how-to-play-unprotected-media-files.md)<br/> | <span data-ttu-id="27dee-109">En este tutorial se muestra cómo reproducir archivos multimedia mediante el objeto de [sesión de medios](media-session.md) .</span><span class="sxs-lookup"><span data-stu-id="27dee-109">This tutorial shows how to play media files using the [Media Session](media-session.md) object.</span></span> <br/>                                 |
| [<span data-ttu-id="27dee-110">Cómo reproducir archivos multimedia protegidos</span><span class="sxs-lookup"><span data-stu-id="27dee-110">How to Play Protected Media Files</span></span>](how-to-play-protected-media-files.md)<br/>               | <span data-ttu-id="27dee-111">Cómo reproducir archivos que contienen medios protegidos con DRM.</span><span class="sxs-lookup"><span data-stu-id="27dee-111">How to play files that contain DRM-protected media.</span></span><br/>                                                                               |
| [<span data-ttu-id="27dee-112">Cómo buscar la duración de un archivo multimedia</span><span class="sxs-lookup"><span data-stu-id="27dee-112">How to Find the Duration of a Media File</span></span>](how-to-find-the-duration-of-a-media-file.md)<br/> | <span data-ttu-id="27dee-113">Cómo buscar la duración de un archivo multimedia.</span><span class="sxs-lookup"><span data-stu-id="27dee-113">How to find the duration of a media file.</span></span><br/>                                                                                         |
| [<span data-ttu-id="27dee-114">Búsqueda, avance rápido y reproducción inversa</span><span class="sxs-lookup"><span data-stu-id="27dee-114">Seeking, Fast Forward, and Reverse Play</span></span>](seeking--fast-forward--and-reverse-play.md)<br/>   | <span data-ttu-id="27dee-115">En este tema se muestra código de ejemplo para administrar los cambios de búsqueda y tasa cuando se usa la [sesión multimedia](media-session.md) para la reproducción.</span><span class="sxs-lookup"><span data-stu-id="27dee-115">This topic shows example code to manage seeking and rate changes, when using the [Media Session](media-session.md) for playback.</span></span><br/> |
| [<span data-ttu-id="27dee-116">Cómo establecer la hora de detención de la reproducción</span><span class="sxs-lookup"><span data-stu-id="27dee-116">How to Set the Playback Stop Time</span></span>](how-to-set-the-playback-stop-time-.md)<br/>              | <span data-ttu-id="27dee-117">En este tema se describe cómo establecer una hora de detención para la reproducción cuando se usa la [sesión multimedia](media-session.md).</span><span class="sxs-lookup"><span data-stu-id="27dee-117">This topic describes how to set a stop time for playback when using the [Media Session](media-session.md).</span></span><br/>                       |
| [<span data-ttu-id="27dee-118">Representador de vídeo mejorado</span><span class="sxs-lookup"><span data-stu-id="27dee-118">Enhanced Video Renderer</span></span>](enhanced-video-renderer.md)<br/>                                   | <span data-ttu-id="27dee-119">El representador de vídeo mejorado (EVR) es un componente que muestra vídeo en el monitor del usuario.</span><span class="sxs-lookup"><span data-stu-id="27dee-119">The enhanced video renderer (EVR) is a component that displays video on the user's monitor.</span></span><br/>                                       |
| [<span data-ttu-id="27dee-120">Representador de audio de streaming</span><span class="sxs-lookup"><span data-stu-id="27dee-120">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)<br/>                                 | <span data-ttu-id="27dee-121">Streaming audio renderer (SAR) es un receptor de medios que representa el audio.</span><span class="sxs-lookup"><span data-stu-id="27dee-121">The streaming audio renderer (SAR) is a media sink that renders audio.</span></span><br/>                                                            |
| [<span data-ttu-id="27dee-122">MFPlay</span><span class="sxs-lookup"><span data-stu-id="27dee-122">MFPlay</span></span>](using-mfplay-for-audio-video-playback.md)<br/>                                      | <span data-ttu-id="27dee-123">La API de MFPlay está en desuso.</span><span class="sxs-lookup"><span data-stu-id="27dee-123">The MFPlay API is deprecated.</span></span><br/>                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="27dee-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="27dee-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27dee-125">Arquitectura de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="27dee-125">Media Foundation Architecture</span></span>](media-foundation-architecture.md)
</dt> <dt>

[<span data-ttu-id="27dee-126">Guía de programación de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="27dee-126">Media Foundation Programming Guide</span></span>](media-foundation-programming-guide.md)
</dt> <dt>

[<span data-ttu-id="27dee-127">Compatibilidad con MPEG-4 en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="27dee-127">MPEG-4 Support in Media Foundation</span></span>](mpeg-4-support-in-media-foundation.md)
</dt> </dl>

 

 




