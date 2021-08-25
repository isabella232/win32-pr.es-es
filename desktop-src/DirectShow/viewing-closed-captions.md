---
description: Visualización de subtítulos
ms.assetid: 86c0c553-af35-4ad1-8918-63d9e4577c73
title: Visualización de subtítulos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f52288b1c4fa5c43f7e0419d81bd9727a4db86848d368b600e1d713c53dc1593
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903444"
---
# <a name="viewing-closed-captions"></a>Visualización de subtítulos

Para admitir subtítulos en televisión análoga, el filtro de captura expone un pin que proporciona datos de título cerrado o VBI. El pin tendrá una de las siguientes categorías de pin:

-   Pin de VBI (PIN \_ CATEGORY \_ VBI). Proporciona una secuencia de muestras de forma de onda de VBI. Se pasan a un filtro de descodificador que extrae los datos de subtítulos.
-   CC pin (PIN \_ CATEGORY \_ CC). Proporciona pares de bytes de subtítulos, extraídos de los datos de línea 21.
-   Pin CC de cortar hardware (PINNAME \_ VIDEO \_ CC \_ CAPTURE).

Para obtener una vista previa de los subtítulos, llame a [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) con la categoría de pin de VBI y, si se produce un error, vuelva a llamarlo con la categoría CC.


```C++
hr = pBuild->RenderStream(&PIN_CATEGORY_VBI, 0, pCap, 0, 0);
if (FAILED(hr))
{
    hr = pBuild->RenderStream(&PIN_CATEGORY_CC, 0, pCap, 0, 0);
}
```



En el diagrama siguiente se muestra un gráfico de filtros típico para mostrar subtítulos.

![gráfico de versión preliminar de subtítulos](images/vidcap08.png)

Este gráfico usa los siguientes filtros para la presentación de subtítulos:

-   [Convertidor de tee/sink-to-sink](tee-sink-to-sink-converter.md). Acepta la información de VBI del filtro de captura y la divide en secuencias independientes para cada uno de los servicios de datos presentes en la señal. Microsoft proporciona códecs VBI para subtítulos, MPEGTS y teletexto estándar mundial (WST).
-   [Descodificador CC](cc-decoder-filter.md). Descodifica datos CC de las formas de onda de VBI muestreadas proporcionadas por el filtro de captura.
-   [Descodificador de línea 21.](line-21-decoder-filter.md) Traduce los pares de bytes CC y dibuja el texto del título en mapas de bits. El filtro de nivel inferior (en este caso, la propiedad Overlay Mixer) superpone los mapas de bits en el vídeo.

El método [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) de Capture Graph Builder agrega estos filtros automáticamente. Si el filtro de captura tiene un pin CC en lugar de un pin de VBI, el pin CC se conecta directamente al filtro Descodificador de línea 21.

> [!Note]  
> Si usa el filtro Representador de mezcla de vídeo (VMR) para la representación, use el filtro descodificador de línea 21 2. Este filtro tiene la misma funcionalidad que el descodificador de línea 21, pero el CLSID es CLSID \_ Line21Decoder2.

 

> [!Note]  
> El filtro descodificador CC se quitó en Windows Vista. Las nuevas aplicaciones deben usar el filtro VBICodec, que se documenta en la documentación de Microsoft TV Technologies.

 

Si el dispositivo de captura usa un puerto de vídeo, el filtro de captura podría tener un pin de VBI de puerto de vídeo (PIN \_ CATEGORY \_ VIDEOPORT \_ VBI). Este pin debe estar conectado al filtro Asignador de superficie de [VBI,](vbi-surface-allocator.md) que asigna superficies para contener los datos de VBI capturados. El [**método RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) agrega este filtro si es necesario. En el diagrama siguiente se muestra un gráfico de filtros con el asignador de superficie de VBI.

![gráfico de versión preliminar de subtítulos con asignador de superficie de vbi](images/vidcap09.png)

### <a name="enabling-and-disabling-the-captions"></a>Habilitación y deshabilitación de los títulos

Para controlar la pantalla de subtítulos, use la [**interfaz IAMLine21Decoder**](/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder) en el filtro Descodificador de línea 21. Por ejemplo, puede desactivar la presentación de subtítulos mediante el método [**IAMLine21Decoder::SetServiceState,**](/previous-versions/windows/desktop/api/il21dec/nf-il21dec-iamline21decoder-setservicestate) como se muestra a continuación:


```C++
// Use the FindInterface method to find the interface.
IAMLine21Decoder *pLine21 = NULL;
hr = pBuild->FindInterface(
    &LOOK_DOWNSTREAM_ONLY, // Look downstream from pCap 
    NULL,                  // No particular media type
    pCap,                  // Pointer to the capture filter.
    IID_IAMLine21Decoder, (void**)&pLine21);
if (SUCCEEDED(hr))
{
    pLine21->SetServiceState(AM_L21_CCSTATE_Off);
    // (Use AM_L21_CCSTATE_On to enable.)
    pLine21->Release();
}
```



En este ejemplo se [**usa el método ICaptureGraphBuilder2::FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) para buscar la [**interfaz IAMLine21Decoder.**](/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder) El primer parámetro de **FindInterface** **es&LOOK \_ DOWNSTREAM \_ ONLY**, que especifica que se busque de bajada desde el filtro de captura (*pCap*).

### <a name="capturing-closed-caption-bitmaps"></a>Captura de mapas de bits de subtítulos

Puede capturar los mapas de bits de título en un archivo. Para ello, agregue la sección de escritura de archivos del gráfico de filtros, como se describe en [Captura de vídeo en un archivo](capturing-video-to-a-file.md). A continuación, represente el pin CC o VBI en el filtro mux:


```C++
hr = pBuild->RenderStream(&PIN_CATEGORY_VBI, 0, pCap, 0, pMux);
if (FAILED(hr))
{
    hr = pBuild->RenderStream(&PIN_CATEGORY_CC, 0, pCap, 0, pMux);
}
```



Si también captura el vídeo, se creará un archivo con dos secuencias de vídeo independientes. No capturará vídeo con subtítulos superados en la parte superior de la imagen.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Subtítulos y teletexto](closed-captions-and-teletext.md)
</dt> </dl>

 

 



