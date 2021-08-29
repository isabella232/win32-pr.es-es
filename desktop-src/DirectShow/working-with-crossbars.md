---
description: Trabajar con barras cruzadas
ms.assetid: 6e8ee9c3-6776-498b-ad38-36f8172a27ae
title: Trabajar con barras cruzadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53686250b423c0bed245650be604fd8ec4b6a6ce713e5cde8582c66c8c4dc88f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119964445"
---
# <a name="working-with-crossbars"></a>Trabajar con barras cruzadas

Si una tarjeta de captura de vídeo tiene más de una entrada física o admite más de una ruta de acceso de hardware para los datos, el gráfico de filtros puede contener el filtro de barra cruzada [de vídeo análogo](analog-video-crossbar-filter.md). Capture Graph Builder agrega automáticamente este filtro cuando es necesario. será ascendente desde el filtro de captura. Dependiendo del hardware, el gráfico de filtros puede contener más de una instancia del filtro de barra cruzada.

El filtro de barra cruzada expone la [**interfaz IAMCrossbar,**](/windows/desktop/api/Strmif/nn-strmif-iamcrossbar) que puede usar para enrutar una entrada determinada a una salida determinada. Por ejemplo, una tarjeta de vídeo podría tener un conector de conector y una entrada de S-Video. Se representarán como pines de entrada en el filtro de barra cruzada. Para seleccionar una entrada, enruta el pin de entrada correspondiente al pin de salida de la barra cruzada mediante el [**método IAMCrossbar::Route.**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-route)

Para buscar filtros de barra cruzada en el gráfico, puede usar el método [**ICaptureGraphBuilder2::FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) para buscar filtros que admitan **IAMCrossbar**. Por ejemplo, el código siguiente busca dos barras cruzadas:


```C++
// Search upstream for a crossbar.
IAMCrossbar *pXBar1 = NULL;
hr = pBuild->FindInterface(&LOOK_UPSTREAM_ONLY, NULL, pSrc,
        IID_IAMCrossbar, (void**)&pXBar1);
if (SUCCEEDED(hr)) 
{
    // Found one crossbar. Get its IBaseFilter interface.
    IBaseFilter *pFilter = NULL;
    hr = pXBar1->QueryInterface(IID_IBaseFilter, (void**)&pFilter);
    if (SUCCEEDED(hr)) 
    {
        // Search upstream for another crossbar.
        IAMCrossbar *pXBar2 = NULL;
        hr = pBuild->FindInterface(&LOOK_UPSTREAM_ONLY, NULL, pFilter,
                 IID_IAMCrossbar, (void**)&pXBar2);
        pFilter->Release();

        if (SUCCEEDED(hr))
        {
            /* ... */
            pXBar2->Release();
        }
    }
    pXBar1->Release();
}
```



Para obtener un enfoque más generalizado, vea la clase CCrossbar en [el ejemplo de AmCap](amcap-sample.md).

Una vez que tenga un puntero a la interfaz **IAMCrossbar,** puede obtener información sobre el filtro de barra cruzada, incluido el tipo físico de cada pin, y la matriz de los pines de entrada que se pueden enrutar a los pines de salida.

-   Para determinar el tipo de conector físico al que corresponde un pin, llame al método [**IAMCrossbar::get \_ CrossbarPinInfo.**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-get_crossbarpininfo) El método devuelve un miembro de la [**enumeración PhysicalConnectorType.**](/windows/win32/api/strmif/ne-strmif-physicalconnectortype) Por ejemplo, un pin de S-Video devuelve el valor PhysConn \_ Video \_ SVideo.

    El **método \_ get CrossbarInfo** también indica si dos pines están relacionados entre sí. Por ejemplo, un pin de afinador de vídeo podría estar relacionado con un pin de audio. Los pines relacionados tienen la misma dirección de patilla y normalmente forman parte del mismo conector o conector físico de la tarjeta.

-   Para determinar si puede enrutar un pin de entrada a un pin de salida determinado, llame al [**método IAMCrossbar::CanRoute.**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-canroute)
-   Para determinar el enrutamiento actual entre los pines, llame al [**método IAMCrossbar::get \_ IsRoutedTo.**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-get_isroutedto)

Todos los métodos anteriores especifican pins por número de índice, con pins de salida y de entrada indexados desde cero. Llame al **método IAMCrossbar::get \_ PinCounts** para buscar el número de pines en el filtro.

Por ejemplo, el código siguiente muestra información sobre un filtro de barra cruzada en la ventana de consola:


```C++
// Helper function to associate a name with the type.
const char * GetPhysicalPinName(long lType)
{
    switch (lType) 
    {
    case PhysConn_Video_Tuner:            return "Video Tuner";
    case PhysConn_Video_Composite:        return "Video Composite";
    case PhysConn_Video_SVideo:           return "S-Video";
    case PhysConn_Video_RGB:              return "Video RGB";
    case PhysConn_Video_YRYBY:            return "Video YRYBY";
    case PhysConn_Video_SerialDigital:    return "Video Serial Digital";
    case PhysConn_Video_ParallelDigital:  return "Video Parallel Digital"; 
    case PhysConn_Video_SCSI:             return "Video SCSI";
    case PhysConn_Video_AUX:              return "Video AUX";
    case PhysConn_Video_1394:             return "Video 1394";
    case PhysConn_Video_USB:              return "Video USB";
    case PhysConn_Video_VideoDecoder:     return "Video Decoder";
    case PhysConn_Video_VideoEncoder:     return "Video Encoder";
        
    case PhysConn_Audio_Tuner:            return "Audio Tuner";
    case PhysConn_Audio_Line:             return "Audio Line";
    case PhysConn_Audio_Mic:              return "Audio Microphone";
    case PhysConn_Audio_AESDigital:       return "Audio AES/EBU Digital";
    case PhysConn_Audio_SPDIFDigital:     return "Audio S/PDIF";
    case PhysConn_Audio_SCSI:             return "Audio SCSI";
    case PhysConn_Audio_AUX:              return "Audio AUX";
    case PhysConn_Audio_1394:             return "Audio 1394";
    case PhysConn_Audio_USB:              return "Audio USB";
    case PhysConn_Audio_AudioDecoder:     return "Audio Decoder";
        
    default:                              return "Unknown Type";
    }    
}

void DisplayCrossbarInfo(IAMCrossbar *pXBar)
{
    HRESULT hr;
    long cOutput = -1, cInput = -1;
    hr = pXBar->get_PinCounts(&cOutput, &cInput);

    for (long i = 0; i < cOutput; i++)
    {
        long lRelated = -1, lType = -1, lRouted = -1;

        hr = pXBar->get_CrossbarPinInfo(FALSE, i, &lRelated, &lType);
        hr = pXBar->get_IsRouted(i, &lRouted);

        printf("Output pin %d: %s\n", i, GetPhysicalPinName(lType));
        printf("\tRelated out: %d, Routed in: %d\n", lRelated, lRouted);
        printf("\tSwitching Matrix: ");

        for (long j = 0; j < cInput; j++)
        {
            hr = pXBar->CanRoute(i, j);
            printf("%d-%s", j, (S_OK == hr ? "Yes" : "No"));
        }
        printf("\n\n");
    }

    for (i = 0; i < cInput; i++)
    {
        long lRelated = -1, lType = -1;

        hr = pXBar->get_CrossbarPinInfo(TRUE, i, &lRelated, &lType);

        printf("Input pin %d - %s\n", i, GetPhysicalPinName(lType));
        printf("\tRelated in: %d\n", lRelated);
    }
}
```



En el caso de una tarjeta hipotética, esta función podría generar la siguiente salida:


```C++
Output pin 0: S-Video
    Related out: 2, Routed in: 0
    Switching Matrix: 0-Yes 1-No 2-No 3-No
Output pin 1 - Video Tuner
    Related out: 2, Routed in: 1
    Switching Matrix: 0-No 1-Yes 2-No 3-No
Output pin 2 - Audio decoder
    Related out: 1, Routed in: -1
    Switching Matrix: 0-No 1-No 2-Yes 3-Yes

Input pin 0 - S-Video
    Related in: 2
Input pin 1 - Video Tuner
    Related in: 3
Input pin 2 - Audio line
    Related in: 0
Input pin 3 - Audio tuner
    Related in: 1
```



En el lado de salida, S-Video y el afinador de vídeo están relacionados con el descodificador de audio. En el lado de entrada, el afinador de vídeo está relacionado con el afinador de audio y S-Video está relacionado con la línea de audio de . La entrada S-Video se enruta a la salida de S-Video. y la entrada del afinador de vídeo se enruta a la salida del afinador de vídeo. Actualmente no se enruta nada al descodificador de audio, pero la línea de audio de o el afinador de audio se podrían enrutar a él.

Puede cambiar el enrutamiento existente llamando al [**método IAMCrossbar::Route.**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-route)

 

 



