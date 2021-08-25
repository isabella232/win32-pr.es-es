---
description: En este tema se describe cómo reproducir una secuencia de archivos de audio y vídeo mediante MFPlay.
ms.assetid: ee16eaa3-0506-4444-b139-f8a8498d6597
title: Cómo reproducir una secuencia de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1ddf9cfc6fe48caf5eb185a19ec98ac119fcfbbb78d5e2363bd2db9607a4875
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828165"
---
# <a name="how-to-play-a-sequence-of-files"></a>Cómo reproducir una secuencia de archivos

\[MFPlay está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En versiones posteriores podría modificarse o no estar disponible. \]

En este tema se describe cómo reproducir una secuencia de archivos de audio y vídeo mediante MFPlay.


El tema [Tareas iniciales con MFPlay](getting-started-with-mfplay.md) muestra cómo reproducir un único archivo multimedia. También puede usar MFPlay para reproducir una secuencia de archivos.

### <a name="synchronous-blocking-method"></a>Método sincrónico (bloqueo)

1.  Llame al [**método IMFPMediaPlayer::CreateMediaItemFromURL.**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) El método crea un elemento multimedia.
2.  Llame [**a IMFPMediaPlayer::SetMediaItem para**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) poner en cola el elemento multimedia para su reproducción.
3.  Llame [**a IMFPMediaPlayer::P lay para**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) iniciar la reproducción.

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



El [**método CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) toma los parámetros siguientes:

-   El primer parámetro es la dirección URL del archivo.
-   El segundo parámetro especifica si el método se bloquea. Al especificar el valor **TRUE**, como se muestra aquí, el método se bloquea hasta que se crea el elemento multimedia.
-   El tercer parámetro asocia un valor **\_ PTR de DWORD** arbitrario al elemento multimedia. Puede obtener este valor más adelante mediante una llamada [**a IMFPMediaItem::GetUserData**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-getuserdata).
-   El cuarto parámetro recibe un puntero a la interfaz [**IMFPMediaItem**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) del elemento multimedia.

### <a name="asynchronous-non-blocking-method"></a>Método asincrónico (sin bloqueo)

Evite la opción de bloqueo si llama a [**CreateMediaItemFromURL desde**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) el subproceso de interfaz de usuario, ya que puede tardar un tiempo considerable en completarse. Normalmente, el método abre un archivo o una conexión de red y lee suficientes datos para analizar los encabezados de archivo, que pueden tardar tiempo. Por lo tanto, generalmente es mejor establecer el segundo parámetro en **FALSE.** Esta opción hace que el método se realice de forma asincrónica. Cuando se usa la opción asincrónica, el último parámetro debe ser **NULL**:


```C++
    hr = pPlayer->CreateMediaItemFromURL(
        sURL, 
        FALSE,  // Non-blocking call.
        0,      // User data.
        NULL    // Must be NULL for the non-blocking call.
        );
```



Cuando se crea el elemento multimedia, la aplicación recibe un evento **\_ MEDIAITEM CREATED DEL TIPO DE EVENTO \_ \_ \_ MFP.** La estructura de datos de este evento contiene un puntero al elemento multimedia. Pase este puntero al [**método SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) para poner en cola el elemento para su reproducción.


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

 

 



