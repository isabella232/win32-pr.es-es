---
description: Creación del archivo de recompresión Graph
ms.assetid: 8f25c60e-30be-4cc4-b924-b8d6654604d3
title: Creación del archivo de recompresión Graph
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0432f51e5309a308b32535993fef04da1762d45f179e1ab3a6826d4c5432b02b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118159114"
---
# <a name="building-the-recompression-graph"></a>Creación del archivo de recompresión Graph

Un gráfico de filtros típico para la recompresión de archivos AVI tiene un aspecto similar al siguiente:

![gráfico de recompresión avi](images/avi2avi4.png)

El [filtro divisor AVI](avi-splitter-filter.md) extrae datos del filtro de origen de archivo [(asincrónico)](file-source--async--filter.md) y los analiza en secuencias de audio y vídeo. El descomprimidor de vídeo descodifica el vídeo comprimido, donde lo vuelve a comprimir el vídeo. La elección de los descompresores depende del archivo de código fuente; Intelligent Conectar lo [controlará Conectar](intelligent-connect.md). La aplicación debe elegir el resalte, normalmente mediante la presentación de una lista al usuario. (Consulte [Elección de un filtro de compresión).](choosing-a-compression-filter.md)

A continuación, el vídeo comprimido va al filtro [Mux de AVI.](avi-mux-filter.md) La secuencia de audio de este ejemplo no está comprimida, por lo que va directamente desde el divisor AVI al Mux avi. El Mux avi intercala las dos secuencias y el filtro [del](file-writer-filter.md) escritor de archivos escribe la salida en el disco. Tenga en cuenta que el Mux avi es necesario incluso si el archivo original no tiene una secuencia de audio.

La manera más fácil de compilar este gráfico de filtro es usar [Capture Graph Builder,](capture-graph-builder.md)que es un componente DirectShow para crear gráficos de captura y otros gráficos de filtro personalizados.

Para empezar, llame a CoCreateInstance para crear capture Graph Builder:


```C++
ICaptureGraphBuilder2 *pBuild = NULL;
hr = CoCreateInstance(CLSID_CaptureGraphBuilder2, 
                        NULL, CLSCTX_INPROC_SERVER,
    IID_ICaptureGraphBuilder2, (void **)&pBuild);
```



A continuación, use capture Graph Builder para compilar el gráfico de filtros:

1.  Compile la sección de representación del gráfico, que incluye el filtro AVI Mux y [el escritor de archivos](file-writer-filter.md).
2.  Agregue el filtro de origen y el filtro de compresión al gráfico.
3.  Conectar el filtro de origen al filtro MUX. El generador de gráficos de captura inserta los filtros de divisor y descodificador necesarios para analizar el archivo de origen. También puede enrutar las secuencias de audio y vídeo a través de filtros de compresión.

En las secciones siguientes se explica cada uno de estos pasos.

Compilación de la sección de representación

Para compilar la sección de representación del gráfico, llame al [**método ICaptureGraphBuilder2::SetOutputFileName.**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) Este método toma parámetros de entrada que especifican el subtipo de medio para la salida y el nombre del archivo de salida. Devuelve punteros al filtro MUX y al escritor de archivos. El filtro MUX es necesario para la siguiente fase de creación de grafos. El puntero al escritor de archivos no es necesario para este ejemplo, por lo que el parámetro puede ser **NULL**:


```C++
IBaseFilter *pMux = NULL;
hr = pBuild->SetOutputFileName(
        &MEDIASUBTYPE_Avi, // File type. 
        wszOutputFile,     // File name, as a wide-character string.
        &pMux,             // Receives a pointer to the multiplexer.
        NULL);             // Receives a pointer to the file writer. 
```



Cuando el método vuelve, el filtro MUX tiene un recuento de referencias pendiente, así que asegúrese de liberar el puntero más adelante.

En el diagrama siguiente se muestra el gráfico de filtros en este punto.

![sección de representación del gráfico de filtros](images/avi2avi1.png)

El filtro MUX expone dos interfaces para controlar el formato AVI:

-   [**IConfigInterleaving Interface :**](/windows/desktop/api/Strmif/nn-strmif-iconfiginterleaving)establece el modo de intercalación.
-   [**Interfaz IConfigAviMux:**](/windows/desktop/api/Strmif/nn-strmif-iconfigavimux)establece el flujo maestro y el índice de compatibilidad de AVI.

Agregar los filtros de origen y compresión

El siguiente paso consiste en agregar los filtros de origen y compresión al gráfico de filtros. Capture Graph Builder crea automáticamente una instancia del Administrador de filtros Graph cuando se llama a SetOutputFileName. Obtenga un puntero a él mediante una llamada [**al método ICaptureGraphBuilder2::GetFiltergraph:**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-getfiltergraph)


```C++
IGraphBuilder *pGraph = NULL;
hr = pBuild->GetFiltergraph(&pGraph);
```



Ahora, llame [**al método IGraphBuilder::AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) para agregar el filtro Async File Source y el método [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) para agregar el vídeo:


```C++
IBaseFilter *pSrc = NULL;
hr = pGraph->AddSourceFilter(wszInputFile, L"Source Filter", &pSrc);
hr = pGraph->AddFilter(pVComp, L"Compressor");
```



En este momento, el filtro de origen y el filtro de compresión no están conectados a nada más en el gráfico, como se muestra en la ilustración siguiente:

![gráfico de filtro con filtros de origen y compresión](images/avi2avi2.png)

Conectar origen al Mux

El último paso consiste en conectar el filtro de origen al filtro Mux de AVI, a través del vídeo de vídeo. Use el [**método ICaptureGraphBuilder2::RenderStream,**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) que conecta una clavija de salida del filtro de origen a un filtro de receptor especificado, opcionalmente a través de un filtro de compresión.

Los dos primeros parámetros especifican cuál de los pines del filtro de origen se va a conectar mediante la designación de una categoría de pin y un tipo de medio. El filtro Async File Source solo tiene un pin de salida, por lo que estos parámetros deben ser **NULL.** Los tres parámetros siguientes especifican el filtro de origen, el filtro de compresión (si hay alguno) y el filtro Mux.

En el ejemplo de código siguiente se representa la secuencia de vídeo a través de la secuencia de vídeo:


```C++
hr = pBuild->RenderStream(
        NULL,       // Output pin category
        NULL,       // Media type
        pSrc,       // Source filter
        pVComp,     // Compression filter
        pMux);      // Sink filter (the AVI Mux)
```



En el diagrama siguiente se muestra el gráfico de filtros hasta ahora.

![secuencia de vídeo representado](images/avi2avi3.png)

Suponiendo que el archivo de origen tiene una secuencia de audio, el filtro [divisor AVI](avi-splitter-filter.md) ha creado un pin de salida para el audio. Para conectar este pin, vuelva a llamar a RenderStream:


```C++
hr = pBuild->RenderStream(NULL, NULL, pSrc, NULL, pMux);
```



Aquí no se especifica ningún filtro de compresión. El pin de salida del filtro de origen ya está conectado, por lo que el método RenderStream busca un pin de salida no conectado en el filtro divisor. Busca la clavija de audio y la conecta directamente al filtro MUX. Si el archivo de origen no tiene una secuencia de audio, se producirá un error en la segunda llamada a RenderStream. Este es el comportamiento esperado. El gráfico se completa después de la primera llamada a RenderStream, por lo que el error en la segunda llamada es inofensivo.

En este ejemplo, el orden de las dos llamadas RenderStream es importante. Dado que la segunda llamada no especifica un resalte, conectará cualquier pin no conectado desde el divisor AVI. Si realiza esta llamada antes que la otra, podría conectar la secuencia de vídeo a AVI Mux, sin el vídeo. Por lo tanto, la llamada más específica (con el filtro de compresión) debe producirse primero.

En la explicación anterior se ha supuesto que el archivo de origen es un archivo AVI. Sin embargo, esta técnica también funciona con otros tipos de archivo, como archivos MPEG. El gráfico de filtros resultante será algo diferente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Volver acomprimir un archivo AVI](recompressing-an-avi-file.md)
</dt> </dl>

 

 



