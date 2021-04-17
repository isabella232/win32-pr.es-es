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
# <a name="how-to-play-a-sequence-of-files"></a>Cómo reproducir una secuencia de archivos

\[MFPlay está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En versiones posteriores podría modificarse o no estar disponible. \]

En este tema se describe cómo reproducir una secuencia de archivos de audio y vídeo mediante MFPlay.


El tema [Introducción con MFPlay](getting-started-with-mfplay.md) muestra cómo reproducir un solo archivo multimedia. También puede usar MFPlay para reproducir una secuencia de archivos.

### <a name="synchronous-blocking-method"></a>Método sincrónico (bloqueo)

1.  Llame al método [**IMFPMediaPlayer:: CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) . El método crea un elemento multimedia.
2.  Llame a [**IMFPMediaPlayer:: SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) para poner en cola el elemento multimedia para la reproducción.
3.  Llame a [**IMFPMediaPlayer::P establecer**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) para iniciar la reproducción.

Estos pasos se muestran en el código siguiente.


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



El método [**CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) toma los siguientes parámetros:

-   El primer parámetro es la dirección URL del archivo.
-   El segundo parámetro especifica si el método se bloquea. Especificar el valor **true**, como se muestra aquí, hace que el método se bloquee hasta que se cree el elemento multimedia.
-   El tercer parámetro asocia un valor **DWORD \_ ptr** arbitrario con el elemento multimedia. Puede obtener este valor más adelante llamando a [**IMFPMediaItem:: GetUserData**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-getuserdata).
-   El cuarto parámetro recibe un puntero a la interfaz [**IMFPMediaItem**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) del elemento multimedia.

### <a name="asynchronous-non-blocking-method"></a>Método asincrónico (sin bloqueo)

Evite la opción de bloqueo si llama a [**CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) desde el subproceso de la interfaz de usuario, ya que puede tardar bastante tiempo en completarse. Normalmente, el método abre un archivo o una conexión de red y Lee los datos suficientes para analizar los encabezados de archivo, lo que puede llevar tiempo. Por lo tanto, suele ser mejor establecer el segundo parámetro en **false**. Esta opción hace que el método realice de forma asincrónica. Cuando se usa la opción asincrónica, el último parámetro debe ser **null**:


```C++
    hr = pPlayer->CreateMediaItemFromURL(
        sURL, 
        FALSE,  // Non-blocking call.
        0,      // User data.
        NULL    // Must be NULL for the non-blocking call.
        );
```



Cuando se crea el elemento multimedia, la aplicación recibe un **evento \_ \_ MEDIAITEM de \_ \_ tipo de evento MFP** . La estructura de datos para este evento contiene un puntero al elemento multimedia. Pase este puntero al método [**SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) para poner en cola el elemento para la reproducción.


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



## <a name="requirements"></a>Requisitos

MFPlay requiere Windows 7.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de MFPlay para la reproducción de audio y vídeo](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



