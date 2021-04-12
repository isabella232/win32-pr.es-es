---
description: En este tema se describe cómo escribir un filtro de origen personalizado para DirectShow.
ms.assetid: 032f7624-2237-41cd-844a-18ed4a2e420d
title: Cómo escribir un filtro de origen para DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87af99595a43c86be0e2f4ecaa51768a211e9674
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104538043"
---
# <a name="how-to-write-a-source-filter-for-directshow"></a>Cómo escribir un filtro de origen para DirectShow

En este tema se describe cómo escribir un filtro de origen personalizado para DirectShow.

> [!Note]  
> En este tema solo se describen los orígenes de inserciones; no describe los orígenes de extracción, como el filtro de lectura asincrónico o los filtros divisores que se conectan a los orígenes de extracción. Para ver la diferencia entre los orígenes de *inserción* y de *extracción* , vea [flujo de datos para los desarrolladores de filtros](data-flow-for-filter-developers.md).

 

## <a name="the-directshow-streaming-model"></a>El modelo de streaming de DirectShow

Al escribir un filtro de origen, es importante comprender que un origen de la extracción no es lo mismo que un origen en directo. Un origen en directo obtiene los datos de un origen externo, como una cámara o un flujo de red. Normalmente, un origen en directo no puede controlar la velocidad de entrada de los datos. Si los filtros de nivel inferior no consumen los datos lo suficientemente rápido, el origen deberá quitar ejemplos.

Pero un origen de la extracción no tiene que ser un origen en directo. Por ejemplo, un origen de la extracción puede leer datos de un archivo local. En ese caso, los filtros de representador de nivel inferior determinan la rapidez con la que usan los datos del origen, en función del reloj de referencia y las marcas de tiempo de muestra. El filtro de origen proporciona ejemplos lo más rápido posible, pero los representadores limitan el flujo de datos real. Los mecanismos para canalizar el flujo de datos se describen en [flujo de datos para los desarrolladores de filtros](data-flow-for-filter-developers.md).

Cada pin de salida en el filtro de origen crea un subproceso denominado *subproceso de streaming*. El PIN ofrece ejemplos en el subproceso de streaming. Normalmente, la descodificación, el procesamiento y la representación se producen en este subproceso, aunque algunos filtros de nivel inferior pueden crear subprocesos adicionales para poner en cola sus ejemplos de salida.

El subproceso de streaming ejecuta un bucle con la siguiente estructura:

``` syntax
until (stopped)
  1. Get a media sample from the allocator.
  2. Fill the sample with data.
  3. Time stamp the sample. 
  4. Deliver the sample downstream.
```

Si no hay ningún ejemplo disponible, el paso 1 se bloquea hasta que una muestra esté disponible. El paso 4 también puede bloquearse; por ejemplo, puede bloquear mientras el gráfico está en pausa.

El bucle se ejecuta lo más rápido posible, pero está limitado por la rapidez con la que el filtro de representador representa cada ejemplo. Suponiendo que el gráfico de filtros tiene un reloj de referencia, la frecuencia viene determinada por los tiempos de presentación de los ejemplos. Si no hay ningún reloj de referencia, el representador consume ejemplos lo más rápido posible.

## <a name="using-csource-and-csourcestream"></a>Usar CSource y CSourceStream

Las clases base de DirectShow incluyen dos clases que admiten orígenes de inserciones: [**CSource**](csource.md) y [**CSourceStream**](csourcestream.md).

-   [**CSource**](csource.md) es la clase base para el filtro e implementa la interfaz [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) .
-   [**CSourceStream**](csourcestream.md) es la clase base para los terminales de salida e implementa la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) .

### <a name="output-pins"></a>Clavijas de salida

Un filtro de origen puede tener más de un PIN de salida. En el método de constructor del filtro, cree uno o varios PIN derivados de [**CSourceStream**](csourcestream.md) (un PIN por cada flujo de salida). No es necesario almacenar punteros a los pin; los PIN se agregan automáticamente al filtro cuando se crean.

### <a name="output-formats"></a>Formatos de salida

El PIN de salida controla la negociación de formato con los siguientes métodos [**CSourceStream**](csourcestream.md) :



| Método                                                 | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetMediaType**](csourcestream-getmediatype.md)     | Obtiene un tipo de medio de la clavija de salida. <br/> El PIN debe proponer al menos un tipo de medio, ya que el filtro de nivel inferior podría no proponer ningún tipo. En la mayoría de los casos, el filtro de nivel inferior será un descodificador o un representador, en función de si el filtro de origen proporciona datos comprimidos o sin comprimir. Un filtro de representador normalmente requiere un tipo de medio completo, que contiene toda la información de formato necesaria para representar la secuencia. En el caso de un descodificador, la cantidad de información que se requiere en el tipo de medio depende mucho en el formato de codificación.<br/> |
| [**CheckMediaType**](csourcestream-checkmediatype.md) | Comprueba si el PIN de salida acepta un tipo de medio determinado. Reemplazar este método es opcional, en función de cómo se implemente [**GetMediaType**](csourcestream-getmediatype.md).                                                                                                                                                                                                                                                                                                                                                                                                         |



 

El método [**GetMediaType**](csourcestream-getmediatype.md) está sobrecargado:

-   [**GetMediaType**](csourcestream-getmediatype.md) (1) toma un parámetro único, un puntero a un objeto [**CMediaType**](cmediatype.md) .
-   [**GetMediaType**](csourcestream-getmediatype2.md) (2) toma una variable de índice y un puntero a un objeto [**CMediaType**](cmediatype.md) .

Si el PIN de salida del filtro de origen admite exactamente un formato multimedia, debe reemplazar (1) para inicializar el objeto [**CMediaType**](cmediatype.md) con ese formato. Deje la implementación predeterminada de (2) y deje también la implementación predeterminada de [**CheckMediaType**](csourcestream-checkmediatype.md).

Si el PIN admite más de un formato, invalide (2). Inicialice el objeto [**CMediaType**](cmediatype.md) según el valor de la variable de índice. El PIN debe devolver los formatos como una lista ordenada. En este caso, también debe invalidar el [**CheckMediaType**](csourcestream-checkmediatype.md) para comprobar el tipo de medio en la lista de formatos.

En el caso de los formatos de vídeo sin comprimir, recuerde que el filtro de nivel inferior puede proponer formatos con varios valores de intervalo. El filtro debe aceptar cualquier valor de STRIDE válido. Para obtener más información, vea [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader).

También debe invalidar el método CBaseOutputPin virtual puro [**::D ecidebuffersize**](cbaseoutputpin-decidebuffersize.md) . Use este método para establecer el tamaño de los búferes de ejemplo.

### <a name="streaming"></a>Streaming

La clase [**CSourceStream**](csourcestream.md) crea el subproceso de streaming para el PIN. El procedimiento de subproceso se implementa en el método [**CSourceStream::D obufferprocessingloop**](csourcestream-dobufferprocessingloop.md) . Este método llama al método [**CSourceStream:: FillBuffer**](csourcestream-fillbuffer.md) puro-virtual, que la clase derivada debe reemplazar. Este método es donde el PIN rellena el búfer con los datos. Por ejemplo, si el filtro proporciona vídeo sin comprimir, aquí es donde dibujaría los fotogramas de vídeo.

La clase base se inicia automáticamente y detiene el bucle de subprocesos en el momento adecuado, cuando el filtro se pausa o se detiene. Cuando esto sucede, la clase [**CSourceStream**](csourcestream.md) llama a algunos métodos para notificar a la clase derivada:

-   [**CSourceStream::OnThreadCreate**](csourcestream-onthreadcreate.md)
-   [**CSourceStream::OnThreadDestroy**](csourcestream-onthreaddestroy.md)
-   [**CSourceStream::OnThreadStartPlay**](csourcestream-onthreadstartplay.md)

Puede invalidar estos métodos si necesita agregar un control especial. De lo contrario, las implementaciones predeterminadas simplemente devuelven los valores **\_ correctos**.

## <a name="seeking"></a>Invoca

Si tiene un filtro de origen con un PIN de salida, puede usar la clase [**CSourceSeeking**](csourceseeking.md) como punto de partida para implementar búsquedas. Herede la clase de PIN de [**CSourceStream**](csourcestream.md) y **CSourceSeeking**.

> [!Note]  
> No se recomienda [**CSourceSeeking**](csourceseeking.md) para un filtro con más de un PIN de salida. El problema principal es que solo un PIN debe responder a las solicitudes de búsqueda. Normalmente, esto requiere la comunicación entre los pin y el filtro.

 

La clase [**CSourceSeeking**](csourceseeking.md) administra la velocidad de reproducción, la hora de inicio, la hora de finalización y la duración. La clase derivada debe establecer la hora de detención y la duración iniciales. Cada vez que uno de estos valores cambia, se llama al método [**CSourceSeeking:: ChangeRate**](csourceseeking-changerate.md), [**CSourceSeeking:: cambie las**](csourceseeking-changestart.md)o [**CSourceSeeking:: ChangeStop**](csourceseeking-changestop.md) , según corresponda. Los métodos son métodos virtuales puros. La clase de PIN derivada invalida estos métodos para hacer lo siguiente:

1.  Llame a [**IPin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) en el PIN de nivel inferior. Esto hace que los filtros de nivel inferior puedan publicar ejemplos que contienen y rechazan los nuevos ejemplos.
2.  Llame a [**CSourceStream:: Stop**](csourcestream-stop.md) para detener el subproceso de streaming. El filtro de origen suspende la generación de nuevos datos.
3.  Llame a [**IPin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) en el PIN de nivel inferior. Esto indica a los filtros de nivel inferior que acepten datos nuevos.
4.  Llame a [**IPin:: NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) con las nuevas horas de inicio y detención.
5.  Establezca la propiedad discontinuidad en el ejemplo siguiente.

Para obtener más información, vea [admitir búsquedas en un filtro de origen](supporting-seeking-in-a-source-filter.md).

Si el filtro admite búsquedas, la posición del flujo es ahora independiente del tiempo de presentación. Después de una búsqueda, las marcas de tiempo se restablecen a cero. La fórmula general para las marcas de tiempo es:

-   hora de inicio de ejemplo = tiempo transcurrido/velocidad de reproducción
-   hora de finalización de ejemplo = hora de inicio de ejemplo + (hora por fotograma/velocidad de reproducción)

el tiempo *transcurrido* es el tiempo transcurrido desde que se empezó a ejecutar el filtro o desde el último comando de búsqueda.

### <a name="time-formats-for-seeking"></a>Formatos de hora para buscar

De forma predeterminada, los comandos de búsqueda están en unidades de 100 a nanosegundos. El filtro de origen puede admitir formatos de hora adicionales, como la búsqueda por número de marco. Cada formato de hora se identifica mediante un GUID; consulte [**GUID de formato de hora**](time-format-guids.md).

Para admitir formatos de hora adicionales, debe implementar los métodos siguientes en el PIN de salida:

-   [**IMediaSeeking::ConvertTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-converttimeformat)
-   [**IMediaSeeking::GetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat)
-   [**IMediaSeeking::IsFormatSupported**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported)
-   [**IMediaSeeking::IsUsingTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isusingtimeformat)
-   [**IMediaSeeking::QueryPreferredFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-querypreferredformat)
-   [**IMediaSeeking::SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat)

Si la aplicación establece un nuevo formato de hora, todos los parámetros de posición de los métodos [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) se interpretan en términos del nuevo formato de hora. Por ejemplo, si el formato de hora es frames, el método [**IMediaSeeking:: GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) debe devolver la duración en fotogramas.

En la práctica, pocos filtros de DirectShow admiten formatos de hora adicionales y, como resultado, pocas aplicaciones de DirectShow hacen uso de esta funcionalidad.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Escribir filtros de origen](writing-source-filters.md)
</dt> </dl>

 

 




