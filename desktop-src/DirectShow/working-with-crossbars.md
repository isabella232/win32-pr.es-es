---
description: Trabajar con barras cruzadas
ms.assetid: 6e8ee9c3-6776-498b-ad38-36f8172a27ae
title: Trabajar con barras cruzadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3d3a1c43703ac662d44854b0fc6bad8b280c368
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688602"
---
# <a name="working-with-crossbars"></a>Trabajar con barras cruzadas

Si una tarjeta de captura de vídeo tiene más de una entrada física o admite más de una ruta de acceso de hardware para los datos, el gráfico de filtros puede contener el [filtro de barras de vídeo analógicas](analog-video-crossbar-filter.md). El generador de gráficos de captura agrega automáticamente este filtro cuando sea necesario. será ascendente desde el filtro de captura. Dependiendo del hardware, el gráfico de filtros podría contener más de una instancia del filtro de barras cruzadas.

El filtro de barras cruzadas expone la interfaz [**IAMCrossbar**](/windows/desktop/api/Strmif/nn-strmif-iamcrossbar) , que puede usar para enrutar una entrada determinada a una salida determinada. Por ejemplo, una tarjeta de vídeo puede tener un conector coaxial y una entrada de S-video. Se representarán como clavijas de entrada en el filtro de barras cruzadas. Para seleccionar una entrada, enrute el PIN de entrada correspondiente a la clavija de salida de las barras cruzadas mediante el método [**IAMCrossbar:: Route**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-route) .

Para buscar los filtros de barras cruzadas en el gráfico, puede usar el método [**ICaptureGraphBuilder2:: FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) para buscar filtros que admitan **IAMCrossbar**. Por ejemplo, el código siguiente busca dos barras cruzadas:


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



Para obtener un enfoque más generalizado, consulte la clase CCrossbar en el [ejemplo AMCAP](amcap-sample.md).

Una vez que tenga un puntero a la interfaz **IAMCrossbar** , puede obtener información sobre el filtro de barras cruzadas, incluido el tipo físico de cada pin, y la matriz de los pines de entrada que se pueden enrutar a los terminales de salida.

-   Para determinar el tipo de conector físico al que corresponde un PIN, llame al método [**IAMCrossbar:: get \_ CrossbarPinInfo**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-get_crossbarpininfo) . El método devuelve un miembro de la enumeración [**PhysicalConnectorType**](/windows/win32/api/strmif/ne-strmif-physicalconnectortype) . Por ejemplo, un PIN de S-video devuelve el valor PhysConn \_ video \_ Svideo.

    El método **Get \_ CrossbarInfo** también indica si dos patillas están relacionadas entre sí. Por ejemplo, un PIN de sintonizador de vídeo puede estar relacionado con un PIN de sintonizador de audio. Los pin relacionados tienen la misma dirección del PIN y normalmente forman parte del mismo conector físico o conector de la tarjeta.

-   Para determinar si puede enrutar un PIN de entrada a un determinado PIN de salida, llame al método [**IAMCrossbar:: CanRoute**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-canroute) .
-   Para determinar el enrutamiento actual entre los pin, llame al método [**IAMCrossbar:: get \_ IsRoutedTo**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-get_isroutedto) .

Los métodos anteriores especifican los pin por número de índice, con clavijas de salida y clavijas de entrada indizadas a partir de cero. Llame al método **IAMCrossbar:: get \_ PinCounts** para buscar el número de PIN en el filtro.

Por ejemplo, el código siguiente muestra información sobre un filtro de barras cruzadas en la ventana de la consola:


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



En el caso de una tarjeta hipotética, esta función podría generar el siguiente resultado:


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



En el lado de salida, los elementos de vídeo y sintonizador de vídeo están relacionados con el descodificador de audio. En el lado de entrada, el sintonizador de vídeo está relacionado con el sintonizador de audio y el S-video está relacionado con la línea de audio en. La entrada S-video se enruta a la salida S-video; y la entrada del sintonizador de vídeo se enruta a la salida del sintonizador de vídeo. Actualmente no se enruta nada al descodificador de audio, pero la línea de audio o el sintonizador de audio se pueden enrutar a él.

Puede cambiar el enrutamiento existente llamando al método [**IAMCrossbar:: Route**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-route) .

 

 



