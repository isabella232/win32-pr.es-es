---
description: Cómo reproducir un archivo
ms.assetid: 3d8c5d06-8690-4298-a1d1-f21af35bcfd4
title: Cómo reproducir un archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7d20a021ec5053746c279598d08117c6b25a5fe6a52946fed56f19eda3cafe1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118401153"
---
# <a name="how-to-play-a-file"></a>Cómo reproducir un archivo

Este artículo está pensado para ofrecer el tipo de programación DirectShow programación. Presenta una aplicación de consola sencilla que reproduce un archivo de audio o vídeo. El programa tiene solo unas pocas líneas de longitud, pero muestra parte de la capacidad de DirectShow programación.

Como se describe en el [artículo Introducción a DirectShow programación de](introduction-to-directshow-application-programming.md) aplicaciones, DirectShow aplicación siempre realiza los mismos pasos básicos:

1.  Cree una instancia de [Filter Graph Manager](filter-graph-manager.md).
2.  Use el Administrador de Graph filtros para crear un gráfico de filtros.
3.  Ejecute el gráfico, lo que hace que los datos se muevan a través de los filtros.

Para compilar y vincular el código de este tema, incluya el archivo de encabezado Dshow.h y el vínculo al archivo de biblioteca estática strmiids.lib. Para obtener más información, vea [Compilar DirectShow aplicaciones](setting-up-the-build-environment.md).

Para empezar, [**llame a CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) [**o CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) para inicializar la biblioteca COM:


```C++
HRESULT hr = CoInitialize(NULL);
if (FAILED(hr))
{
    // Add error-handling code here. (Omitted for clarity.)
}
```



Para que todo sea sencillo, en este ejemplo se omite el valor devuelto, pero siempre se debe comprobar el **valor HRESULT** desde cualquier llamada de método.

A continuación, [**llame a CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) para crear el administrador Graph filtros:


```C++
IGraphBuilder *pGraph;
HRESULT hr = CoCreateInstance(CLSID_FilterGraph, NULL, 
    CLSCTX_INPROC_SERVER, IID_IGraphBuilder, (void **)&pGraph);
```



Como se muestra, el identificador de clase (CLSID) es CLSID \_ FilterGraph. El Administrador Graph filtro se proporciona mediante un archivo DLL en proceso, por lo que el contexto de ejecución es **CLSCTX \_ INPROC \_ SERVER**. DirectShow admite el modelo de subprocesamiento libre, por lo que también puede llamar a [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) con la **marca COINIT \_ MULTITHREADED.**

La llamada a [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) devuelve la [**interfaz IGraphBuilder,**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) que contiene principalmente métodos para compilar el gráfico de filtro. Para este ejemplo se necesitan otras dos interfaces:

-   [**IMediaControl controla**](/windows/desktop/api/Control/nn-control-imediacontrol) el streaming. Contiene métodos para detener e iniciar el gráfico.
-   [**IMediaEvent tiene**](/windows/desktop/api/Control/nn-control-imediaevent) métodos para obtener eventos del Administrador de Graph Filtros. En este ejemplo, la interfaz se usa para esperar a que se complete la reproducción.

El Administrador de filtros Graph expone ambas interfaces. Use el puntero [**IGraphBuilder devuelto**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) para consultarlos:


```C++
IMediaControl *pControl;
IMediaEvent   *pEvent;
hr = pGraph->QueryInterface(IID_IMediaControl, (void **)&pControl);
hr = pGraph->QueryInterface(IID_IMediaEvent, (void **)&pEvent);
```



Ahora puede crear el gráfico de filtros. Para la reproducción de archivos, esto se realiza mediante una sola llamada de método:


```C++
hr = pGraph->RenderFile(L"C:\\Example.avi", NULL);
```



El [**método IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) compila un gráfico de filtro que puede reproducir el archivo especificado. El primer parámetro es el nombre de archivo, representado como una cadena de caracteres anchos (2 bytes). El segundo parámetro está reservado y debe ser **null.**

Este método puede producir un error si el archivo especificado no existe o si no se reconoce el formato de archivo. Suponiendo que el método se realiza correctamente, sin embargo, el gráfico de filtros ya está listo para la reproducción. Para ejecutar el gráfico, llame al [**método IMediaControl::Run:**](/windows/desktop/api/Control/nf-control-imediacontrol-run)


```C++
hr = pControl->Run();
```



Cuando se ejecuta el gráfico de filtros, los datos se mueven a través de los filtros y se representan como vídeo y audio. La reproducción se produce en un subproceso independiente. Puede esperar a que se complete la reproducción llamando al [**método IMediaEvent::WaitForCompletion:**](/windows/desktop/api/Control/nf-control-imediaevent-waitforcompletion)


```C++
long evCode = 0;
pEvent->WaitForCompletion(INFINITE, &evCode);
```



Este método se bloquea hasta que se realiza la reproducción del archivo o hasta que transcurre el intervalo de tiempo de espera especificado. El valor INFINITE significa que la aplicación se bloquea indefinidamente hasta que se realiza la reproducción del archivo. Para obtener un ejemplo más realista del control de eventos, vea Responder a [eventos](responding-to-events.md).

Cuando finalice la aplicación, suelte los punteros de interfaz y cierre la biblioteca COM:


```C++
pControl->Release();
pEvent->Release();
pGraph->Release();
CoUninitialize();
```



## <a name="example-code"></a>Código de ejemplo

Este es el código completo del ejemplo descrito en este artículo:


```C++
#include <dshow.h>
void main(void)
{
    IGraphBuilder *pGraph = NULL;
    IMediaControl *pControl = NULL;
    IMediaEvent   *pEvent = NULL;

    // Initialize the COM library.
    HRESULT hr = CoInitialize(NULL);
    if (FAILED(hr))
    {
        printf("ERROR - Could not initialize COM library");
        return;
    }

    // Create the filter graph manager and query for interfaces.
    hr = CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC_SERVER, 
                        IID_IGraphBuilder, (void **)&pGraph);
    if (FAILED(hr))
    {
        printf("ERROR - Could not create the Filter Graph Manager.");
        return;
    }

    hr = pGraph->QueryInterface(IID_IMediaControl, (void **)&pControl);
    hr = pGraph->QueryInterface(IID_IMediaEvent, (void **)&pEvent);

    // Build the graph. IMPORTANT: Change this string to a file on your system.
    hr = pGraph->RenderFile(L"C:\\Example.avi", NULL);
    if (SUCCEEDED(hr))
    {
        // Run the graph.
        hr = pControl->Run();
        if (SUCCEEDED(hr))
        {
            // Wait for completion.
            long evCode;
            pEvent->WaitForCompletion(INFINITE, &evCode);

            // Note: Do not use INFINITE in a real application, because it
            // can block indefinitely.
        }
    }
    pControl->Release();
    pEvent->Release();
    pGraph->Release();
    CoUninitialize();
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tareas DirectShow básicas](basic-directshow-tasks.md)
</dt> </dl>

 

 
