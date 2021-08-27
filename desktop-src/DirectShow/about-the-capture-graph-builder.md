---
description: Acerca de Capture Graph Builder
ms.assetid: 9399a06e-7305-41e8-aefe-3d158052a8ed
title: Acerca de Capture Graph Builder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d6ef82a160ada6e53fe6d2db830efa85118eb699074630905cd41f0b5412ca2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118664527"
---
# <a name="about-the-capture-graph-builder"></a>Acerca de Capture Graph Builder

Un gráfico de filtro que realiza la captura de vídeo o audio se denomina gráfico *de captura.* Los gráficos de captura suelen ser más complicados que los gráficos de reproducción de archivos. Para facilitar a las aplicaciones la compilación de gráficos de captura, DirectShow proporciona un objeto auxiliar denominado Capture Graph Builder. Capture Graph Builder expone la [**interfaz ICaptureGraphBuilder2,**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) que contiene métodos para compilar y controlar un gráfico de captura. En el diagrama siguiente se muestra la Graph Builder y la **interfaz ICaptureGraphBuilder2.**

![uso del generador de gráficos de captura](images/cgb01.png)

Para empezar, llame a CoCreateInstance para crear nuevas instancias de Capture Graph Builder y filter Graph Manager. A continuación, inicialice capture Graph Builder mediante una llamada a [**ICaptureGraphBuilder2::SetFiltergraph**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setfiltergraph) con un puntero a la interfaz [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) del Administrador de filtros Graph Manager. En el siguiente diagrama se muestra este proceso.

![inicialización del generador de gráficos de captura](images/cgb03.png)

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



A lo largo de esta sección sobre la captura de vídeo, se supone que usa Capture Graph Builder para crear el gráfico de captura. Sin embargo, es posible compilar gráficos de captura por completo mediante métodos IGraphBuilder. Sin embargo, esto se considera un tema avanzado y se prefieren los métodos capture Graph Builder. Para obtener más información, vea [Advanced Capture Topics](advanced-capture-topics.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de la captura de vídeo en DirectShow](about-video-capture-in-directshow.md)
</dt> </dl>

 

 



