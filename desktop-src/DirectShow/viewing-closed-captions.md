---
description: Ver subtítulos (CC)
ms.assetid: 86c0c553-af35-4ad1-8918-63d9e4577c73
title: Ver subtítulos (CC)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82ff2d6d213259ccce6e9b02272d0c9db3ad7b71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104569712"
---
# <a name="viewing-closed-captions"></a>Ver subtítulos (CC)

Para admitir subtítulos (CC) en televisión analógica, el filtro de captura expone un PIN que proporciona datos de subtítulos o de subtítulos cerrados. El PIN tendrá una de las siguientes categorías de PIN:

-   PIN de VBI ( \_ categoría de PIN \_ VBI). Proporciona una secuencia de ejemplos de perfiles de onda de VBI. Estos se pasan a un filtro de descodificador que extrae los datos de subtítulos.
-   PIN CC (categoría de PIN \_ \_ CC). Proporciona pares de bytes de subtítulos cerrados, extraídos de los datos de la línea 21.
-   División de hardware de la segmentación CC ( \_ captura de CC de vídeo PINNAME \_ \_ ).

Para obtener una vista previa de los subtítulos cerrados, llame a [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) con la categoría de PIN de VBI y, si se produce un error, vuelva a llamarlo con la categoría CC.


```C++
hr = pBuild->RenderStream(&PIN_CATEGORY_VBI, 0, pCap, 0, 0);
if (FAILED(hr))
{
    hr = pBuild->RenderStream(&PIN_CATEGORY_CC, 0, pCap, 0, 0);
}
```



En el diagrama siguiente se muestra un gráfico de filtros típico para mostrar subtítulos cerrados.

![gráfico de vista previa de subtítulos (CC)](images/vidcap08.png)

En este gráfico se usan los siguientes filtros para la presentación de subtítulos:

-   [Convertidor Tee/Sink-to-Sink](tee-sink-to-sink-converter.md). Acepta la información de VBI del filtro de captura y la divide en secuencias independientes para cada uno de los servicios de datos presentes en la señal. Microsoft proporciona códecs VBI para el título cerrado, NABTS y teletexto universal estándar (elemento WST).
-   [Descodificador de CC](cc-decoder-filter.md). Descodifica los datos de CC de las forma de onda VBI muestreadas proporcionadas por el filtro de captura.
-   [Descodificador de línea 21](line-21-decoder-filter.md). Traduce los pares de bytes de CC y dibuja el texto de la leyenda en mapas de bits. El filtro de nivel inferior (en este caso, el mezclador de superposición) superpone los mapas de bits al vídeo.

El método [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) del generador de gráficos de captura agrega estos filtros automáticamente. Si el filtro de captura tiene un PIN de CC en lugar de un PIN de VBI, el PIN de CC se conecta directamente al filtro de descodificador de línea 21.

> [!Note]  
> Si usa el filtro de representador de mezcla de vídeo (VMR) para la representación, use el filtro de descodificador de línea 21 2. Este filtro tiene la misma funcionalidad que el descodificador de línea 21, pero el CLSID es CLSID \_ Line21Decoder2.

 

> [!Note]  
> El filtro del descodificador de CC se quitó en Windows Vista. Las nuevas aplicaciones deben usar el filtro VBICodec, que se documenta en la documentación de las tecnologías de Microsoft TV.

 

Si el dispositivo de captura usa un puerto de vídeo, el filtro de captura podría tener un PIN de puerto de vídeo VBI (categoría de PIN de \_ \_ videopuerto \_ VBI). Este pin debe estar conectado al filtro de [asignador de superficie de VBI](vbi-surface-allocator.md) , que asigna superficies para almacenar los datos de VBI capturados. El método [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) agrega este filtro si es necesario. En el diagrama siguiente se muestra un gráfico de filtros con el asignador de superficie de VBI.

![gráfico de vista previa de subtítulos (CC) con asignador de superficie de VBI](images/vidcap09.png)

### <a name="enabling-and-disabling-the-captions"></a>Habilitar y deshabilitar los títulos

Para controlar la presentación de subtítulos, use la interfaz [**IAMLine21Decoder**](/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder) en el filtro del descodificador line 21. Por ejemplo, puede desactivar la presentación de subtítulos mediante el método [**IAMLine21Decoder:: SetServiceState**](/previous-versions/windows/desktop/api/il21dec/nf-il21dec-iamline21decoder-setservicestate) , como se indica a continuación:


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



En este ejemplo se usa el método [**ICaptureGraphBuilder2:: FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) para buscar la interfaz [**IAMLine21Decoder**](/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder) . El primer parámetro de **FindInterface** es **&look \_ downstream \_ Only**, que especifica que se busque downstream desde el filtro de captura (*pCap*).

### <a name="capturing-closed-caption-bitmaps"></a>Captura de mapas de bits de subtítulos cerrados

Puede capturar los mapas de bits de los títulos en un archivo. Para ello, agregue la sección de escritura de archivos del gráfico de filtros, como se describe en [capturar vídeo en un archivo](capturing-video-to-a-file.md). A continuación, represente el PIN de CC o VBI en el filtro MUX:


```C++
hr = pBuild->RenderStream(&PIN_CATEGORY_VBI, 0, pCap, 0, pMux);
if (FAILED(hr))
{
    hr = pBuild->RenderStream(&PIN_CATEGORY_CC, 0, pCap, 0, pMux);
}
```



Si también va a capturar el vídeo, se creará un archivo con dos secuencias de vídeo independientes. No capturará vídeo con títulos superpuestos encima de la imagen.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Subtítulos y teletexto](closed-captions-and-teletext.md)
</dt> </dl>

 

 



