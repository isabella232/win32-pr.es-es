---
description: Ver teletexto estándar del mundo
ms.assetid: 99b3395b-8775-4fe8-b173-187fa359978f
title: Ver teletexto estándar del mundo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f9b0885c08403de9578a8dee1eca6e000408ee5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360474"
---
# <a name="viewing-world-standard-teletext"></a>Ver teletexto estándar del mundo

> [!Note]  
> Esta funcionalidad se ha quitado de Windows Vista y sistemas operativos posteriores. Está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.

 

El teletexto estándar universal (elemento WST) está codificado en el intervalo de blanking vertical (VBI) de la señal de televisión analógica. El gráfico de filtro para obtener una vista previa del teletexto es similar al gráfico que se usa para ver los subtítulos cerrados. En el siguiente diagrama se ilustra este gráfico.

![gráfico de vista previa de elemento WST](images/vidcap10.png)

En este gráfico se usan los siguientes filtros para la visualización de elemento WST:

-   [Convertidor Tee/Sink-to-Sink](tee-sink-to-sink-converter.md). Acepta la información de VBI del filtro de captura y la divide en secuencias independientes para cada uno de los servicios de datos presentes en la señal.
-   [Códec elemento WST](wst-codec-filter.md). Descodifica los datos de teletexto de los ejemplos de VBI.
-   [Descodificador de elemento WST](wst-decoder-filter.md). Traduce los datos de teletexto y dibuja el texto en mapas de bits. El filtro de nivel inferior (en este caso, el mezclador de superposición) superpone los mapas de bits al vídeo.

El método **RenderStream** del generador de gráficos de captura no admite directamente los filtros elemento WST, por lo que la aplicación debe realizar algún trabajo adicional.

1.  Agregue el filtro de mezclador de superposición al gráfico de filtro. En el código siguiente se usa la función AddFilterByCLSID que se describe en [Agregar un filtro por CLSID](add-a-filter-by-clsid.md). (AddFilterByCLSID no es una API de DirectShow).
    ```C++
    IBaseFilter *pOvMix = NULL;  // Pointer to the Overlay Mixer filter.
    hr = AddFilterByCLSID(pGraph, CLSID_OverlayMixer, L"OVMix", &pOvMix);
    if (FAILED(hr)) 
    {
        // Handle the error ...
    }
    ```

    

2.  Conecte el PIN de vista previa al filtro de representador de vídeo a través del mezclador de superposición. Puede usar el método **RenderStream** , como se indica a continuación:
    ```C++
    hr = pBuild->RenderStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, 
        pCap, pOvMix, 0);
    ```

    

3.  Agregue el filtro de convertidor Tee/Sink-to-Sink al gráfico de filtro. En el código siguiente se usa la función CreateKernelFilter que se describe en [crear Kernel-Mode filtros](creating-kernel-mode-filters.md). (CreateKernelFilter no es una API de DirectShow).
    ```C++
    IBaseFilter* pKernelTee = NULL;
    hr = CreateKernelFilter(AM_KSCATEGORY_SPLITTER, 
        OLESTR("Tee/Sink-to-Sink Converter"), &pKernelTee);
    if (SUCCEEDED(hr))
    {
        hr = pGraph->AddFilter(pKernelTee, L"Kernel Tee");
    }
    ```

    

4.  Agregue el filtro de códec elemento WST al gráfico de filtros:
    ```C++
    IBaseFilter* pWstCodec = NULL;
    hr = CreateKernelFilter(AM_KSCATEGORY_VBICODEC, 
        OLESTR("WST Codec"), &pWstCodec);
    if (SUCCEEDED(hr))
    {
        hr = pGraph->AddFilter(pWstCodec, L"WST Codec");
    }
    ```

    

5.  Llame a **RenderStream** para conectar el PIN VBI del filtro de captura al convertidor Tee/Sink-to-Sink y el convertidor Tee/Sink-to-Sink al filtro de códec elemento WST:
    ```C++
    hr = pBuild->RenderStream(&PIN_CATEGORY_VBI, 0, pCap, 
        pKernelTee, pWstCodec);
    ```

    

6.  Vuelva a llamar a **RenderStream** para conectar el filtro de códec elemento WST al mezclador de superposición. El filtro del descodificador de elemento WST se incorpora automáticamente al gráfico.
    ```C++
    hr = pBuild->RenderStream(0, 0, pWstCodec, 0, pOvMix);
    ```

    

7.  Recuerde liberar todas las interfaces de filtro.
    ```C++
    pOvMix->Release();
    pKernelTee->Release();
    pWstCodec->Release();
    ```

    

> [!Note]  
> Actualmente, el filtro del descodificador de elemento WST no admite conexiones al filtro de representador de mezcla de vídeo (VMR). Por lo tanto, debe usar el filtro de representador de vídeo heredado para ver el teletexto.

 

Si el filtro de captura tiene un PIN de puerto de vídeo VBI (PIN \_ CATEGPORY \_ videopuerto \_ VBI), conéctelo al filtro de [asignador de superficie de VBI](vbi-surface-allocator.md) . De lo contrario, el gráfico no se ejecutará correctamente. En el ejemplo de código siguiente se usa la función AddFilterByCLSID, que se describe en [Agregar un filtro por CLSID](add-a-filter-by-clsid.md)y la función FindPinByCategory, que se describe en [trabajar con categorías de PIN](working-with-pin-categories.md). (Ninguna de las funciones es una API de DirectShow).


```C++
// Look for a video port VBI pin on the capture filter.
IPin *pVPVBI = NULL;
hr = FindPinByCategory(pCap, PINDIR_OUTPUT, 
    PIN_CATEGORY_VIDEOPORT_VBI, &pVPVBI);
if (FAILED(hr))
{
    // No video port VBI pin; nothing else to do. OK to run the graph.
}
else
{
    // Found one. Connect it to the VBI Surface Allocator.
    IBaseFilter *pSurf = NULL;
    hr = AddFilterByCLSID(pGraph, CLSID_VBISurfaces, L"VBI Surf", &pSurf);
    if (SUCCEEDED(hr))
    {
        hr = pBuild->RenderStream(NULL, NULL, pVPVBI, 0, pSurf);
        pSurf->Release();
    }
    if (FAILED(hr))
    {
        // Handle the error (not shown). It is probably not safe to 
        // run the graph at this point.
    }
    pVPVBI->Release();
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Subtítulos y teletexto](closed-captions-and-teletext.md)
</dt> </dl>

 

 



