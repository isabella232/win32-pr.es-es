---
description: Acerca del generador de gráficos de captura
ms.assetid: 9399a06e-7305-41e8-aefe-3d158052a8ed
title: Acerca del generador de gráficos de captura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae321665e0eae65a1d464bf87a12ac33e935d7ac
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103997967"
---
# <a name="about-the-capture-graph-builder"></a>Acerca del generador de gráficos de captura

Un gráfico de filtros que realiza la captura de vídeo o audio se denomina *gráfico de captura*. Los gráficos de captura suelen ser más complicados que los gráficos de reproducción de archivos. Para facilitar a las aplicaciones la creación de gráficos de captura, DirectShow proporciona un objeto auxiliar denominado generador de gráficos de captura. El generador de gráficos de captura expone la interfaz [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) , que contiene métodos para compilar y controlar un gráfico de captura. En el diagrama siguiente se ilustra el generador de gráficos de captura y la interfaz **ICaptureGraphBuilder2** .

![usar el generador de gráficos de captura](images/cgb01.png)

Empiece por llamar a CoCreateInstance para crear nuevas instancias del generador de gráficos de captura y el administrador de gráficos de filtro. A continuación, inicialice el generador de gráficos de captura mediante una llamada a [**ICaptureGraphBuilder2:: SetFiltergraph**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setfiltergraph) con un puntero a la interfaz [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) del administrador de gráficos de filtro. En el siguiente diagrama se muestra este proceso.

![inicializar el generador de gráficos de captura](images/cgb03.png)

En el código siguiente se muestra una función auxiliar para realizar estos pasos:


```C++
HRESULT InitCaptureGraphBuilder(
  IGraphBuilder **ppGraph,  // Receives the pointer.
  ICaptureGraphBuilder2 **ppBuild  // Receives the pointer.
)
{
    if (!ppGraph || !ppBuild)
    {
        return E_POINTER;
    }
    IGraphBuilder *pGraph = NULL;
    ICaptureGraphBuilder2 *pBuild = NULL;

    // Create the Capture Graph Builder.
    HRESULT hr = CoCreateInstance(CLSID_CaptureGraphBuilder2, NULL, 
        CLSCTX_INPROC_SERVER, IID_ICaptureGraphBuilder2, (void**)&pBuild );
    if (SUCCEEDED(hr))
    {
        // Create the Filter Graph Manager.
        hr = CoCreateInstance(CLSID_FilterGraph, 0, CLSCTX_INPROC_SERVER,
            IID_IGraphBuilder, (void**)&pGraph);
        if (SUCCEEDED(hr))
        {
            // Initialize the Capture Graph Builder.
            pBuild->SetFiltergraph(pGraph);

            // Return both interface pointers to the caller.
            *ppBuild = pBuild;
            *ppGraph = pGraph; // The caller must release both interfaces.
            return S_OK;
        }
        else
        {
            pBuild->Release();
        }
    }
    return hr; // Failed
}
```



A lo largo de esta sección sobre la captura de vídeo, se supone que está usando el generador de gráficos de captura para crear el gráfico de captura. Sin embargo, es posible crear gráficos de captura por completo mediante métodos IGraphBuilder. Esto se considera un tema avanzado, sin embargo, y se prefieren los métodos del generador de gráficos de captura. Para obtener más información, vea [temas de captura avanzada](advanced-capture-topics.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de la captura de vídeo en DirectShow](about-video-capture-in-directshow.md)
</dt> </dl>

 

 



