---
description: Compilar el gráfico de recompresión
ms.assetid: 8f25c60e-30be-4cc4-b924-b8d6654604d3
title: Compilar el gráfico de recompresión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b8ea604bead34c22c123bbabe5d88e985006a9e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906385"
---
# <a name="building-the-recompression-graph"></a>Compilar el gráfico de recompresión

Un gráfico de filtro típico para la recompresión de archivos AVI tiene el siguiente aspecto:

![gráfico de recompresión de AVI](images/avi2avi4.png)

El [filtro de divisor de AVI](avi-splitter-filter.md) extrae datos del [filtro de origen de archivos (Async)](file-source--async--filter.md) y los analiza en secuencias de audio y vídeo. El descompresor de vídeo descodifica el vídeo comprimido, donde se vuelve a comprimir con el compresor de vídeo. La elección de descompresores depende del archivo de código fuente; se controlará automáticamente mediante la [conexión inteligente](intelligent-connect.md). La aplicación debe elegir el compresor, normalmente presentando una lista al usuario. (Vea [elegir un filtro de compresión](choosing-a-compression-filter.md)).

Después, el vídeo comprimido se dirige al [filtro de AVI](avi-mux-filter.md). La secuencia de audio de este ejemplo no está comprimida, por lo que va directamente desde el divisor de AVI a AVI Mux. El MUX de AVI entrelaza las dos secuencias y el filtro de [escritura de archivos](file-writer-filter.md) escribe la salida en el disco. Tenga en cuenta que se requiere AVI MUX incluso si el archivo original no tiene una secuencia de audio.

La manera más sencilla de generar este gráfico de filtro es usar el [generador de gráficos de captura](capture-graph-builder.md), que es un componente de DirectShow para crear gráficos de captura y otros gráficos de filtros personalizados.

Empiece por llamar a CoCreateInstance para crear el generador de gráficos de captura:


```C++
ICaptureGraphBuilder2 *pBuild = NULL;
hr = CoCreateInstance(CLSID_CaptureGraphBuilder2, 
                        NULL, CLSCTX_INPROC_SERVER,
    IID_ICaptureGraphBuilder2, (void **)&pBuild);
```



A continuación, use el generador de gráficos de captura para compilar el gráfico de filtro:

1.  Cree la sección de representación del gráfico, que incluye el filtro de AVI y el [escritor de archivos](file-writer-filter.md).
2.  Agregue el filtro de origen y el filtro de compresión al gráfico.
3.  Conecte el filtro de origen al filtro MUX. El generador de gráficos de captura inserta cualquier filtro de divisor y descodificador que se necesite para analizar el archivo de código fuente. También puede enrutar las secuencias de audio y vídeo a través de filtros de compresión.

En las secciones siguientes se explica cada uno de estos pasos.

Crear la sección de representación

Para compilar la sección de representación del gráfico, llame al método [**ICaptureGraphBuilder2:: SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) . Este método toma parámetros de entrada que especifican el subtipo de medios para la salida y el nombre del archivo de salida. Devuelve punteros al filtro MUX y al escritor de archivos. El filtro MUX es necesario para la siguiente fase de creación del gráfico. El puntero al escritor de archivos no es necesario en este ejemplo, de modo que el parámetro puede ser **null**:


```C++
IBaseFilter *pMux = NULL;
hr = pBuild->SetOutputFileName(
        &MEDIASUBTYPE_Avi, // File type. 
        wszOutputFile,     // File name, as a wide-character string.
        &pMux,             // Receives a pointer to the multiplexer.
        NULL);             // Receives a pointer to the file writer. 
```



Cuando el método devuelve, el filtro MUX tiene un recuento de referencias pendiente, de modo que asegúrese de liberar el puntero más adelante.

En el diagrama siguiente se muestra el gráfico de filtro en este punto.

![sección de representación del gráfico de filtros](images/avi2avi1.png)

El filtro MUX expone dos interfaces para controlar el formato AVI:

-   [**Interfaz IConfigInterleaving**](/windows/desktop/api/Strmif/nn-strmif-iconfiginterleaving): establece el modo de intercalación.
-   [**Interfaz IConfigAviMux**](/windows/desktop/api/Strmif/nn-strmif-iconfigavimux): establece la secuencia maestra y el índice de compatibilidad AVI.

Agregar los filtros de origen y compresión

El siguiente paso consiste en agregar los filtros de origen y de compresión al gráfico de filtro. El generador de gráficos de captura crea automáticamente una instancia del administrador de gráficos de filtro cuando se llama a SetOutputFileName. Obtenga un puntero a él llamando al método [**ICaptureGraphBuilder2:: GetFiltergraph**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-getfiltergraph) :


```C++
IGraphBuilder *pGraph = NULL;
hr = pBuild->GetFiltergraph(&pGraph);
```



Ahora llame al método [**IGraphBuilder:: AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) para agregar el filtro de origen de archivo asincrónico y el método [**IFilterGraph:: addFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) para agregar el compresor de vídeo:


```C++
IBaseFilter *pSrc = NULL;
hr = pGraph->AddSourceFilter(wszInputFile, L"Source Filter", &pSrc);
hr = pGraph->AddFilter(pVComp, L"Compressor");
```



En este momento, el filtro de origen y el filtro de compresión no están conectados a ningún otro elemento del gráfico, tal como se muestra en la siguiente ilustración:

![filtrar gráfico con filtros de origen y compresión](images/avi2avi2.png)

Conexión del origen con el MUX

El paso final consiste en conectar el filtro de origen al filtro de AVI, a través del compresor de vídeo. Use el método [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) , que conecta un PIN de salida en el filtro de origen con un filtro de receptor especificado, opcionalmente a través de un filtro de compresión.

Los dos primeros parámetros especifican cuál de los PIN del filtro de origen se conectan, mediante la designación de una categoría de PIN y un tipo de medio. El filtro de origen de archivo Async solo tiene un PIN de salida, por lo que estos parámetros deben ser **null**. Los tres parámetros siguientes especifican el filtro de origen, el filtro de compresión (si existe) y el filtro Mux.

En el ejemplo de código siguiente se representa la secuencia de vídeo a través del compresor de vídeo:


```C++
hr = pBuild->RenderStream(
        NULL,       // Output pin category
        NULL,       // Media type
        pSrc,       // Source filter
        pVComp,     // Compression filter
        pMux);      // Sink filter (the AVI Mux)
```



En el diagrama siguiente se muestra el gráfico de filtro hasta ahora.

![secuencia de vídeo representada](images/avi2avi3.png)

Suponiendo que el archivo de origen tiene una secuencia de audio, el filtro de [divisor de AVI](avi-splitter-filter.md) ha creado un PIN de salida para el audio. Para conectar este pin, vuelva a llamar a RenderStream:


```C++
hr = pBuild->RenderStream(NULL, NULL, pSrc, NULL, pMux);
```



Aquí no se especifica ningún filtro de compresión. El PIN de salida del filtro de origen ya está conectado, por lo que el método RenderStream busca un PIN de salida no conectado en el filtro divisor. Busca el PIN de audio y lo conecta directamente al filtro MUX. Si el archivo de origen no tiene una secuencia de audio, se producirá un error en la segunda llamada a RenderStream. Este es el comportamiento esperado. El gráfico se completa después de la primera llamada a RenderStream, por lo que el error en la segunda llamada es inofensivo.

En este ejemplo, es importante el orden de las dos llamadas a RenderStream. Dado que la segunda llamada no especifica un compresor, conectará cualquier PIN no conectado desde el divisor de AVI. Si realiza esta llamada antes de la otra, podría conectar la secuencia de vídeo a AVI MUX sin su compresor de vídeo. Por lo tanto, la llamada más específica (con el filtro de compresión) debe aparecer en primer lugar.

En la explicación anterior se supone que el archivo de código fuente es un archivo AVI. Sin embargo, esta técnica también funciona con otros tipos de archivo, como los archivos MPEG. El gráfico de filtros resultante será algo diferente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Volver a comprimir un archivo AVI](recompressing-an-avi-file.md)
</dt> </dl>

 

 



