---
description: Cómo reproducir un archivo
ms.assetid: 3d8c5d06-8690-4298-a1d1-f21af35bcfd4
title: Cómo reproducir un archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc84ef751db318354da36454e6a30fd2ce4bd8e7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104423084"
---
# <a name="how-to-play-a-file"></a>Cómo reproducir un archivo

Este artículo está destinado a proporcionarle el tipo de programación de DirectShow. Presenta una sencilla aplicación de consola que reproduce un archivo de audio o vídeo. El programa tiene solo unas pocas líneas, pero muestra parte de la eficacia de la programación de DirectShow.

Como se describe [en el artículo Introducción a la programación de aplicaciones de DirectShow](introduction-to-directshow-application-programming.md) , una aplicación de DirectShow siempre realiza los mismos pasos básicos:

1.  Cree una instancia del [Administrador de gráficos de filtro](filter-graph-manager.md).
2.  Use el administrador de gráficos de filtro para generar un gráfico de filtro.
3.  Ejecute el gráfico, haciendo que los datos se muevan a través de los filtros.

Para compilar y vincular el código de este tema, incluya el archivo de encabezado DShow. h y un vínculo al archivo de biblioteca estática strmiids. lib. Para obtener más información, consulte [Building DirectShow Applications](setting-up-the-build-environment.md).

Para empezar, llame a [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) o a [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) para inicializar la biblioteca com:


```C++
HRESULT hr = CoInitialize(NULL);
if (FAILED(hr))
{
    // Add error-handling code here. (Omitted for clarity.)
}
```



Para simplificar las cosas, en este ejemplo se omite el valor devuelto, pero siempre debe comprobar el valor **HRESULT** de cualquier llamada al método.

A continuación, llame a [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) para crear el administrador de gráficos de filtro:


```C++
IGraphBuilder *pGraph;
HRESULT hr = CoCreateInstance(CLSID_FilterGraph, NULL, 
    CLSCTX_INPROC_SERVER, IID_IGraphBuilder, (void **)&pGraph);
```



Como se muestra, el identificador de clase (CLSID) es CLSID \_ FilterGraph. El administrador de gráficos de filtro lo proporciona un archivo DLL en proceso, por lo que el contexto de ejecución es **CLSCTX \_ Inproc \_ Server**. DirectShow admite el modelo de subprocesamiento libre, por lo que también puede llamar a [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) con la marca de **coinit \_ multiproceso** .

La llamada a [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) devuelve la interfaz [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) , que principalmente contiene métodos para generar el gráfico de filtro. En este ejemplo se necesitan otras dos interfaces:

-   Streaming de controles [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) . Contiene métodos para detener e iniciar el gráfico.
-   [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) tiene métodos para obtener eventos del administrador de gráficos de filtro. En este ejemplo, la interfaz se usa para esperar a que se complete la reproducción.

Ambas interfaces las expone el administrador de gráficos de filtro. Use el puntero [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) devuelto para consultarlos:


```C++
IMediaControl *pControl;
IMediaEvent   *pEvent;
hr = pGraph->QueryInterface(IID_IMediaControl, (void **)&pControl);
hr = pGraph->QueryInterface(IID_IMediaEvent, (void **)&pEvent);
```



Ahora puede crear el gráfico de filtro. Para la reproducción de archivos, esto se realiza mediante una única llamada al método:


```C++
hr = pGraph->RenderFile(L"C:\\Example.avi", NULL);
```



El método [**IGraphBuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) crea un gráfico de filtro que puede reproducir el archivo especificado. El primer parámetro es el nombre de archivo, representado como una cadena de caracteres anchos (de 2 bytes). El segundo parámetro está reservado y debe ser igual a **null**.

Este método puede producir un error si el archivo especificado no existe o no se reconoce el formato del archivo. Sin embargo, suponiendo que el método se ejecuta correctamente, el gráfico de filtro ya está listo para la reproducción. Para ejecutar el gráfico, llame al método [**IMediaControl:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) :


```C++
hr = pControl->Run();
```



Cuando se ejecuta el gráfico de filtro, los datos se mueven a través de los filtros y se representan como vídeo y audio. La reproducción se produce en un subproceso independiente. Puede esperar a que se complete la reproducción llamando al método [**IMediaEvent:: WaitForCompletion**](/windows/desktop/api/Control/nf-control-imediaevent-waitforcompletion) :


```C++
long evCode = 0;
pEvent->WaitForCompletion(INFINITE, &evCode);
```



Este método se bloquea hasta que se realiza la reproducción del archivo o hasta que transcurre el intervalo de tiempo de espera especificado. El valor infinito significa que la aplicación se bloquea indefinidamente hasta que el archivo termina de reproducirse. Para obtener un ejemplo más realista del control de eventos, vea [responder a eventos](responding-to-events.md).

Una vez finalizada la aplicación, libere los punteros de interfaz y cierre la biblioteca COM:


```C++
pControl->Release();
pEvent->Release();
pGraph->Release();
CoUninitialize();
```



## <a name="example-code"></a>Código de ejemplo

Este es el código completo para el ejemplo que se describe en este artículo:


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

[Tareas básicas de DirectShow](basic-directshow-tasks.md)
</dt> </dl>

 

 
