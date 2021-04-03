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
# <a name="about-the-capture-graph-builder"></a><span data-ttu-id="49020-103">Acerca del generador de gráficos de captura</span><span class="sxs-lookup"><span data-stu-id="49020-103">About the Capture Graph Builder</span></span>

<span data-ttu-id="49020-104">Un gráfico de filtros que realiza la captura de vídeo o audio se denomina *gráfico de captura*.</span><span class="sxs-lookup"><span data-stu-id="49020-104">A filter graph that performs video or audio capture is called a *capture graph*.</span></span> <span data-ttu-id="49020-105">Los gráficos de captura suelen ser más complicados que los gráficos de reproducción de archivos.</span><span class="sxs-lookup"><span data-stu-id="49020-105">Capture graphs are often more complicated than file playback graphs.</span></span> <span data-ttu-id="49020-106">Para facilitar a las aplicaciones la creación de gráficos de captura, DirectShow proporciona un objeto auxiliar denominado generador de gráficos de captura.</span><span class="sxs-lookup"><span data-stu-id="49020-106">To make it easier for applications to build capture graphs, DirectShow provides a helper object called the Capture Graph Builder.</span></span> <span data-ttu-id="49020-107">El generador de gráficos de captura expone la interfaz [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) , que contiene métodos para compilar y controlar un gráfico de captura.</span><span class="sxs-lookup"><span data-stu-id="49020-107">The Capture Graph Builder exposes the [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) interface, which contains methods for building and controlling a capture graph.</span></span> <span data-ttu-id="49020-108">En el diagrama siguiente se ilustra el generador de gráficos de captura y la interfaz **ICaptureGraphBuilder2** .</span><span class="sxs-lookup"><span data-stu-id="49020-108">The following diagram illustrates the Capture Graph Builder and the **ICaptureGraphBuilder2** interface.</span></span>

![usar el generador de gráficos de captura](images/cgb01.png)

<span data-ttu-id="49020-110">Empiece por llamar a CoCreateInstance para crear nuevas instancias del generador de gráficos de captura y el administrador de gráficos de filtro.</span><span class="sxs-lookup"><span data-stu-id="49020-110">Start by calling CoCreateInstance to create new instances of the Capture Graph Builder and the Filter Graph Manager.</span></span> <span data-ttu-id="49020-111">A continuación, inicialice el generador de gráficos de captura mediante una llamada a [**ICaptureGraphBuilder2:: SetFiltergraph**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setfiltergraph) con un puntero a la interfaz [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) del administrador de gráficos de filtro.</span><span class="sxs-lookup"><span data-stu-id="49020-111">Then initialize the Capture Graph Builder by calling [**ICaptureGraphBuilder2::SetFiltergraph**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setfiltergraph) with a pointer to the Filter Graph Manager's [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) interface.</span></span> <span data-ttu-id="49020-112">En el siguiente diagrama se muestra este proceso.</span><span class="sxs-lookup"><span data-stu-id="49020-112">The following diagram illustrates this process.</span></span>

![inicializar el generador de gráficos de captura](images/cgb03.png)

<span data-ttu-id="49020-114">En el código siguiente se muestra una función auxiliar para realizar estos pasos:</span><span class="sxs-lookup"><span data-stu-id="49020-114">The following code shows a helper function to perform these steps:</span></span>


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



<span data-ttu-id="49020-115">A lo largo de esta sección sobre la captura de vídeo, se supone que está usando el generador de gráficos de captura para crear el gráfico de captura.</span><span class="sxs-lookup"><span data-stu-id="49020-115">Throughout this section on video capture, it is assumed that you are using the Capture Graph Builder to create the capture graph.</span></span> <span data-ttu-id="49020-116">Sin embargo, es posible crear gráficos de captura por completo mediante métodos IGraphBuilder.</span><span class="sxs-lookup"><span data-stu-id="49020-116">However, it is possible to build capture graphs entirely by using IGraphBuilder methods.</span></span> <span data-ttu-id="49020-117">Esto se considera un tema avanzado, sin embargo, y se prefieren los métodos del generador de gráficos de captura.</span><span class="sxs-lookup"><span data-stu-id="49020-117">This is considered an advanced topic, however, and the Capture Graph Builder methods are preferred.</span></span> <span data-ttu-id="49020-118">Para obtener más información, vea [temas de captura avanzada](advanced-capture-topics.md).</span><span class="sxs-lookup"><span data-stu-id="49020-118">For more information, see [Advanced Capture Topics](advanced-capture-topics.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="49020-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="49020-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="49020-120">Acerca de la captura de vídeo en DirectShow</span><span class="sxs-lookup"><span data-stu-id="49020-120">About Video Capture in DirectShow</span></span>](about-video-capture-in-directshow.md)
</dt> </dl>

 

 



