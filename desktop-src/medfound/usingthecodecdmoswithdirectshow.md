---
description: Usar los códecs de Windows Media en DirectShow
ms.assetid: 5b930447-6bf2-4bb3-8dfb-05f4c1e7cd64
title: Usar los códecs de Windows Media en DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb521c0e3897dc2415fbd613f97b755a146657d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687170"
---
# <a name="using-the-window-media-codecs-in-directshow"></a>Usar los códecs de Windows Media en DirectShow

Los objetos de codificador y descodificador de Windows Media Audio y vídeo se diseñaron y optimizaron originalmente para trabajar con el formato de contenedor de archivos ASF y el SDK de Windows Media Format. Los objetos de códec funcionan bien en DirectShow en algunos escenarios, es decir, un paso de una sola fase y una codificación VBR basada en la calidad de las secuencias de vídeo. Pero si está pensando en utilizar los objetos de códec directamente en DirectShow mediante contenedores de archivos que no sean ASF, existen ciertos comportamientos y problemas que debe tener en cuenta de antemano.

> [!Note]  
> Si va a utilizar códecs independientes con DirectShow, es probable que solo desee usarlos como DMOs. En otras palabras, utilizará la interfaz [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) en lugar de [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform).

 

## <a name="wm-audio-in-avi-files"></a>Audio de WM en archivos AVI

Puede usar DirectShow para codificar secuencias WMA en cualquier formato de contenedor de archivos para el que tenga un filtro multiplexor. Sin embargo, las interfaces de Windows Media Audio y códec de vídeo no admiten WMA en archivos AVI porque no es posible, mediante los filtros de reproducción de DirectShow AVI predeterminados, para mantener la sincronización de audio y vídeo en un archivo AVI con una secuencia WMA. Para obtener más información, vea [almacenar medios comprimidos en archivos AVI](storingcompressedmediainavifiles.md).

El codificador de audio DMO genera ejemplos de duración variable, incluso cuando está en modo de "velocidad de bits constante". Por lo tanto, funciona mejor con formatos de contenedor de archivos que usan marcas de tiempo. Los archivos AVI no proporcionan una marca de tiempo para cada ejemplo de audio o grupo de muestras. En DirectShow, el filtro de divisor de AVI fabrica marcas de tiempo para cada grupo de muestras (cada fotograma de audio) basándose en el valor **nAvgBytesPerSec** de la estructura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) del encabezado de la secuencia AVI.

La suposición subyacente de este cálculo es que todas las muestras de audio del flujo tienen la misma duración. sin embargo, los ejemplos generados por DMO no tienen la misma duración, por lo que las marcas de tiempo aplicadas por el divisor de AVI no son precisas. Por lo tanto, no es posible, sin modificar el divisor de AVI o el descodificador de audio DMO, para usar cualquier aplicación basada en DirectShow para reproducir archivos AVI con secuencias de audio y vídeo sincronizadas. El códec de voz de Windows Media Audio 9 funcionará en algunos casos, pero incluso esto perderá la sincronización después de cualquier operación de búsqueda, por lo que realmente no se puede considerar una solución viable.

Si tiene un codificador MP3, puede crear archivos AVI con WMV y MP3 para la secuencia de audio. Estos archivos se reproducirán y buscarán correctamente en Windows Media Player y otras aplicaciones basadas en DirectShow, ya que el divisor de AVI contiene código de control especial para flujos MP3. Otra opción consiste en usar audio PCM sin comprimir, aunque obviamente el tamaño de archivo resultante será mucho mayor que con una secuencia de audio comprimida. Dado que la aplicación de ejemplo de DirectShow crea archivos AVI, no muestra cómo usar el codificador de audio DMO.

## <a name="one-pass-encoding"></a>Codificación de un paso

El codificador de vídeo DMO funciona fácilmente en DirectShow con dos modos de codificación: CBR y VBR basada en la calidad. Siempre que siga el orden correcto de las operaciones al compilar el gráfico de filtros, tal como se muestra en la aplicación de ejemplo, es relativamente sencillo colocar el contenido WMV en un archivo AVI mediante el multiplexor de AVI y el escritor de archivos.

## <a name="two-pass-encoding"></a>Codificación de dos pasos

Los modos de codificación de dos pasos requieren un enfoque más complejo a la creación y la transmisión de gráficos para evitar que DMO vacíe su contenido del primer paso antes de comenzar el segundo paso. En la codificación de dos pasos, es necesario ejecutar el gráfico una vez para que DMO pueda realizar el análisis de preprocesamiento de los datos de archivo y, a continuación, rebobinar el gráfico y volver a ejecutarlo para que el DMO pueda realizar la codificación real.

Cuando el gráfico entra en un estado de ejecución para el segundo paso, el contenedor de DMO establece la marca de discontinuidad en el primer ejemplo, porque la marca de tiempo no es secuencial con la última marca de tiempo en el primer paso. Cuando DMO, que no estaba diseñado para funcionar en DirectShow de esta manera, recibe la marca de discontinuidad, realiza un vaciado y pierde los datos almacenados desde el primer paso. Para solucionar este problema, la mejor solución es probablemente escribir un filtro contenedor de DMO personalizado que no establezca la marca de discontinuidad cuando se busque el gráfico después del primer paso. En el ejemplo de vídeo para Windows (VfW) de este SDK se muestra cómo realizar la codificación de dos pasos.

## <a name="interlaced-content"></a>Contenido entrelazado

El codificador WMV DMO es capaz de codificar contenido entrelazado a la vez que conserva el entrelazado, lo que resulta útil para el contenido capturado de un televisor y también puede reproducirse en un televisor. Sin embargo, no es posible conservar el entrelazado mediante el contenedor DMO predeterminado, ya que ese filtro no admite [**INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) en sus ejemplos de entrada.

DMO utiliza esa interfaz para obtener la configuración entrelazada de cada ejemplo que recibe. Si no se encuentra la interfaz, como es el caso del contenedor de DMO, DMO simplemente trata los ejemplos de entrada como no entrelazados. Hay varias alternativas para realizar la codificación entrelazada en DirectShow. El enfoque más sencillo es probablemente usar el SDK de Windows Media Format 9 series, ya sea directamente o mediante el filtro DirectShow del escritor ASF de WM, para crear un archivo ASF entrelazado. Después, puede transcodificar ese archivo en otro formato. Si transcodificas en AVI, tendrá un archivo entrelazado, pero los filtros de reproducción de AVI de DirectShow estándar no lo reconocerán como tal porque no son compatibles con [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2). Otro enfoque consiste en escribir su propio filtro de contenedor de DMO que admita la interfaz [**INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Trabajar con códec DMOs](workingwithcodecdmos.md)
</dt> </dl>

 

 
