---
description: Cómo realizar la limpieza
ms.assetid: 3cf56caf-5c6d-4318-811a-c8bdc1959148
title: Cómo realizar la limpieza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab86ae39567132352592883b7441e4f325cb1b021b74e5b7a67f4a2755c3c947
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118063362"
---
# <a name="how-to-perform-scrubbing"></a>Cómo realizar la limpieza

La limpieza se realiza para buscar instantáneamente puntos específicos dentro de un archivo mediante la interacción con una representación visual del tiempo, como una barra de desplazamiento. En Media Foundation, limpiar significa buscar en un archivo y obtener un fotograma actualizado.

Para obtener información sobre la limpieza, vea [About Rate Control](about-rate-control.md).

## <a name="to-perform-scrubbing"></a>Para realizar la limpieza

1.  Llame [**a MFGetService para**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) obtener la interfaz [**MFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) de la sesión [multimedia](media-session.md).
    > [!Note]  
    > No obtenga la interfaz [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) del origen multimedia. Obtenga siempre la interfaz de la sesión multimedia.

     

2.  Llame [**a IMFRateControl::SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) para establecer la velocidad de reproducción en cero. Para obtener más información sobre cómo llamar a este método, [vea How to Set the Playback Rate on the Media Session](how-to-set-the-playback-rate-on-the-media-session.md).
3.  Cree una posición de búsqueda en **PROPVARIANT** especificando el tiempo de presentación al que se buscará en un **tipo MFTIME.**
4.  Llame [**a IMFMediaSession::Start con**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) la posición de búsqueda para iniciar la reproducción.
5.  Una vez completada la operación de limpieza, la sesión multimedia envía un [evento MESessionScrubSampleComplete.](mesessionscrubsamplecomplete.md) Espere este evento antes de llamar a [**Start de**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) nuevo para otra operación de limpieza.

## <a name="example"></a>Ejemplo

En el ejemplo de código siguiente se muestra cómo realizar la limpieza.


```C++
HRESULT SkipToPosition (MFTIME SeekTime, IMFMediaSession *pMediaSession)
{
    PROPVARIANT var;
    PropVariantInit(&var);

    IMFRateControl *pRateControl = NULL;

    // Get the rate control service.
    HRESULT hr = MFGetService(pMediaSession, MF_RATE_CONTROL_SERVICE, IID_PPV_ARGS(&pRateControl));

    // Set the playback rate to zero without thinning.
    if(SUCCEEDED(hr))
    {
        hr = pRateControl ->SetRate( FALSE, 0.0F); 
    }

    // Create the Media Session start position.
    if( SeekTime == PRESENTATION_CURRENT_POSITION )
    {
        var.vt = VT_EMPTY;
    }
    else
    {
        var.vt = VT_I8;
        var.hVal.QuadPart = SeekTime;
    }

    // Start the Media Session.
    if(SUCCEEDED(hr))
    {
        hr = pMediaSession->Start( NULL, &var);
    }

// Clean up.
    SafeRelease(&pRateControl);
    PropVariantClear(&var)
    return hr;
}
```



Una operación de limpieza correcta genera el evento [MESessionScrubSampleComplete](mesessionscrubsamplecomplete.md) después de que todos los receptores de flujo se actualicen con el nuevo fotograma y la operación de limpieza se complete correctamente. Al limpiar un archivo de vídeo se muestra el fotograma al que se ha buscando, pero no se genera una salida de audio.

La aplicación puede realizar la ejecución paso a paso de fotogramas estableciendo la velocidad de reproducción en cero y, a continuación, pasando un **VALOR PROPVARIANT** que se establece en **VT \_ EMPTY** en la llamada a [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sesión multimedia](media-session.md)
</dt> <dt>

[Control de velocidad](rate-control.md)
</dt> </dl>

 

 



