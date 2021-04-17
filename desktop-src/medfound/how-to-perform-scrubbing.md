---
description: Cómo realizar la limpieza
ms.assetid: 3cf56caf-5c6d-4318-811a-c8bdc1959148
title: Cómo realizar la limpieza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dad1f06cb6abe6a570fd85407028450651e32a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543606"
---
# <a name="how-to-perform-scrubbing"></a>Cómo realizar la limpieza

La limpieza se realiza para buscar de forma instantánea puntos específicos dentro de un archivo interactuando con una representación visual del tiempo, como una barra de desplazamiento. En Media Foundation, la limpieza significa buscar en un archivo y obtener un marco actualizado.

Para obtener información acerca de la limpieza, vea [About Rate Control](about-rate-control.md).

## <a name="to-perform-scrubbing"></a>Para realizar la limpieza

1.  Llame a [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) para obtener la interfaz [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) de la [sesión multimedia](media-session.md).
    > [!Note]  
    > No obtenga la interfaz [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) desde el origen de medios. Obtenga siempre la interfaz de la sesión multimedia.

     

2.  Llame a [**IMFRateControl:: SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) para establecer la velocidad de reproducción en cero. Para obtener más información sobre cómo llamar a este método, vea [cómo establecer la velocidad de reproducción en la sesión multimedia](how-to-set-the-playback-rate-on-the-media-session.md).
3.  Cree una posición de búsqueda en un **PROPVARIANT** especificando el tiempo de presentación que se va a buscar en un tipo de **MFTIME** .
4.  Llame a [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) con la posición de búsqueda para iniciar la reproducción.
5.  Cuando se completa la operación de limpieza, la sesión multimedia envía un evento [MESessionScrubSampleComplete](mesessionscrubsamplecomplete.md) . Espere a que este evento antes de llamar a [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) de nuevo para otra operación de limpieza.

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



Una operación de limpieza correcta genera el evento [MESessionScrubSampleComplete](mesessionscrubsamplecomplete.md) después de que todos los receptores de flujo se actualicen con el nuevo marco y la operación de limpieza se complete correctamente. Al limpiar un archivo de vídeo se muestra el fotograma en el que se ha buscado, pero no se genera una salida de audio.

La aplicación puede realizar la ejecución paso a paso estableciendo la velocidad de reproducción en cero y, a continuación, pasando un **PROPVARIANT** que se establece en **VT \_ vacío** en la llamada a [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sesión de medios](media-session.md)
</dt> <dt>

[Control de tasa](rate-control.md)
</dt> </dl>

 

 



