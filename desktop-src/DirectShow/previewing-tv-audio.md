---
description: Obtener una vista previa del audio de TV
ms.assetid: 25da8bcc-51c1-49f0-b4b5-885ff4f254d8
title: Obtener una vista previa del audio de TV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1cc63583c946d47ed744eacd51f0939ec852d53
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494866"
---
# <a name="previewing-tv-audio"></a>Obtener una vista previa del audio de TV

Para obtener una vista previa del audio de TV, enrute el PIN del descodificador de audio en el filtro de barras cruzadas al pin de sintonizador de audio. Para silenciar el audio, enrute el PIN del descodificador de audio a-1, tal como se muestra en el diagrama siguiente. (Los filtros de barras cruzadas se describen en [trabajar con barras cruzadas](working-with-crossbars.md)).

![enrutamiento del PIN del descodificador de audio](images/vidcap07.png)

El enfoque básico es el siguiente:

1.  Use el método [**ICaptureGraphBuilder2:: FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) para buscar el filtro de barras cruzadas.
2.  Use el método [**IAMCrossbar:: get \_ CrossbarPinInfo**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-get_crossbarpininfo) para enumerar los pines de entrada y salida del filtro de barras cruzadas. Busque un PIN de salida de descodificador de audio y un PIN de entrada de sintonizador de audio.
3.  Si encuentra los pin correctos, llame a [**IAMCrossbar:: Route**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-route) para enrutar los pin. Si no es así, busque el flujo ascendente de otra Cruz y repita el proceso.
4.  Para silenciar el audio, enrute el PIN del descodificador de audio a-1.

La mayoría de los sintonizadores de TV usan un solo filtro de barras cruzadas, pero algunos usan dos filtros de barras cruzadas. Por lo tanto, es posible que tenga que buscar una segunda cruz si se produce un error en la primera.

> [!Note]  
> Contrariamente a lo que cabría esperar, no se requiere ningún filtro de captura de audio o representador de audio para obtener una vista previa del audio, ya que hay una conexión física entre la tarjeta sintonizadora y la tarjeta de sonido.

 

En el código siguiente se muestran estos pasos con más detalle. En primer lugar, se trata de una función auxiliar que busca un filtro de cruz para un tipo de PIN especificado:


```C++
HRESULT FindCrossbarPin(
    IAMCrossbar *pXBar,                 // Pointer to the crossbar.
    PhysicalConnectorType PhysicalType, // Pin type to match.
    PIN_DIRECTION Dir,                  // Pin direction.
    long *pIndex)       // Receives the index of the pin, if found.
{
    BOOL bInput = (Dir == PINDIR_INPUT ? TRUE : FALSE);

    // Find out how many pins the crossbar has.
    long cOut, cIn;
    HRESULT hr = pXBar->get_PinCounts(&cOut, &cIn);
    if (FAILED(hr)) return hr;
    // Enumerate pins and look for a matching pin.
    long count = (bInput ? cIn : cOut);
    for (long i = 0; i < count; i++)
    {
        long iRelated = 0;
        long ThisPhysicalType = 0;
        hr = pXBar->get_CrossbarPinInfo(bInput, i, &iRelated,
            &ThisPhysicalType);
        if (SUCCEEDED(hr) && ThisPhysicalType == PhysicalType)
        {
            // Found a match, return the index.
            *pIndex = i;
            return S_OK;
        }
    }
    // Did not find a matching pin.
    return E_FAIL;
}
```



La función siguiente intenta activar o desactivar el audio, dependiendo del valor del parámetro *bActivate* . Busca los pin necesarios en el filtro de barras cruzadas especificado. Si no se encuentra, devuelve un código de error.


```C++
HRESULT ConnectAudio(IAMCrossbar *pXBar, BOOL bActivate)
{
    // Look for the Audio Decoder output pin.
    long i = 0;
    HRESULT hr = FindCrossbarPin(pXBar, PhysConn_Audio_AudioDecoder,
        PINDIR_OUTPUT, &i);
    if (SUCCEEDED(hr))
    {
        if (bActivate)  // Activate the audio. 
        {
            // Look for the Audio Tuner input pin.
            long j = 0;
            hr = FindCrossbarPin(pXBar, PhysConn_Audio_Tuner, 
                PINDIR_INPUT, &j);
            if (SUCCEEDED(hr))
            {
                return pXBar->Route(i, j);
            }
        }
        else  // Mute the audio
        {
            return pXBar->Route(i, -1);
        }
    }
    return E_FAIL;
}
```



La función siguiente busca un filtro de barras cruzadas en el gráfico de filtro. Si encuentra uno, intenta activar o desactivar el audio (con la función anterior). Si se produce un error en esa operación, el método busca una segunda cruz y vuelve a intentarlo. Para obtener un enfoque más generalizado para administrar varios filtros de barras cruzadas en un gráfico, vea la clase CCrossbar en la aplicación de ejemplo AmCap.


```C++
HRESULT ActivateAudio(ICaptureGraphBuilder2 *pBuild, IBaseFilter *pSrc,
  BOOL bActivate)
{
    // Search upstream for a crossbar.
    IAMCrossbar *pXBar1 = NULL;
    HRESULT hr = pBuild->FindInterface(&LOOK_UPSTREAM_ONLY, NULL, pSrc,
        IID_IAMCrossbar, (void**)&pXBar1);
    if (SUCCEEDED(hr)) 
    {
        hr = ConnectAudio(pXBar1, bActivate);
        if (FAILED(hr))
        {
            // Look for another crossbar.
            IBaseFilter *pF = NULL;
            hr = pXBar1->QueryInterface(IID_IBaseFilter, (void**)&pF);
            if (SUCCEEDED(hr)) 
            {
                // Search upstream for another one.
                IAMCrossbar *pXBar2 = NULL;
                hr = pBuild->FindInterface(&LOOK_UPSTREAM_ONLY, NULL, pF,
                    IID_IAMCrossbar, (void**)&pXBar2);
                pF->Release();
                if (SUCCEEDED(hr))
                {
                    hr = ConnectAudio(pXBar2, bActivate);
                    pXBar2->Release();
                }
            }
        }
        pXBar1->Release();
    }
    return hr;
}
```



En el código siguiente se muestra cómo llamar a estas funciones:


```C++
// Build the analog TV graph (not shown).
// Activate the audio.
hr = ActivateAudio(pBuild, pCap, TRUE);
// Later, mute the audio.
hr = ActivateAudio(pBuild, pCap, FALSE);
```



Tenga en cuenta que estas funciones de ejemplo repiten muchas de las llamadas a funciones. Por ejemplo, enumeran las barras cruzadas cada vez. En una aplicación real, puede almacenar en caché parte de esta información.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Audio analógico de televisión](analog-television-audio.md)
</dt> <dt>

[Trabajar con barras cruzadas](working-with-crossbars.md)
</dt> </dl>

 

 



