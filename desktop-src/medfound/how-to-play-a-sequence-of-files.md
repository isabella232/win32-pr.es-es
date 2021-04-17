---
description: En este tema se describe cómo reproducir una secuencia de archivos de audio y vídeo mediante MFPlay.
ms.assetid: ee16eaa3-0506-4444-b139-f8a8498d6597
title: Cómo reproducir una secuencia de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58dc4d1523be4cc6cc09416096af260c9eae736c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652575"
---
# <a name="how-to-play-a-sequence-of-files"></a><span data-ttu-id="4213b-103">Cómo reproducir una secuencia de archivos</span><span class="sxs-lookup"><span data-stu-id="4213b-103">How to Play a Sequence of Files</span></span>

<span data-ttu-id="4213b-104">\[MFPlay está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="4213b-104">\[MFPlay is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="4213b-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="4213b-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="4213b-106">\]</span><span class="sxs-lookup"><span data-stu-id="4213b-106">\]</span></span>

<span data-ttu-id="4213b-107">En este tema se describe cómo reproducir una secuencia de archivos de audio y vídeo mediante MFPlay.</span><span class="sxs-lookup"><span data-stu-id="4213b-107">This topic describes how to play a sequence of audio/video files using MFPlay.</span></span>


<span data-ttu-id="4213b-108">El tema [Introducción con MFPlay](getting-started-with-mfplay.md) muestra cómo reproducir un solo archivo multimedia.</span><span class="sxs-lookup"><span data-stu-id="4213b-108">The topic [Getting Started with MFPlay](getting-started-with-mfplay.md) shows how to play a single media file.</span></span> <span data-ttu-id="4213b-109">También puede usar MFPlay para reproducir una secuencia de archivos.</span><span class="sxs-lookup"><span data-stu-id="4213b-109">You can also use MFPlay to play a sequence of files.</span></span>

### <a name="synchronous-blocking-method"></a><span data-ttu-id="4213b-110">Método sincrónico (bloqueo)</span><span class="sxs-lookup"><span data-stu-id="4213b-110">Synchronous (Blocking) Method</span></span>

1.  <span data-ttu-id="4213b-111">Llame al método [**IMFPMediaPlayer:: CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) .</span><span class="sxs-lookup"><span data-stu-id="4213b-111">Call the [**IMFPMediaPlayer::CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) method.</span></span> <span data-ttu-id="4213b-112">El método crea un elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="4213b-112">The method creates a media item.</span></span>
2.  <span data-ttu-id="4213b-113">Llame a [**IMFPMediaPlayer:: SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) para poner en cola el elemento multimedia para la reproducción.</span><span class="sxs-lookup"><span data-stu-id="4213b-113">Call [**IMFPMediaPlayer::SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) to queue the media item for playback.</span></span>
3.  <span data-ttu-id="4213b-114">Llame a [**IMFPMediaPlayer::P establecer**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) para iniciar la reproducción.</span><span class="sxs-lookup"><span data-stu-id="4213b-114">Call [**IMFPMediaPlayer::Play**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) to start playback.</span></span>

<span data-ttu-id="4213b-115">Estos pasos se muestran en el código siguiente.</span><span class="sxs-lookup"><span data-stu-id="4213b-115">These steps are shown in the following code.</span></span>


```C++
HRESULT OpenMediaFile(IMFPMediaPlayer *pPlayer, PCWSTR pwszURL)
{
    HRESULT hr = S_OK;
    
    IMFPMediaItem *pItem = NULL;

    hr = pPlayer->CreateMediaItemFromURL(
        sURL, 
        TRUE,  // Blocking call
        0,     // User data.
        &pItem
        );

    if (SUCCEEDED(hr))
    {
        hr = pPlayer->SetMediaItem(pItem);
    }

    if (SUCCEEDED(hr))
    {
       hr = pPlayer->Play();
    }

    if (pItem)
    {
        pItem->Release();
    }
    return hr;
}
```



<span data-ttu-id="4213b-116">El método [**CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) toma los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="4213b-116">The [**CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) method takes the following parameters:</span></span>

-   <span data-ttu-id="4213b-117">El primer parámetro es la dirección URL del archivo.</span><span class="sxs-lookup"><span data-stu-id="4213b-117">The first parameter is the URL of the file.</span></span>
-   <span data-ttu-id="4213b-118">El segundo parámetro especifica si el método se bloquea.</span><span class="sxs-lookup"><span data-stu-id="4213b-118">The second parameter specifies whether the method blocks.</span></span> <span data-ttu-id="4213b-119">Especificar el valor **true**, como se muestra aquí, hace que el método se bloquee hasta que se cree el elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="4213b-119">Specifying the value **TRUE**, as shown here, causes the method to block until the media item is created.</span></span>
-   <span data-ttu-id="4213b-120">El tercer parámetro asocia un valor **DWORD \_ ptr** arbitrario con el elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="4213b-120">The third parameter associates an arbitrary **DWORD\_PTR** value with the media item.</span></span> <span data-ttu-id="4213b-121">Puede obtener este valor más adelante llamando a [**IMFPMediaItem:: GetUserData**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-getuserdata).</span><span class="sxs-lookup"><span data-stu-id="4213b-121">You can get this value later by calling [**IMFPMediaItem::GetUserData**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-getuserdata).</span></span>
-   <span data-ttu-id="4213b-122">El cuarto parámetro recibe un puntero a la interfaz [**IMFPMediaItem**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) del elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="4213b-122">The fourth parameter receives a pointer to the [**IMFPMediaItem**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) interface of the media item.</span></span>

### <a name="asynchronous-non-blocking-method"></a><span data-ttu-id="4213b-123">Método asincrónico (sin bloqueo)</span><span class="sxs-lookup"><span data-stu-id="4213b-123">Asynchronous (Non-Blocking) Method</span></span>

<span data-ttu-id="4213b-124">Evite la opción de bloqueo si llama a [**CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) desde el subproceso de la interfaz de usuario, ya que puede tardar bastante tiempo en completarse.</span><span class="sxs-lookup"><span data-stu-id="4213b-124">Avoid the blocking option if you call [**CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) from your UI thread, because it can take a noticeable amount of time to complete.</span></span> <span data-ttu-id="4213b-125">Normalmente, el método abre un archivo o una conexión de red y Lee los datos suficientes para analizar los encabezados de archivo, lo que puede llevar tiempo.</span><span class="sxs-lookup"><span data-stu-id="4213b-125">The method typically opens a file or network connection and reads enough data to parse the file headers, all of which can take time.</span></span> <span data-ttu-id="4213b-126">Por lo tanto, suele ser mejor establecer el segundo parámetro en **false**.</span><span class="sxs-lookup"><span data-stu-id="4213b-126">Therefore, it is generally better to set the second parameter to **FALSE**.</span></span> <span data-ttu-id="4213b-127">Esta opción hace que el método realice de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="4213b-127">This option causes the method to perform asynchronously.</span></span> <span data-ttu-id="4213b-128">Cuando se usa la opción asincrónica, el último parámetro debe ser **null**:</span><span class="sxs-lookup"><span data-stu-id="4213b-128">When the asynchronous option is used, the last parameter must be **NULL**:</span></span>


```C++
    hr = pPlayer->CreateMediaItemFromURL(
        sURL, 
        FALSE,  // Non-blocking call.
        0,      // User data.
        NULL    // Must be NULL for the non-blocking call.
        );
```



<span data-ttu-id="4213b-129">Cuando se crea el elemento multimedia, la aplicación recibe un **evento \_ \_ MEDIAITEM de \_ \_ tipo de evento MFP** .</span><span class="sxs-lookup"><span data-stu-id="4213b-129">When the media item is created, your application receives an **MFP\_EVENT\_TYPE\_MEDIAITEM\_CREATED** event.</span></span> <span data-ttu-id="4213b-130">La estructura de datos para este evento contiene un puntero al elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="4213b-130">The data structure for this event contains a pointer to the media item.</span></span> <span data-ttu-id="4213b-131">Pase este puntero al método [**SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) para poner en cola el elemento para la reproducción.</span><span class="sxs-lookup"><span data-stu-id="4213b-131">Pass this pointer to the [**SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) method to queue the item for playback.</span></span>


```C++
void OnMediaItemCreated(MFP_MEDIAITEM_CREATED_EVENT *pEvent)
{
    HRESULT hr = S_OK;
    if (FAILED(pEvent->header.hrEvent))
    {
        // Handle error. (Not shown.)
    }
    else
    {
        hr = g_pPlayer->SetMediaItem(pEvent->pMediaItem);
    }
}
```



## <a name="requirements"></a><span data-ttu-id="4213b-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4213b-132">Requirements</span></span>

<span data-ttu-id="4213b-133">MFPlay requiere Windows 7.</span><span class="sxs-lookup"><span data-stu-id="4213b-133">MFPlay requires Windows 7.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4213b-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4213b-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4213b-135">Uso de MFPlay para la reproducción de audio y vídeo</span><span class="sxs-lookup"><span data-stu-id="4213b-135">Using MFPlay for Audio/Video Playback</span></span>](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



