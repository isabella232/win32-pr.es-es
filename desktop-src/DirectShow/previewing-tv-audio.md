---
description: Vista previa de audio de TV
ms.assetid: 25da8bcc-51c1-49f0-b4b5-885ff4f254d8
title: Vista previa de audio de TV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1cc63583c946d47ed744eacd51f0939ec852d53
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127254210"
---
# <a name="previewing-tv-audio"></a>Vista previa de audio de TV

Para obtener una vista previa del audio de televisión, enruta el pin descodificador de audio del filtro de barra cruzada al pin Audio Tuner (Audio Tuner). Para silenciar el audio, enruta el pin descodificador de audio a -1, como se muestra en el diagrama siguiente. (Los filtros de barras cruzadas se describen [en Trabajar con barras cruzadas).](working-with-crossbars.md)

![enrutamiento del pin del descodificador de audio](images/vidcap07.png)

El enfoque básico es el siguiente:

1.  Use el [**método ICaptureGraphBuilder2::FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) para buscar el filtro de barra cruzada.
2.  Use el [**método IAMCrossbar::get \_ CrossbarPinInfo**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-get_crossbarpininfo) para enumerar los pines de entrada y salida del filtro de barra cruzada. Busque un pin de salida de descodificador de audio y un pin de entrada de audio.
3.  Si encuentra los pines correctos, llame a [**IAMCrossbar::Route**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-route) para enrutar los pines. Si no es así, busque otra barra cruzada y repita el proceso.
4.  Para silenciar el audio, enruta el pin del descodificador de audio a -1.

La mayoría de los tuners de TV usan un único filtro de barra cruzada, pero algunos usan dos filtros de barra cruzada. Por lo tanto, es posible que tenga que buscar una segunda barra cruzada si se produce un error en la primera.

> [!Note]  
> Al contrario de lo que podría esperar, no se requiere ningún filtro de captura de audio ni representador de audio para obtener una vista previa del audio, ya que hay una conexión física entre la tarjeta de tuner y la tarjeta de sonido.

 

En el código siguiente se muestran estos pasos con más detalle. En primer lugar, esta es una función auxiliar que busca un tipo de pin especificado en un filtro de barra cruzada:


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



La siguiente función intenta activar o silenciar el audio, en función del valor del *parámetro bActivate.* Busca los pines necesarios en el filtro de barra cruzada especificado. Si no los encuentra, devuelve un código de error.


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



La función siguiente busca un filtro de barra cruzada en el gráfico de filtros. Si encuentra uno, intenta activar o silenciar el audio (mediante la función anterior). Si se produce un error en esa operación, el método busca una segunda barra cruzada en sentido ascendente e intenta de nuevo. Para obtener un enfoque más generalizado para administrar varios filtros de barras cruzadas en un gráfico, consulte la clase CCrossbar en la aplicación de ejemplo AmCap.


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



El código siguiente muestra cómo llamar a estas funciones:


```C++
// Build the analog TV graph (not shown).
// Activate the audio.
hr = ActivateAudio(pBuild, pCap, TRUE);
// Later, mute the audio.
hr = ActivateAudio(pBuild, pCap, FALSE);
```



Tenga en cuenta que estas funciones de ejemplo repiten muchas de las mismas llamadas de función. Por ejemplo, enumera los pines de barra cruzada cada vez. En una aplicación real, puede almacenar en caché parte de esta información.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Audio de televisión análoga](analog-television-audio.md)
</dt> <dt>

[Trabajar con barras cruzadas](working-with-crossbars.md)
</dt> </dl>

 

 



