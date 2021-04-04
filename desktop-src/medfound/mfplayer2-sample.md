---
description: Importante en desuso.
ms.assetid: bb71e792-d09c-4338-9cf4-4854e14042f9
title: Ejemplo de MFPlayer2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1904dcc6e64024dacb76e9109f2e785ec8d5a96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908381"
---
# <a name="mfplayer2-sample"></a><span data-ttu-id="61e77-103">Ejemplo de MFPlayer2</span><span class="sxs-lookup"><span data-stu-id="61e77-103">MFPlayer2 Sample</span></span>

> [!IMPORTANT]
> <span data-ttu-id="61e77-104">En desuso.</span><span class="sxs-lookup"><span data-stu-id="61e77-104">Deprecated.</span></span> <span data-ttu-id="61e77-105">Esta API se puede quitar de las versiones futuras de Windows.</span><span class="sxs-lookup"><span data-stu-id="61e77-105">This API may be removed from future releases of Windows.</span></span> <span data-ttu-id="61e77-106">Las aplicaciones deben usar la [sesión multimedia](media-session.md) para la reproducción.</span><span class="sxs-lookup"><span data-stu-id="61e77-106">Applications should use the [Media Session](media-session.md) for playback.</span></span>

 

<span data-ttu-id="61e77-107">Muestra algunas de las características de reproducción que se omiten en el ejemplo [SimplePlay](simpleplay-sample.md) , como:</span><span class="sxs-lookup"><span data-stu-id="61e77-107">Demonstrates some of the playback features that are omitted from the [SimplePlay](simpleplay-sample.md) sample, such as:</span></span>

-   <span data-ttu-id="61e77-108">Invoca</span><span class="sxs-lookup"><span data-stu-id="61e77-108">Seeking</span></span>
-   <span data-ttu-id="61e77-109">Control de velocidad (avance rápido y rebobinado)</span><span class="sxs-lookup"><span data-stu-id="61e77-109">Rate control (fast forward and rewind)</span></span>
-   <span data-ttu-id="61e77-110">Controles volumen de audio y silenciar</span><span class="sxs-lookup"><span data-stu-id="61e77-110">Audio volume and mute controls</span></span>
-   <span data-ttu-id="61e77-111">Zoom de vídeo</span><span class="sxs-lookup"><span data-stu-id="61e77-111">Video zoom</span></span>

<span data-ttu-id="61e77-112">En la imagen siguiente se muestran los controles que se usan para estas características.</span><span class="sxs-lookup"><span data-stu-id="61e77-112">The following image shows the controls used for these features.</span></span>

![<span data-ttu-id="61e77-113">captura de pantalla del ejemplo mfPlayer</span><span class="sxs-lookup"><span data-stu-id="61e77-113">screen shot of the mfplayer sample</span></span> ](images/mfplayer2.png)

## <a name="apis-demonstrated"></a><span data-ttu-id="61e77-114">API mostradas</span><span class="sxs-lookup"><span data-stu-id="61e77-114">APIs Demonstrated</span></span>

<span data-ttu-id="61e77-115">Este ejemplo muestra las siguientes API.</span><span class="sxs-lookup"><span data-stu-id="61e77-115">This sample demonstrates the following APIs.</span></span>

-   [<span data-ttu-id="61e77-116">**IAudioSessionControl**</span><span class="sxs-lookup"><span data-stu-id="61e77-116">**IAudioSessionControl**</span></span>](/windows/win32/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol)
-   [<span data-ttu-id="61e77-117">**IAudioSessionManager**</span><span class="sxs-lookup"><span data-stu-id="61e77-117">**IAudioSessionManager**</span></span>](/windows/win32/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager)
-   [<span data-ttu-id="61e77-118">**IMFPMediaItem**</span><span class="sxs-lookup"><span data-stu-id="61e77-118">**IMFPMediaItem**</span></span>](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem)
-   [<span data-ttu-id="61e77-119">**IMFPMediaPlayer**</span><span class="sxs-lookup"><span data-stu-id="61e77-119">**IMFPMediaPlayer**</span></span>](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer)
-   [<span data-ttu-id="61e77-120">**IMFPMediaPlayerCallback**</span><span class="sxs-lookup"><span data-stu-id="61e77-120">**IMFPMediaPlayerCallback**</span></span>](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback)
-   [<span data-ttu-id="61e77-121">**IMMDevice**</span><span class="sxs-lookup"><span data-stu-id="61e77-121">**IMMDevice**</span></span>](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdevice)
-   [<span data-ttu-id="61e77-122">**IMMDeviceEnumerator**</span><span class="sxs-lookup"><span data-stu-id="61e77-122">**IMMDeviceEnumerator**</span></span>](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator)
-   [<span data-ttu-id="61e77-123">**ISimpleAudioVolume**</span><span class="sxs-lookup"><span data-stu-id="61e77-123">**ISimpleAudioVolume**</span></span>](/windows/win32/api/audioclient/nn-audioclient-isimpleaudiovolume)

## <a name="requirements"></a><span data-ttu-id="61e77-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61e77-124">Requirements</span></span>



| <span data-ttu-id="61e77-125">Producto</span><span class="sxs-lookup"><span data-stu-id="61e77-125">Product</span></span>                                                        | <span data-ttu-id="61e77-126">Versión</span><span class="sxs-lookup"><span data-stu-id="61e77-126">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="61e77-127">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="61e77-127">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="61e77-128">Windows 7</span><span class="sxs-lookup"><span data-stu-id="61e77-128">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="61e77-129">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="61e77-129">Downloading the Sample</span></span>

<span data-ttu-id="61e77-130">Este ejemplo está disponible en el [repositorio de github de ejemplos de Windows clásico](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/MFPlayer2).</span><span class="sxs-lookup"><span data-stu-id="61e77-130">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/MFPlayer2).</span></span>

## <a name="related-topics"></a><span data-ttu-id="61e77-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="61e77-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61e77-132">Muestras de SDK de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="61e77-132">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> <dt>

[<span data-ttu-id="61e77-133">Uso de MFPlay para la reproducción de audio y vídeo</span><span class="sxs-lookup"><span data-stu-id="61e77-133">Using MFPlay for Audio/Video Playback</span></span>](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 
