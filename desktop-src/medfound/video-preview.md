---
description: En este tema se describe cómo usar MFPlay para obtener una vista previa del vídeo de una cámara de vídeo.
ms.assetid: ecf6113f-1d8e-4680-87ab-bfd45a9663e4
title: Vista previa de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9d458568a18f598e5aa4ee7e8fb21059e503362
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715479"
---
# <a name="video-preview"></a><span data-ttu-id="793a9-103">Vista previa de vídeo</span><span class="sxs-lookup"><span data-stu-id="793a9-103">Video Preview</span></span>

<span data-ttu-id="793a9-104">\[MFPlay está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="793a9-104">\[MFPlay is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="793a9-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="793a9-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="793a9-106">\]</span><span class="sxs-lookup"><span data-stu-id="793a9-106">\]</span></span>

<span data-ttu-id="793a9-107">En este tema se describe cómo usar MFPlay para obtener una vista previa del vídeo de una cámara de vídeo.</span><span class="sxs-lookup"><span data-stu-id="793a9-107">This topic describes how to use MFPlay to preview video from a video camera.</span></span>

<span data-ttu-id="793a9-108">MFPlay proporciona la forma más sencilla de Microsoft Media Foundation para obtener una vista previa de vídeo desde un dispositivo de captura.</span><span class="sxs-lookup"><span data-stu-id="793a9-108">MFPlay provides the simplest way in Microsoft Media Foundation to preview video from a capture device.</span></span> <span data-ttu-id="793a9-109">Debe usar MFPlay si se cumplen todas las condiciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="793a9-109">You should use MFPlay if the following conditions are all true:</span></span>

-   <span data-ttu-id="793a9-110">No es necesario capturar el vídeo en un archivo.</span><span class="sxs-lookup"><span data-stu-id="793a9-110">You do not need to capture the video to a file.</span></span>
-   <span data-ttu-id="793a9-111">No es necesario tener un control preciso sobre cómo se representa el vídeo.</span><span class="sxs-lookup"><span data-stu-id="793a9-111">You do not need fine-grained control over how the video is rendered.</span></span> <span data-ttu-id="793a9-112">(Por ejemplo, no es necesario controlar la creación del dispositivo Direct3D).</span><span class="sxs-lookup"><span data-stu-id="793a9-112">(For example, you do not need to control the creation of the Direct3D device.)</span></span>
-   <span data-ttu-id="793a9-113">No es necesario procesar los datos de vídeo de la cámara antes de la representación.</span><span class="sxs-lookup"><span data-stu-id="793a9-113">You do not need to process the video data from the camera prior to rendering.</span></span>

<span data-ttu-id="793a9-114">De lo contrario, el [lector de origen](source-reader.md) puede ser una opción mejor.</span><span class="sxs-lookup"><span data-stu-id="793a9-114">Otherwise, the [Source Reader](source-reader.md) may be a better option.</span></span>

<span data-ttu-id="793a9-115">Para usar MFPlay con un dispositivo de captura de vídeo, realice los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="793a9-115">To use MFPlay with a video capture device, perform the following steps:</span></span>

1.  <span data-ttu-id="793a9-116">Cree un origen de medios para el dispositivo de captura.</span><span class="sxs-lookup"><span data-stu-id="793a9-116">Create a media source for the capture device.</span></span> <span data-ttu-id="793a9-117">Consulte [enumeración de dispositivos de captura de vídeo](enumerating-video-capture-devices.md).</span><span class="sxs-lookup"><span data-stu-id="793a9-117">See [Enumerating Video Capture Devices](enumerating-video-capture-devices.md).</span></span>
2.  <span data-ttu-id="793a9-118">Llame a [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) para crear una instancia del objeto Player.</span><span class="sxs-lookup"><span data-stu-id="793a9-118">Call [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) to create an instance of the player object.</span></span>
3.  <span data-ttu-id="793a9-119">Llame al método [**IMFPMediaPlayer:: CreateMediaItemFromObject**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromobject) .</span><span class="sxs-lookup"><span data-stu-id="793a9-119">Call the [**IMFPMediaPlayer::CreateMediaItemFromObject**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromobject) method.</span></span> <span data-ttu-id="793a9-120">Pase un puntero a la interfaz IMFMediaSource del origen multimedia.</span><span class="sxs-lookup"><span data-stu-id="793a9-120">Pass in a pointer to the IMFMediaSource interface of the media source.</span></span> <span data-ttu-id="793a9-121">El método recibe un puntero a la interfaz [**IMFPMediaItem**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) .</span><span class="sxs-lookup"><span data-stu-id="793a9-121">The method receives a pointer to the [**IMFPMediaItem**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) interface.</span></span>
4.  <span data-ttu-id="793a9-122">Llame a [**IMFPMediaPlayer:: SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem).</span><span class="sxs-lookup"><span data-stu-id="793a9-122">Call [**IMFPMediaPlayer::SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem).</span></span>
5.  <span data-ttu-id="793a9-123">Llame a [**IMFPMediaPlayer::P establecer**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) para comenzar la vista previa.</span><span class="sxs-lookup"><span data-stu-id="793a9-123">Call [**IMFPMediaPlayer::Play**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) to begin previewing.</span></span>

<span data-ttu-id="793a9-124">El siguiente código muestra estos pasos:</span><span class="sxs-lookup"><span data-stu-id="793a9-124">The following code shows these steps:</span></span>


```C++
    IMFPMediaItem *pItem = NULL;

    if (SUCCEEDED(hr))
    {
        hr = MFPCreateMediaPlayer(
            NULL,       // URL.
            FALSE,      // Do not start playback yet.
            0,          // Option flags.
            NULL,       // Callback interface.
            hwnd,
            &g_pPlayer
            );
    }

    if (SUCCEEDED(hr))
    {
        hr = g_pPlayer->CreateMediaItemFromObject(
            g_pSource,
            TRUE,       // Blocking call.
            0,          // User data.
            &pItem
            );
    }

    if (SUCCEEDED(hr))
    {
        hr = g_pPlayer->SetMediaItem(pItem);
    }

    if (SUCCEEDED(hr))
    {
        hr = g_pPlayer->Play();
    }

    SafeRelease(&pItem);
```



<span data-ttu-id="793a9-125">En una aplicación típica, se proporciona un puntero a una interfaz de devolución de llamada en la función [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) y se usa la interfaz de devolución de llamada para obtener eventos del reproductor.</span><span class="sxs-lookup"><span data-stu-id="793a9-125">In a typical application, you would provide a pointer to a callback interface in the [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) function, and use the callback interface to get events from the player.</span></span> <span data-ttu-id="793a9-126">Para simplificar, el código que se muestra aquí omite estos pasos.</span><span class="sxs-lookup"><span data-stu-id="793a9-126">For simplicity, the code shown here skips these steps.</span></span> <span data-ttu-id="793a9-127">Para obtener más información, vea [Introducción con MFPlay](getting-started-with-mfplay.md).</span><span class="sxs-lookup"><span data-stu-id="793a9-127">For more information, see [Getting Started with MFPlay](getting-started-with-mfplay.md).</span></span>

### <a name="shutting-down"></a><span data-ttu-id="793a9-128">Apagar</span><span class="sxs-lookup"><span data-stu-id="793a9-128">Shutting Down</span></span>

<span data-ttu-id="793a9-129">Antes de que se cierre la aplicación, cierre el origen de medios y el objeto de reproductor como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="793a9-129">Before the application exits, shut down the media source and the player object as follows:</span></span>

1.  <span data-ttu-id="793a9-130">Llame a [**IMFMediaSource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) en el origen del medio.</span><span class="sxs-lookup"><span data-stu-id="793a9-130">Call [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) on the media source.</span></span>
2.  <span data-ttu-id="793a9-131">Llame a [**IMFPMediaPlayer:: Shutdown**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-shutdown) en el objeto Player.</span><span class="sxs-lookup"><span data-stu-id="793a9-131">Call [**IMFPMediaPlayer::Shutdown**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-shutdown) on the player object.</span></span>


```C++
    if (g_pSource)
    {
        g_pSource->Shutdown();
        g_pSource->Release();
        g_pSource = NULL;
    }

    if (g_pPlayer)
    {
        g_pPlayer->Shutdown();
        g_pPlayer->Release();
        g_pPlayer = NULL;
    }
```



## <a name="requirements"></a><span data-ttu-id="793a9-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="793a9-132">Requirements</span></span>

<span data-ttu-id="793a9-133">MFPlay requiere Windows 7.</span><span class="sxs-lookup"><span data-stu-id="793a9-133">MFPlay requires Windows 7.</span></span>

## <a name="related-topics"></a><span data-ttu-id="793a9-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="793a9-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="793a9-135">MFPlay</span><span class="sxs-lookup"><span data-stu-id="793a9-135">MFPlay</span></span>](using-mfplay-for-audio-video-playback.md)
</dt> <dt>

[<span data-ttu-id="793a9-136">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="793a9-136">Video Capture</span></span>](audio-video-capture.md)
</dt> </dl>

 

 



