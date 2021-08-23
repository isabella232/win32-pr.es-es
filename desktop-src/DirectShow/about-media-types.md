---
description: Obtenga información sobre los tipos de medios en DirectShow. El tipo de medio es una manera universal y extensible de describir formatos de medios digitales.
ms.assetid: 9984ba36-4e43-4886-a073-34b330274c9c
title: Acerca de los tipos de medios (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fa3034581e443472f1b73c0bc42ca7b8b532a18120df3e067b02ad16f37930e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074899"
---
# <a name="about-media-types-directshow"></a>Acerca de los tipos de medios (DirectShow)

Dado DirectShow es modular, requiere una manera de describir el formato de los datos en cada punto del gráfico de filtro. Por ejemplo, considere la posibilidad de reproducir AVI. Los datos entran en el gráfico como una secuencia de fragmentos de RIFF. Se analizan en secuencias de audio y vídeo. La secuencia de vídeo consta de fotogramas de vídeo, que probablemente estén comprimidos. Después de la decodificación, la secuencia de vídeo es una serie de mapas de bits sin comprimir. La secuencia de audio pasa por un proceso similar.

Tipos de medios: cómo DirectShow los formatos

El *tipo de medio* es una manera universal y extensible de describir formatos de medios digitales. Cuando se conectan dos filtros, se ponen de acuerdo en un tipo de medio. El tipo de medio identifica el tipo de datos que el filtro ascendente entregará al filtro de nivel inferior y el diseño físico de los datos. Si dos filtros no pueden estar de acuerdo en un tipo de medio, no se conectarán.

En algunas aplicaciones, nunca tendrá que preocuparse por los tipos de medios. En la reproducción de archivos, por ejemplo, DirectShow controla todos los detalles. Es posible que otros tipos de aplicaciones necesiten trabajar directamente con tipos de medios.

Los tipos de medios se definen mediante la [**estructura \_ AM MEDIA \_ TYPE.**](/windows/win32/api/strmif/ns-strmif-am_media_type) Esta estructura contiene la siguiente información:

-   **Tipo principal:** el tipo principal es un GUID que define la categoría general de los datos. Los tipos principales incluyen vídeo, audio, secuencia de bytes sin análisis, datos DE MIDI, etc.
-   **Subtipo:** el subtipo es otro GUID, que define aún más el formato. Por ejemplo, dentro del tipo principal de vídeo, hay subtipos para RGB-24, RGB-32, UYVY, etc. Dentro del audio, hay audio PCM, carga MPEG-1 y otros. El subtipo proporciona más información que el tipo principal, pero no define todo sobre el formato. Por ejemplo, los subtipos de vídeo no definen el tamaño de la imagen ni la velocidad de fotogramas. Estos se definen mediante el bloque de formato, que se describe a continuación.
-   **Bloque de formato:** el bloque de formato es un bloque de datos que describe el formato en detalle. El bloque de formato se asigna por separado de la [**estructura \_ AM MEDIA \_ TYPE.**](/windows/win32/api/strmif/ns-strmif-am_media_type) El **miembro pbFormat** de la **estructura AM MEDIA \_ \_ TYPE** apunta al bloque de formato.

    El **miembro pbFormat** tiene el tipo **void \** _ porque el diseño del bloque de formato cambia en función del tipo de medio. Por ejemplo, el audio PCM usa una [estructura _ *FORMADEDATEX.* *](/previous-versions/dd757713(v=vs.85)) El vídeo usa varias estructuras, como [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) y [**VIDEOINFOHEADER2.**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) El **miembro formattype** de la estructura [**AM MEDIA \_ \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) es un GUID que especifica qué estructura se encuentra en el bloque de formato. A cada estructura de formato se le asigna un GUID. El **miembro cbFormat** especifica el tamaño del bloque de formato. Compruebe siempre estos valores antes de desreferenciar el **puntero pbFormat.**

Si se rellena el bloque de formato, el tipo principal y el subtipo contienen información redundante. Sin embargo, el tipo principal y el subtipo proporcionan una manera cómoda de identificar formatos sin un bloque de formato completo. Por ejemplo, puede especificar un formato RGB genérico de 24 bits (MEDIASUBTYPE RGB24), sin conocer toda la información requerida por la estructura VIDEOINFOHEADER, como el tamaño de la imagen y la velocidad de \_ fotogramas. [](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)

Por ejemplo, un filtro podría usar el código siguiente para comprobar un tipo de medio:


```C++
HRESULT CheckMediaType(AM_MEDIA_TYPE *pmt)
{
    if (pmt == NULL) return E_POINTER;

    // Check the major type. We're looking for video.
    if (pmt->majortype != MEDIATYPE_Video)
    {
        return VFW_E_INVALIDMEDIATYPE;
    }

    // Check the subtype. We're looking for 24-bit RGB.
    if (pmt->subtype != MEDIASUBTYPE_RGB24)
    {
        return VFW_E_INVALIDMEDIATYPE;
    }

    // Check the format type and the size of the format block.
    if ((pmt->formattype == FORMAT_VideoInfo) &&
         (pmt->cbFormat >= sizeof(VIDEOINFOHEADER) &&
         (pmt->pbFormat != NULL))
    {
        // Now it's safe to coerce the format block pointer to the
        // correct structure, as defined by the formattype GUID.
        VIDEOINFOHEADER *pVIH = (VIDEOINFOHEADER*)pmt->pbFormat;
    
        // Examine pVIH (not shown). If it looks OK, return S_OK.
        return S_OK;
    }

    return VFW_E_INVALIDMEDIATYPE;
}
```



La [**estructura AM MEDIA \_ \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) también contiene algunos campos opcionales. Se pueden usar para proporcionar información adicional, pero no se necesitan filtros para usarlos:

-   **lSampleSize**. Si este campo es distinto de cero, define el tamaño de cada muestra. Si es cero, indica que el tamaño de la muestra puede cambiar de muestra a muestra.
-   **bFixedSizeSamples**. Si esta marca booleana **es TRUE**, significa que el valor de **lSampleSize** es válido. De lo contrario, debe omitir **lSampleSize**.
-   **bComposiciónCompression**. Si esta marca booleana **es FALSE**, significa que todos los fotogramas son fotogramas clave.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[El filtro Graph y sus componentes](the-filter-graph-and-its-components.md)
</dt> </dl>

 

 
