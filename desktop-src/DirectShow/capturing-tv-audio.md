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
# <a name="capturing-tv-audio"></a><span data-ttu-id="71aa9-103">Captura de audio de TV</span><span class="sxs-lookup"><span data-stu-id="71aa9-103">Capturing TV Audio</span></span>

<span data-ttu-id="71aa9-104">Para capturar audio de televisión analógica en un archivo, use el [filtro de captura de audio](audio-capture-filter.md).</span><span class="sxs-lookup"><span data-stu-id="71aa9-104">To capture audio from analog television to a file, use the [Audio Capture Filter](audio-capture-filter.md).</span></span> <span data-ttu-id="71aa9-105">Use el enumerador de dispositivos del sistema para crear el filtro de captura de audio.</span><span class="sxs-lookup"><span data-stu-id="71aa9-105">Use the System Device Enumerator to create the Audio Capture Filter.</span></span> <span data-ttu-id="71aa9-106">Puede haber varios dispositivos de captura de audio en el sistema del usuario. el usuario debe seleccionar el dispositivo que representa la tarjeta de sonido.</span><span class="sxs-lookup"><span data-stu-id="71aa9-106">There may be several audio capture devices on the user's system; the user must select the device that represents the sound card.</span></span>

<span data-ttu-id="71aa9-107">Conecte el PIN de salida de la captura de audio al filtro MUX:</span><span class="sxs-lookup"><span data-stu-id="71aa9-107">Connect the audio capture output pin to the mux filter:</span></span>


```C++
hr = pBuild->RenderStream(
   &PIN_CATEGORY_CAPTURE, // Capture pin.
   &MEDIATYPE_Audio,      // Audio media type.
   pAudioCap,             // Pointer to the audio capture filter.
   NULL,                  // Optional audio compressor filter.
   pMux);                 // Pointer to the mux filter.
```



<span data-ttu-id="71aa9-108">No es necesario que los pin de entrada estén conectados a nada.</span><span class="sxs-lookup"><span data-stu-id="71aa9-108">The input pins do not have to be connected to anything.</span></span> <span data-ttu-id="71aa9-109">Cada pin de entrada representa una entrada física en el dispositivo de captura de audio.</span><span class="sxs-lookup"><span data-stu-id="71aa9-109">Each input pin represents a physical input on the audio capture device.</span></span> <span data-ttu-id="71aa9-110">Use la interfaz [**IAMAudioInputMixer**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer) para habilitar la entrada que recibe la secuencia de audio desde el sintonizador.</span><span class="sxs-lookup"><span data-stu-id="71aa9-110">Use the [**IAMAudioInputMixer**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer) interface to enable the input that receives the audio stream from the tuner.</span></span> <span data-ttu-id="71aa9-111">Los pin de entrada se identifican por su nombre, como "línea en" o "audio de CD".</span><span class="sxs-lookup"><span data-stu-id="71aa9-111">The input pins are identified by name, such as "Line In" or "CD Audio."</span></span> <span data-ttu-id="71aa9-112">Desafortunadamente, los nombres pueden cambiar de un dispositivo a otro.</span><span class="sxs-lookup"><span data-stu-id="71aa9-112">Unfortunately, the names can change from one device to the next.</span></span> <span data-ttu-id="71aa9-113">Además, las distintas tarjetas sintonizadoras de TV usan entradas diferentes para la tarjeta de sonido.</span><span class="sxs-lookup"><span data-stu-id="71aa9-113">Also, different TV tuner cards use different inputs to the sound card.</span></span> <span data-ttu-id="71aa9-114">Por lo tanto, depende del usuario identificar la entrada que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="71aa9-114">Therefore, it is up to the user to identify which input to use.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="71aa9-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="71aa9-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71aa9-116">Audio analógico de televisión</span><span class="sxs-lookup"><span data-stu-id="71aa9-116">Analog Television Audio</span></span>](analog-television-audio.md)
</dt> <dt>

[<span data-ttu-id="71aa9-117">Captura de audio</span><span class="sxs-lookup"><span data-stu-id="71aa9-117">Audio Capture</span></span>](audio-capture.md)
</dt> </dl>

 

 



