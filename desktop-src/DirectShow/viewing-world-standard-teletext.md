---
description: Visualización del texto teletexto estándar del mundo
ms.assetid: 99b3395b-8775-4fe8-b173-187fa359978f
title: Visualización del texto teletexto estándar del mundo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2129538d91a7ac48fea26fd5f1987473896760c164fb3e2b1d4a2b1d142a1f04
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078555"
---
# <a name="viewing-world-standard-teletext"></a>Visualización del texto teletexto estándar del mundo

> [!Note]  
> Esta funcionalidad se ha quitado de Windows Vista y sistemas operativos posteriores. Está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.

 

El teletexto estándar del mundo (WST) se codifica en el intervalo de espacio en blanco vertical (VBI) de la señal de televisión análoga. El gráfico de filtro para obtener una vista previa del teletexto es similar al gráfico que se usa para ver los títulos cerrados. En el diagrama siguiente se muestra este gráfico.

![wst preview graph](images/vidcap10.png)

Este gráfico usa los siguientes filtros para la presentación de WST:

-   [Convertidor de tee/sink-to-sink](tee-sink-to-sink-converter.md). Acepta la información de VBI del filtro de captura y la divide en secuencias independientes para cada uno de los servicios de datos presentes en la señal.
-   [Códec WST](wst-codec-filter.md). Descodifica los datos de teletexto de los ejemplos de VBI.
-   [Descodificador WST](wst-decoder-filter.md). Traduce los datos de teletexto y dibuja el texto en mapas de bits. El filtro de nivel inferior (en este caso, la propiedad Overlay Mixer) superpone los mapas de bits en el vídeo.

El método **RenderStream** de Capture Graph Builder no admite directamente los filtros WST, por lo que la aplicación debe realizar algún trabajo adicional.

1.  Agregue el filtro Overlay Mixer al gráfico de filtros. El código siguiente usa la función AddFilterByCLSID descrita en [Agregar un filtro por CLSID.](add-a-filter-by-clsid.md) (AddFilterByCLSID no es DirectShow API).
    ```C++
    IBaseFilter *pOvMix = NULL;  // Pointer to the Overlay Mixer filter.
    hr = AddFilterByCLSID(pGraph, CLSID_OverlayMixer, L"OVMix", &pOvMix);
    if (FAILED(hr)) 
    {
        // Handle the error ...
    }
    ```

    

2.  Conectar el pin de vista previa al filtro Representador de vídeo a través de la ventana Superposición Mixer. Puede usar el **método RenderStream,** como se muestra a continuación:
    ```C++
    hr = pBuild->RenderStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, 
        pCap, pOvMix, 0);
    ```

    

3.  Agregue el filtro Tee/Sink-to-Sink Converter al gráfico de filtros. En el código siguiente se usa la función CreateKernelFilter que se describe en [Creación de Kernel-Mode filtros](creating-kernel-mode-filters.md). (CreateKernelFilter no es una API DirectShow).
    ```C++
    IBaseFilter* pKernelTee = NULL;
    hr = CreateKernelFilter(AM_KSCATEGORY_SPLITTER, 
        OLESTR("Tee/Sink-to-Sink Converter"), &pKernelTee);
    if (SUCCEEDED(hr))
    {
        hr = pGraph->AddFilter(pKernelTee, L"Kernel Tee");
    }
    ```

    

4.  Agregue el filtro códec WST al gráfico de filtros:
    ```C++
    IBaseFilter* pWstCodec = NULL;
    hr = CreateKernelFilter(AM_KSCATEGORY_VBICODEC, 
        OLESTR("WST Codec"), &pWstCodec);
    if (SUCCEEDED(hr))
    {
        hr = pGraph->AddFilter(pWstCodec, L"WST Codec");
    }
    ```

    

5.  Llame **a RenderStream** para conectar el pin de VBI del filtro de captura al convertidor tee/sink-to-sink y al convertidor de receptor a receptor con el filtro de códec WST:
    ```C++
    hr = pBuild->RenderStream(&PIN_CATEGORY_VBI, 0, pCap, 
        pKernelTee, pWstCodec);
    ```

    

6.  Vuelva **a llamar a RenderStream** para conectar el filtro de códec WST al filtro Overlay Mixer. El filtro descodificador de WST se incluye automáticamente en el gráfico.
    ```C++
    hr = pBuild->RenderStream(0, 0, pWstCodec, 0, pOvMix);
    ```

    

7.  No olvide liberar todas las interfaces de filtro.
    ```C++
    pOvMix->Release();
    pKernelTee->Release();
    pWstCodec->Release();
    ```

    

> [!Note]  
> Actualmente, el filtro descodificador WST no admite conexiones con el filtro de representador de mezcla de vídeo (VMR). Por lo tanto, debe usar el filtro representador de vídeo heredado para ver el teletexto.

 

Si el filtro de captura tiene un pin de VBI de puerto de vídeo (PIN \_ CATEGPORY \_ VIDEOPORT \_ VBI), conéctelo al filtro Asignador de superficie de [VBI.](vbi-surface-allocator.md) De lo contrario, el gráfico no se ejecutará correctamente. En el ejemplo de código siguiente se usa la función AddFilterByCLSID, descrita en Agregar un filtro por [CLSID](add-a-filter-by-clsid.md)y la función FindPinByCategory, que se describe en Trabajar con categorías de [pin](working-with-pin-categories.md). (Ninguna de las funciones es DirectShow API).


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

 

 



