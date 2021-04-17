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
# <a name="video-preview"></a>Vista previa de vídeo

\[MFPlay está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En versiones posteriores podría modificarse o no estar disponible. \]

En este tema se describe cómo usar MFPlay para obtener una vista previa del vídeo de una cámara de vídeo.

MFPlay proporciona la forma más sencilla de Microsoft Media Foundation para obtener una vista previa de vídeo desde un dispositivo de captura. Debe usar MFPlay si se cumplen todas las condiciones siguientes:

-   No es necesario capturar el vídeo en un archivo.
-   No es necesario tener un control preciso sobre cómo se representa el vídeo. (Por ejemplo, no es necesario controlar la creación del dispositivo Direct3D).
-   No es necesario procesar los datos de vídeo de la cámara antes de la representación.

De lo contrario, el [lector de origen](source-reader.md) puede ser una opción mejor.

Para usar MFPlay con un dispositivo de captura de vídeo, realice los pasos siguientes:

1.  Cree un origen de medios para el dispositivo de captura. Consulte [enumeración de dispositivos de captura de vídeo](enumerating-video-capture-devices.md).
2.  Llame a [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) para crear una instancia del objeto Player.
3.  Llame al método [**IMFPMediaPlayer:: CreateMediaItemFromObject**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromobject) . Pase un puntero a la interfaz IMFMediaSource del origen multimedia. El método recibe un puntero a la interfaz [**IMFPMediaItem**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) .
4.  Llame a [**IMFPMediaPlayer:: SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem).
5.  Llame a [**IMFPMediaPlayer::P establecer**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) para comenzar la vista previa.

El siguiente código muestra estos pasos:


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



En una aplicación típica, se proporciona un puntero a una interfaz de devolución de llamada en la función [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) y se usa la interfaz de devolución de llamada para obtener eventos del reproductor. Para simplificar, el código que se muestra aquí omite estos pasos. Para obtener más información, vea [Introducción con MFPlay](getting-started-with-mfplay.md).

### <a name="shutting-down"></a>Apagar

Antes de que se cierre la aplicación, cierre el origen de medios y el objeto de reproductor como se indica a continuación:

1.  Llame a [**IMFMediaSource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) en el origen del medio.
2.  Llame a [**IMFPMediaPlayer:: Shutdown**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-shutdown) en el objeto Player.


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



## <a name="requirements"></a>Requisitos

MFPlay requiere Windows 7.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[MFPlay](using-mfplay-for-audio-video-playback.md)
</dt> <dt>

[Captura de vídeo](audio-video-capture.md)
</dt> </dl>

 

 



