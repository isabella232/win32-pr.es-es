---
description: Acerca de los tipos de medios
ms.assetid: 9984ba36-4e43-4886-a073-34b330274c9c
title: Acerca de los tipos de medios (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3289a37e95bf5dbd1e5c277b5799a2c7c8c90586
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104361845"
---
# <a name="about-media-types-directshow"></a>Acerca de los tipos de medios (DirectShow)

Dado que DirectShow es modular, requiere una manera de describir el formato de los datos en cada punto del gráfico de filtro. Por ejemplo, considere la posibilidad de reproducir AVI. Los datos entran en el gráfico como un flujo de fragmentos RIFF. Se analizan en secuencias de audio y vídeo. La secuencia de vídeo se compone de fotogramas de vídeo, que probablemente estén comprimidos. Después de la descodificación, el flujo de vídeo es una serie de mapas de bits sin comprimir. La secuencia de audio pasa por un proceso similar.

Tipos de medios: Cómo representa DirectShow los formatos

El *tipo de medio* es una manera universal y extensible de describir formatos de medios digitales. Cuando dos filtros se conectan, coinciden con un tipo de medio. El tipo de medio identifica el tipo de datos que el filtro de nivel superior proporcionará al filtro de bajada y el diseño físico de los datos. Si dos filtros no pueden estar de acuerdo en un tipo de medio, no se conectarán.

En el caso de algunas aplicaciones, nunca tendrá que preocuparse de los tipos de medios. En la reproducción de archivos, por ejemplo, DirectShow controla todos los detalles. Otros tipos de aplicaciones pueden necesitar trabajar directamente con los tipos de medios.

Los tipos de medios se definen mediante la estructura de [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) . Esta estructura contiene la siguiente información:

-   **Tipo principal**: el tipo principal es un GUID que define la categoría general de los datos. Entre los tipos principales se incluyen vídeo, audio, secuencia de bytes sin analizar, datos MIDI, etc.
-   **SubType**: el subtipo es otro GUID, que define el formato. Por ejemplo, en el tipo de vídeo principal, hay subtipos para RGB-24, RGB-32, UYVY, etc. Dentro de audio, hay audio PCM, carga MPEG-1 y otros. El subtipo proporciona más información que el tipo principal, pero no define todo lo relacionado con el formato. Por ejemplo, los subtipos de vídeo no definen el tamaño de la imagen ni la velocidad de fotogramas. Se definen mediante el bloque de formato, que se describe a continuación.
-   **Bloque de formato**: el bloque de formato es un bloque de datos que describe el formato en detalle. El bloque de formato se asigna por separado de la estructura de [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) . El miembro **pbFormat** de la estructura de **\_ \_ tipo de medio am** apunta al bloque de formato.

    El miembro **pbFormat** tiene tipo **void \** _ porque el diseño del bloque Format cambia según el tipo de medio. Por ejemplo, PCM audio usa una estructura [_ *WAVEFORMATEX* *](/previous-versions/dd757713(v=vs.85)) . El vídeo usa varias estructuras, como [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) y [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2). El miembro **formatType** de la estructura de [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) es un GUID que especifica la estructura que se encuentra en el bloque de formato. A cada estructura de formato se le asigna un GUID. El miembro **cbFormat** especifica el tamaño del bloque de formato. Compruebe siempre estos valores antes de desreferenciar el puntero **pbFormat** .

Si el bloque de formato se rellena, el tipo y el subtipo principales contienen información redundante. Sin embargo, el tipo y el subtipo principales proporcionan una manera cómoda de identificar formatos sin un bloque de formato completo. Por ejemplo, puede especificar un formato RGB de 24 bits genérico (MEDIASUBTYPE \_ RGB24), sin conocer toda la información requerida por la estructura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) , como el tamaño de la imagen y la velocidad de fotogramas.

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



La estructura de [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) también contiene algunos campos opcionales. Se pueden usar para proporcionar información adicional, pero no es necesario que los filtros los usen:

-   **lSampleSize**. Si este campo es distinto de cero, define el tamaño de cada ejemplo. Si es cero, indica que el tamaño de la muestra puede cambiar de sample a sample.
-   **bFixedSizeSamples**. Si esta marca booleana es **true**, significa que el valor de **lSampleSize** es válido. De lo contrario, debe omitir **lSampleSize**.
-   **bTemporalCompression**. Si esta marca booleana es **false**, significa que todos los marcos son fotogramas clave.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[El gráfico de filtro y sus componentes](the-filter-graph-and-its-components.md)
</dt> </dl>

 

 
