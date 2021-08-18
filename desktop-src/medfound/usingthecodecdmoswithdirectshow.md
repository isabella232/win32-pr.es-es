---
description: Uso de códecs multimedia de ventana en DirectShow
ms.assetid: 5b930447-6bf2-4bb3-8dfb-05f4c1e7cd64
title: Uso de códecs multimedia de ventana en DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 495a2675335474351da80b9845fba67f9e967d637d7c9d9c749ffc2f12ce3ea4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012185"
---
# <a name="using-the-window-media-codecs-in-directshow"></a>Uso de códecs multimedia de ventana en DirectShow

Los Windows codificador y descodificador multimedia de audio y vídeo se diseñaron y optimizaron originalmente para funcionar con el formato de contenedor de archivos ASF y el SDK Windows Media Format. Los objetos de códec funcionan bien en DirectShow para determinados escenarios, es decir, cbr de un paso y codificación VBR basada en calidad de secuencias de vídeo. Pero si está pensando en usar los objetos de códec directamente en DirectShow mediante contenedores de archivos que no sean ASF, hay ciertos comportamientos y problemas que debe tener en cuenta de antemano.

> [!Note]  
> Si va a usar códecs independientes con DirectShow, probablemente quiera usarlos solo como DDO. En otras palabras, va a usar la [**interfaz IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) en lugar de [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform).

 

## <a name="wm-audio-in-avi-files"></a>Audio WM en archivos AVI

Puede usar DirectShow codificar secuencias WMA en cualquier formato de contenedor de archivos para el que tenga un filtro multiplexor. Sin embargo, las interfaces de códecs de audio y vídeo multimedia de Windows no admiten WMA en archivos AVI porque es imposible, mediante los filtros de reproducción avi de DirectShow predeterminados, mantener la sincronización de audio y vídeo en un archivo AVI con una secuencia WMA. Para obtener más información, vea [Almacenamiento de medios comprimidos en archivos AVI.](storingcompressedmediainavifiles.md)

El codificador de audio DMO muestra muestras de duración variable, incluso cuando se encuentra en modo de "velocidad de bits constante". Por lo tanto, funciona mejor con formatos de contenedor de archivos que usan marcas de tiempo. Los archivos AVI no proporcionan una marca de tiempo para cada muestra de audio o grupo de muestras. En DirectShow, el filtro divisor AVI fabrica marcas de tiempo para cada grupo de muestras (cada fotograma de audio) en función del valor **nAvgBytesPerSec** de la estructura [**DESATEX**](/previous-versions/dd757713(v=vs.85)) en el encabezado de flujo AVI.

La suposición subyacente a este cálculo es que todas las muestras de audio de la secuencia tienen la misma duración; sin embargo, los ejemplos que genera el DMO no son de la misma duración, por lo que las marcas de tiempo aplicadas por el divisor AVI no son precisas. Por lo tanto, no es posible, sin modificar el divisor AVI o el descodificador de audio DMO, usar cualquier aplicación basada en DirectShow para reproducir archivos AVI con secuencias de audio y vídeo sincronizadas. El códec Windows Media Audio 9 Voice funcionará en algunos casos, pero incluso esto perderá la sincronización después de cualquier operación de búsqueda, por lo que realmente no se puede considerar una solución viable.

Si tiene un codificador MP3, puede crear archivos AVI con WMV y MP3 para la secuencia de audio. Estos archivos se reproducirán y buscarán correctamente en Reproductor de Windows Media y otras aplicaciones basadas en DirectShow, ya que el divisor AVI contiene código de control especial para secuencias MP3. Otra opción es usar audio PCM sin comprimir, aunque obviamente el tamaño del archivo resultante será mucho mayor que con una secuencia de audio comprimida. Dado que DirectShow aplicación de ejemplo crea archivos AVI, no muestra cómo usar el codificador de audio DMO.

## <a name="one-pass-encoding"></a>Codificación de un solo paso

El codificador de DMO funciona fácilmente en DirectShow dos modos de codificación: CBR y VBR basado en calidad. Siempre que siga el orden correcto de las operaciones al compilar el gráfico de filtros, como se muestra en la aplicación de ejemplo, es relativamente sencillo colocar contenido WMV en un archivo AVI mediante el multiplexador AVI y el escritor de archivos.

## <a name="two-pass-encoding"></a>Codificación de dos pases

Los modos de codificación de dos pases requieren un enfoque más complejo para la creación y el streaming de grafos con el fin de evitar que el DMO vacíe su contenido desde el primer paso antes de comenzar el segundo paso. En la codificación de dos pasos, es necesario ejecutar el gráfico una vez para que el DMO pueda realizar su análisis de preprocesamiento de los datos de archivo y, a continuación, rebobinar el gráfico y ejecutarlo de nuevo para que el DMO pueda realizar la codificación real.

Cuando el gráfico entra en un estado de ejecución para el segundo paso, el contenedor de DMO establece la marca DISCONTINUITY en el primer ejemplo, porque la marca de tiempo no es secuencial con la última marca de tiempo en el primer paso. Cuando el DMO, que no se diseñó para funcionar en DirectShow de esta manera, recibe la marca DISCONTINUITY, realiza un vaciado y pierde los datos almacenados desde el primer paso. Para evitar este problema, es probable que la mejor solución sea escribir un filtro contenedor de DMO personalizado que no establezca la marca DISCONTINUITY cuando se busca el gráfico después del primer paso. En el ejemplo Video for Windows (VfW) de este SDK se muestra cómo realizar la codificación de dos pases.

## <a name="interlaced-content"></a>Contenido entrelazado

El codificador WMV DMO codificar contenido entrelazado a la vez que se conserva el entrelazado, lo que resulta útil para el contenido que se captura desde un televisor y que también se puede reproducir en un televisor. Sin embargo, no es posible conservar el entrelazado mediante el contenedor DMO predeterminado, ya que ese filtro no admite [**INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) en sus ejemplos de entrada.

El DMO usa esa interfaz para obtener la configuración entrelazada de cada muestra que recibe. Si no se encuentra la interfaz, como sucede con DMO Wrapper, el DMO simplemente trata las muestras de entrada como no entrelazadas. Para realizar la codificación entrelazada DirectShow, hay varias alternativas. El enfoque más sencillo es usar el SDK de la serie Windows Media Format 9 directamente o mediante el filtro de DirectShow WM ASF Writer, para crear un archivo ASF entrelazado. A continuación, puede transcodificar ese archivo en otro formato. Si transcodifica en AVI, tendrá un archivo entrelazado, pero los filtros de reproducción estándar de DirectShow AVI no lo reconocerán como tal porque no [**admiten VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2). Otro enfoque es escribir su propio filtro DMO wrapper que admita la [**interfaz INSSBuffer.**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Trabajar con DDO de códec](workingwithcodecdmos.md)
</dt> </dl>

 

 
