---
description: En este tema se describe cómo escribir un filtro de origen personalizado para DirectShow.
ms.assetid: 032f7624-2237-41cd-844a-18ed4a2e420d
title: Cómo escribir un filtro de origen para DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87af99595a43c86be0e2f4ecaa51768a211e9674
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061663"
---
# <a name="how-to-write-a-source-filter-for-directshow"></a>Cómo escribir un filtro de origen para DirectShow

En este tema se describe cómo escribir un filtro de origen personalizado para DirectShow.

> [!Note]  
> En este tema solo se describen los orígenes de inserción; no describe los orígenes de extracción, como el filtro de lector asincrónico ni los filtros divisores que se conectan a los orígenes de extracción. Para la distinción  entre *los orígenes de inserción* y extracción, vea Data Flow for [Filter Developers](data-flow-for-filter-developers.md).

 

## <a name="the-directshow-streaming-model"></a>El modelo DirectShow streaming

Al escribir un filtro de origen, es importante comprender que un origen de inserción no es lo mismo que un origen en directo. Un origen en directo obtiene datos de algún origen externo, como una cámara o un flujo de red. Por lo general, un origen en directo no puede controlar la tasa entrante de datos. Si los filtros de nivel inferior no consumen los datos lo suficientemente rápido, el origen deberá quitar muestras.

Pero un origen de inserción no tiene que ser un origen en directo. Por ejemplo, un origen de inserción puede leer datos de un archivo local. En ese caso, los filtros de representador de bajada determinan la rapidez con la que consumen los datos del origen, en función del reloj de referencia y las marcas de tiempo de ejemplo. El filtro de origen entrega muestras lo antes posible, pero el flujo de datos real está limitado por los representadores. Los mecanismos para el acceso al flujo de datos se describen en [Data Flow for Filter Developers](data-flow-for-filter-developers.md).

Cada pin de salida del filtro de origen crea un subproceso denominado subproceso *de streaming.* El pin proporciona ejemplos en el subproceso de streaming. Normalmente, toda lacoding, el procesamiento y la representación se produce en este subproceso, aunque algunos filtros de nivel inferior podrían crear subprocesos adicionales para poner en cola sus ejemplos de salida.

El subproceso de streaming ejecuta un bucle con la siguiente estructura:

``` syntax
until (stopped)
  1. Get a media sample from the allocator.
  2. Fill the sample with data.
  3. Time stamp the sample. 
  4. Deliver the sample downstream.
```

Si no hay ejemplos disponibles, el paso 1 se bloquea hasta que haya disponible una muestra. El paso 4 también se puede bloquear; por ejemplo, puede bloquearse mientras el gráfico está en pausa.

El bucle se ejecuta lo más rápido posible, pero está limitado por la rapidez con la que el filtro del representador representa cada ejemplo. Suponiendo que el gráfico de filtros tiene un reloj de referencia, la velocidad viene determinada por los tiempos de presentación de las muestras. Si no hay ningún reloj de referencia, el representador consume muestras lo antes posible.

## <a name="using-csource-and-csourcestream"></a>Uso de CSource y CSourceStream

Las DirectShow base incluyen dos clases que admiten orígenes de inserción: [**CSource**](csource.md) y [**CSourceStream**](csourcestream.md).

-   [**CSource**](csource.md) es la clase base para el filtro e implementa la [**interfaz IBaseFilter.**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)
-   [**CSourceStream es**](csourcestream.md) la clase base para los pines de salida e implementa la [**interfaz IPin.**](/windows/desktop/api/Strmif/nn-strmif-ipin)

### <a name="output-pins"></a>Pins de salida

Un filtro de origen puede tener más de un pin de salida. En el método de constructor del filtro, cree uno o varios pines derivados de [**CSourceStream**](csourcestream.md) (un pin por flujo de salida). No es necesario almacenar punteros a los pines; los pines se agregan automáticamente al filtro cuando se crean.

### <a name="output-formats"></a>Formatos de salida

El pin de salida controla la negociación de formato con los siguientes [**métodos CSourceStream:**](csourcestream.md)



| Método                                                 | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetMediaType**](csourcestream-getmediatype.md)     | Obtiene un tipo de medio del pin de salida. <br/> El pin debe proponer al menos un tipo de medio, porque es posible que el filtro de nivel inferior no proponga ningún tipo. En la mayoría de los casos, el filtro de bajada será un descodificador o un representador, dependiendo de si el filtro de origen entrega datos comprimidos o sin comprimir. Un filtro de representador normalmente requiere un tipo de medio completo, que contiene toda la información de formato necesaria para representar la secuencia. Para un descodificador, la cantidad de información necesaria en el tipo de medio depende en gran medida del formato de codificación.<br/> |
| [**CheckMediaType**](csourcestream-checkmediatype.md) | Comprueba si el pin de salida acepta un tipo de medio determinado. La invalidación de este método es opcional, en función de cómo implemente [**GetMediaType**](csourcestream-getmediatype.md).                                                                                                                                                                                                                                                                                                                                                                                                         |



 

El [**método GetMediaType**](csourcestream-getmediatype.md) está sobrecargado:

-   [**GetMediaType**](csourcestream-getmediatype.md) (1) toma un único parámetro, un puntero a un [**objeto CMediaType.**](cmediatype.md)
-   [**GetMediaType**](csourcestream-getmediatype2.md) (2) toma una variable de índice y un puntero a un [**objeto CMediaType.**](cmediatype.md)

Si el pin de salida del filtro de origen admite exactamente un formato multimedia, debe invalidar (1) para inicializar el objeto [**CMediaType**](cmediatype.md) con ese formato. Deje la implementación predeterminada de (2) y deje también la implementación predeterminada de [**CheckMediaType**](csourcestream-checkmediatype.md).

Si el pin admite más de un formato, invalide (2). Inicialice [**el objeto CMediaType**](cmediatype.md) según el valor de la variable de índice. El pin debe devolver los formatos como una lista ordenada. En este caso, también debe invalidar [**CheckMediaType para**](csourcestream-checkmediatype.md) comprobar el tipo de medio con la lista de formatos.

En el caso de los formatos de vídeo sin comprimir, recuerde que el filtro de bajada puede proponer formatos con varios valores de paso. El filtro debe aceptar cualquier valor de intervalo válido. Para obtener más información, vea [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader).

También debe invalidar el método [**CBaseOutputPin::D ecideBufferSize**](cbaseoutputpin-decidebuffersize.md) puramente virtual. Use este método para establecer el tamaño de los búferes de ejemplo.

### <a name="streaming"></a>Streaming

La [**clase CSourceStream**](csourcestream.md) crea el subproceso de streaming para el pin. El procedimiento de subproceso se implementa en el [**método CSourceStream::D oBufferProcessingLoop.**](csourcestream-dobufferprocessingloop.md) Este método llama al método [**CSourceStream::FillBuffer**](csourcestream-fillbuffer.md) puramente virtual, que la clase derivada debe invalidar. Este método es donde el pin rellena el búfer con datos. Por ejemplo, si el filtro entrega vídeo sin comprimir, aquí es donde dibujaría los fotogramas de vídeo.

La clase base se inicia automáticamente y detiene el bucle de subprocesos en los momentos adecuados, cuando el filtro se detiene o se detiene. Cuando esto sucede, la [**clase CSourceStream**](csourcestream.md) llama a algunos métodos para notificar a la clase derivada:

-   [**CSourceStream::OnThreadCreate**](csourcestream-onthreadcreate.md)
-   [**CSourceStream::OnThreadDestroy**](csourcestream-onthreaddestroy.md)
-   [**CSourceStream::OnThreadStartPlay**](csourcestream-onthreadstartplay.md)

Puede invalidar estos métodos si necesita agregar cualquier control especial. De lo contrario, las implementaciones predeterminadas simplemente **devuelven S \_ OK**.

## <a name="seeking"></a>Buscando

Si tiene un filtro de origen con un pin de salida, puede usar la clase [**CSourceSeeking**](csourceseeking.md) como punto de partida para implementar la búsqueda. Herede la clase pin de [**CSourceStream**](csourcestream.md) y **CSourceSeeking.**

> [!Note]  
> [**CSourceSeeking**](csourceseeking.md) no se recomienda para un filtro con más de un pin de salida. El problema principal es que solo un pin debe responder a las solicitudes de búsqueda. Normalmente, esto requiere comunicación entre los pines y el filtro.

 

La [**clase CSourceSeeking**](csourceseeking.md) administra la velocidad de reproducción, la hora de inicio, la hora de detenerse y la duración. La clase derivada debe establecer la duración y el tiempo de detenerse iniciales. Cada vez que cambia uno de estos valores, se llama al método [**CSourceSeeking::ChangeRate,**](csourceseeking-changerate.md) [**CSourceSeeking::ChangeStart**](csourceseeking-changestart.md)o [**CSourceSeeking::ChangeStop,**](csourceseeking-changestop.md) según corresponda. Todos los métodos son métodos virtuales puros. La clase pin derivada invalida estos métodos para hacer lo siguiente:

1.  Llame [**a IPin::BeginFlush en**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) el pin de bajada. Esto hace que los filtros de nivel inferior liberen los ejemplos que están manteniendo y rechacen nuevos ejemplos.
2.  Llame [**a CSourceStream::Stop**](csourcestream-stop.md) para detener el subproceso de streaming. El filtro de origen suspende la generación de nuevos datos.
3.  Llame [**a IPin::EndFlush en**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) el pin de bajada. Esto indica a los filtros de nivel inferior que acepten nuevos datos.
4.  Llame [**a IPin::NewSegment con**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) las nuevas horas de inicio y detención y velocidad.
5.  Establezca la propiedad discontinuidad en el ejemplo siguiente.

Para obtener más información, [vea Compatibilidad con búsquedas en un filtro de origen.](supporting-seeking-in-a-source-filter.md)

Si el filtro admite búsquedas, la posición del flujo ahora es independiente del tiempo de presentación. Después de una búsqueda, las marcas de tiempo se restablecen en cero. La fórmula general para las marcas de tiempo es:

-   sample start time = time elapsed/playback rate
-   sample end time = sample start time + (time per frame/playback rate)

donde *el tiempo transcurrido es* el tiempo transcurrido desde que el filtro empezó a ejecutarse o desde el último comando de búsqueda.

### <a name="time-formats-for-seeking"></a>Formatos de tiempo para la búsqueda

De forma predeterminada, los comandos seek se encuentran en unidades de 100 nanosegundos. El filtro de origen puede admitir formatos de tiempo adicionales, como buscar por número de fotograma. Cada formato de hora se identifica mediante un GUID; vea [**GUID de formato de hora**](time-format-guids.md).

Para admitir formatos de tiempo adicionales, debe implementar los métodos siguientes en el pin de salida:

-   [**IMediaSeeking::ConvertTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-converttimeformat)
-   [**IMediaSeeking::GetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat)
-   [**IMediaSeeking::IsFormatSupported**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported)
-   [**IMediaSeeking::IsUsingTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isusingtimeformat)
-   [**IMediaSeeking::QueryPreferredFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-querypreferredformat)
-   [**IMediaSeeking::SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat)

Si la aplicación establece un nuevo formato de hora, todos los parámetros de posición de los métodos [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) se interpretan en términos del nuevo formato de hora. Por ejemplo, si el formato de hora es fotogramas, el método [**IMediaSeeking::GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) debe devolver la duración en fotogramas.

En la práctica, algunos DirectShow admiten formatos de tiempo adicionales y, como resultado, algunas DirectShow aplicaciones hacen uso de esta funcionalidad.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Escribir filtros de origen](writing-source-filters.md)
</dt> </dl>

 

 




