---
description: Control de eventos Repaint en la captura de vídeo
ms.assetid: 80739be7-fa38-409d-a827-d788d3044abe
title: Control de eventos Repaint en la captura de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 418ca42ebc80b338b077336fdac48a01dfb8509e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103997990"
---
# <a name="handling-repaint-events-in-video-capture"></a><span data-ttu-id="5ee72-103">Control de eventos Repaint en la captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="5ee72-103">Handling Repaint Events in Video Capture</span></span>

<span data-ttu-id="5ee72-104">Si crea un gráfico de captura de vídeo sin usar la interfaz [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) y obtiene una vista previa del vídeo con el filtro de representador de vídeo anterior, debe invalidar el control predeterminado de los eventos de [**\_ Repaint de EC**](ec-repaint.md) .</span><span class="sxs-lookup"><span data-stu-id="5ee72-104">If you build a video capture graph without using the [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) interface, and you preview the video using the old Video Renderer filter, then you should override the default handling for [**EC\_REPAINT**](ec-repaint.md) events.</span></span> <span data-ttu-id="5ee72-105">Consulte el administrador de gráficos de filtro para la interfaz [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) y llame al método [**IMediaEvent:: CancelDefaultHandling**](/windows/desktop/api/Control/nf-control-imediaevent-canceldefaulthandling) con el valor EC \_ Repaint:</span><span class="sxs-lookup"><span data-stu-id="5ee72-105">Query the Filter Graph Manager for the [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) interface and call the [**IMediaEvent::CancelDefaultHandling**](/windows/desktop/api/Control/nf-control-imediaevent-canceldefaulthandling) method with the value EC\_REPAINT:</span></span>


```C++
IMediaEvent *pEvent = 0;
hr = pGraph->QueryInterface(IID_IMediaEvent, (void**)&pEvent);
if (SUCCEEDED(hr))
{
    pEvent->CancelDefaultHandling (EC_REPAINT);
    pEvent->Release();
}
```



<span data-ttu-id="5ee72-106">Esto evita un posible error que puede dañar el archivo de captura.</span><span class="sxs-lookup"><span data-stu-id="5ee72-106">This prevents a possible error that can corrupt your capture file.</span></span> <span data-ttu-id="5ee72-107">Si el usuario cubre y detecta la ventana de vista previa, el filtro de representador de vídeo recibe un mensaje de dibujo de WM \_ .</span><span class="sxs-lookup"><span data-stu-id="5ee72-107">If the user covers and uncovers the preview window, the Video Renderer filter receives a WM\_PAINT message.</span></span> <span data-ttu-id="5ee72-108">De forma predeterminada, el representador de vídeo solicita un nuevo fotograma y Filter Graph Manager pausa el gráfico para señalar otro fotograma de vídeo.</span><span class="sxs-lookup"><span data-stu-id="5ee72-108">By default, the Video Renderer requests a new frame, and the Filter Graph Manager pauses the graph in order to cue another video frame.</span></span> <span data-ttu-id="5ee72-109">Si esto sucede mientras el gráfico está escribiendo un archivo, se dañará el archivo.</span><span class="sxs-lookup"><span data-stu-id="5ee72-109">If that happens while the graph is writing a file, it will corrupt the file.</span></span> <span data-ttu-id="5ee72-110">Invalidar el comportamiento predeterminado de \_ REpaint de EC evita que el representador solicite un nuevo marco.</span><span class="sxs-lookup"><span data-stu-id="5ee72-110">Overriding the default EC\_REPAINT behavior prevents the renderer from requesting a new frame.</span></span>

<span data-ttu-id="5ee72-111">No es necesario que realice este paso si está utilizando la interfaz **ICaptureGraphBuilder2** , porque el generador de gráficos de captura lo hace automáticamente.</span><span class="sxs-lookup"><span data-stu-id="5ee72-111">You do not have to perform this step if you are using the **ICaptureGraphBuilder2** interface, because the Capture Graph Builder does it for you automatically.</span></span> <span data-ttu-id="5ee72-112">Además, no es necesario si usa el representador de mezcla de vídeo (VMR) para la versión preliminar.</span><span class="sxs-lookup"><span data-stu-id="5ee72-112">Also, it is not required if you are using the Video Mixing Renderer (VMR) for preview.</span></span> <span data-ttu-id="5ee72-113">La VMR siempre tiene el fotograma más reciente disponible, por lo que no envía \_ eventos de Repaint de EC.</span><span class="sxs-lookup"><span data-stu-id="5ee72-113">The VMR always has the most recent frame available, so it does not send EC\_REPAINT events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5ee72-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5ee72-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ee72-115">Temas de captura avanzada</span><span class="sxs-lookup"><span data-stu-id="5ee72-115">Advanced Capture Topics</span></span>](advanced-capture-topics.md)
</dt> <dt>

[<span data-ttu-id="5ee72-116">Notificación de eventos en DirectShow</span><span class="sxs-lookup"><span data-stu-id="5ee72-116">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 



