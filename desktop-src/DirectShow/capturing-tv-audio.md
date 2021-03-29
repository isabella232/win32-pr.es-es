---
description: Captura de audio de TV
ms.assetid: c0c62a8e-ab16-4617-936c-b64e6e3865b4
title: Captura de audio de TV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 138ce631aedf12ddfb52be92d08ffb47da0cbdec
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105666129"
---
# <a name="capturing-tv-audio"></a>Captura de audio de TV

Para capturar audio de televisión analógica en un archivo, use el [filtro de captura de audio](audio-capture-filter.md). Use el enumerador de dispositivos del sistema para crear el filtro de captura de audio. Puede haber varios dispositivos de captura de audio en el sistema del usuario. el usuario debe seleccionar el dispositivo que representa la tarjeta de sonido.

Conecte el PIN de salida de la captura de audio al filtro MUX:


```C++
hr = pBuild->RenderStream(
   &PIN_CATEGORY_CAPTURE, // Capture pin.
   &MEDIATYPE_Audio,      // Audio media type.
   pAudioCap,             // Pointer to the audio capture filter.
   NULL,                  // Optional audio compressor filter.
   pMux);                 // Pointer to the mux filter.
```



No es necesario que los pin de entrada estén conectados a nada. Cada pin de entrada representa una entrada física en el dispositivo de captura de audio. Use la interfaz [**IAMAudioInputMixer**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer) para habilitar la entrada que recibe la secuencia de audio desde el sintonizador. Los pin de entrada se identifican por su nombre, como "línea en" o "audio de CD". Desafortunadamente, los nombres pueden cambiar de un dispositivo a otro. Además, las distintas tarjetas sintonizadoras de TV usan entradas diferentes para la tarjeta de sonido. Por lo tanto, depende del usuario identificar la entrada que se va a usar.


```C++
IEnumPins *pEnum = NULL;
hr = pAudioCap->EnumPins(&pEnum);
if (SUCCEEDED(hr))
{
    IPin *pPin = NULL;
    while (S_OK == pEnum->Next(1, &pPin, NULL))
    {
        IAMAudioInputMixer *pMix;
        hr = pPin->QueryInterface(IID_IAMAudioInputMixer, (void**)&pMix);
        if (SUCCEEDED(hr))
        {
            // Use IPin::QueryPinInfo to get the pin name.
            pPin->Release();
            if (...) // If the user selects this pin:
            {
                pMix->put_Enable(TRUE);
                pMix->put_MixLevel(1.0);
                pMix->Release();
                break;
            }
            pMix->Release();
        }
    }
}
pEnum->Release();
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Audio analógico de televisión](analog-television-audio.md)
</dt> <dt>

[Captura de audio](audio-capture.md)
</dt> </dl>

 

 



