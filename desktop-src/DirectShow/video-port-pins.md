---
description: PIN de puerto de vídeo
ms.assetid: a6be24e5-7937-48f1-abeb-3f29c3deeafd
title: PIN de puerto de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d13ab4ad63995dd38460bf29064035c9c1802dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911053"
---
# <a name="video-port-pins"></a><span data-ttu-id="976f5-103">PIN de puerto de vídeo</span><span class="sxs-lookup"><span data-stu-id="976f5-103">Video Port Pins</span></span>

<span data-ttu-id="976f5-104">Un dispositivo de captura con un puerto de vídeo de hardware podría usar las extensiones de puerto de vídeo (VPE) de Microsoft® DirectX®.</span><span class="sxs-lookup"><span data-stu-id="976f5-104">A capture device with a hardware video port might use the video port extensions (VPE) in Microsoft® DirectX®.</span></span> <span data-ttu-id="976f5-105">Si es así, el filtro de captura tendrá un PIN de puerto de vídeo (VP).</span><span class="sxs-lookup"><span data-stu-id="976f5-105">If so, the capture filter will have a video port (VP) pin.</span></span> <span data-ttu-id="976f5-106">No se transmiten datos de vídeo desde el eje VP a través del gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="976f5-106">No video data travels from the VP pin through the filter graph.</span></span> <span data-ttu-id="976f5-107">En su lugar, los fotogramas de vídeo se producen en hardware y se envían directamente a la memoria de vídeo.</span><span class="sxs-lookup"><span data-stu-id="976f5-107">Instead, video frames are produced in hardware and sent directly to video memory.</span></span> <span data-ttu-id="976f5-108">The VP PIN permite enviar mensajes de control al hardware.</span><span class="sxs-lookup"><span data-stu-id="976f5-108">The VP pin allows control messages to be sent to the hardware.</span></span>

<span data-ttu-id="976f5-109">Es importante conectar la VP, incluso si la aplicación solo realiza la captura de archivos sin vista previa.</span><span class="sxs-lookup"><span data-stu-id="976f5-109">It is important to connect the VP pin, even if your application only performs file capture with no preview.</span></span> <span data-ttu-id="976f5-110">Si deja el PIN sin conexión, el gráfico no se ejecutará correctamente.</span><span class="sxs-lookup"><span data-stu-id="976f5-110">If you leave the pin unconnected, the graph will not run correctly.</span></span> <span data-ttu-id="976f5-111">Esto es diferente de los pin de vista previa, que no tienen que estar conectados.</span><span class="sxs-lookup"><span data-stu-id="976f5-111">This is different from preview pins, which do not have to be connected.</span></span>

<span data-ttu-id="976f5-112">Los distintos representadores de vídeo de DirectShow proporcionan compatibilidad variable para VP PIN:</span><span class="sxs-lookup"><span data-stu-id="976f5-112">The different DirectShow video renderers provide varying support for VP pins:</span></span>

-   <span data-ttu-id="976f5-113">Representador de vídeo: Conecte el código de la VP al pin 0 en el filtro del [mezclador de superposición](overlay-mixer-filter.md) y conecte el filtro de mezclador superpuesto al representador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="976f5-113">Video Renderer: Connect the VP pin to pin 0 on the [Overlay Mixer](overlay-mixer-filter.md) filter, and connect the Overlay Mixer filter to the Video Renderer.</span></span>
-   <span data-ttu-id="976f5-114">VMR-7: Conecte el código VP al filtro del [Administrador de puertos de vídeo](video-port-manager.md) y conecte el administrador de puertos de vídeo a VMR-7.</span><span class="sxs-lookup"><span data-stu-id="976f5-114">VMR-7: Connect the VP pin to the [Video Port Manager](video-port-manager.md) filter, and connect the Video Port Manager to the VMR-7.</span></span>
-   <span data-ttu-id="976f5-115">VMR-9: no puede usar la VMR-9 Si el dispositivo tiene una VP, porque Direct3D 9 no admite puertos de vídeo.</span><span class="sxs-lookup"><span data-stu-id="976f5-115">VMR-9: You cannot use the VMR-9 if the device has a VP pin, because Direct3D 9 does not support video ports.</span></span> <span data-ttu-id="976f5-116">Use el representador de vídeo o VMR-7.</span><span class="sxs-lookup"><span data-stu-id="976f5-116">Use either the Video Renderer or the VMR-7.</span></span>

<span data-ttu-id="976f5-117">En los escenarios de puerto de vídeo, se recomienda usar el mezclador de superposición y el representador de vídeo en el administrador de puertos de vídeo y VMR-7, ya que no todos los controladores son compatibles con el administrador de puertos de vídeo.</span><span class="sxs-lookup"><span data-stu-id="976f5-117">For video port scenarios, the Overlay Mixer and Video Renderer are recommended over the Video Port Manager and VMR-7, because not all drivers support the Video Port Manager.</span></span> <span data-ttu-id="976f5-118">En general, el mezclador de superposición es la opción más confiable para los puertos de vídeo.</span><span class="sxs-lookup"><span data-stu-id="976f5-118">In general, the Overlay Mixer is the most reliable option for video ports.</span></span>

<span data-ttu-id="976f5-119">El método [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) inserta automáticamente el mezclador de superposición si hay un código de VP.</span><span class="sxs-lookup"><span data-stu-id="976f5-119">The [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method automatically inserts the Overlay Mixer if there is a VP pin.</span></span> <span data-ttu-id="976f5-120">Si va a compilar el gráfico sin utilizar este método, debe comprobar si hay un PIN de puerto de vídeo en el filtro de captura y, si hay alguno, conéctelo al filtro de mezclador de superposición, como se muestra en el diagrama siguiente.</span><span class="sxs-lookup"><span data-stu-id="976f5-120">If you are building the graph without using this method, you should check for a video port pin on the capture filter, and if one is present, connect it to the Overlay Mixer filter, as shown in the following diagram.</span></span>

![conexión de un PIN de puerto de vídeo al filtro de mezclador de superposición.](images/vidcap11.png)

<span data-ttu-id="976f5-122">Puede usar el método [**ICaptureGraphBuilder2:: FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) para buscar una VP en el filtro de captura:</span><span class="sxs-lookup"><span data-stu-id="976f5-122">You can use the [**ICaptureGraphBuilder2::FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) method to search for a VP pin on the capture filter:</span></span>


```C++
hr = pBuild->FindPin(
    pCap,                    // Pointer to the capture filter.
    PINDIR_OUTPUT,           // Look for an output pin.
    &PIN_CATEGORY_VIDEOPORT, // Look for a video port pin.
    NULL,                    // Any media type.
    FALSE,                   // Pin can be connected.
    0,                       // Retrieve the first matching pin.
    &pVPPin                  // Receives a pointer to the pin.
);
```



<span data-ttu-id="976f5-123">Después de agregar el mezclador de superposición al gráfico, vuelva a llamar a **FindPin** para buscar el pin 0 en el mezclador de superposición.</span><span class="sxs-lookup"><span data-stu-id="976f5-123">After you add the Overlay Mixer to the graph, call **FindPin** again to find pin 0 on the Overlay Mixer.</span></span> <span data-ttu-id="976f5-124">El pin 0 siempre es el primer PIN de entrada del filtro.</span><span class="sxs-lookup"><span data-stu-id="976f5-124">Pin 0 is always the first input pin on the filter.</span></span>


```C++
pBuild->FindPin(pOvMix, PINDIR_INPUT, NULL, NULL, TRUE, 0, &pOVPin);
```



<span data-ttu-id="976f5-125">Conecte los dos PIN llamando a [**IGraphBuilder:: Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect).</span><span class="sxs-lookup"><span data-stu-id="976f5-125">Connect the two pins by calling [**IGraphBuilder::Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect).</span></span>


```C++
pGraph->Connect(pVPPin, pOvPin);
```



<span data-ttu-id="976f5-126">A continuación, conecte el PIN de salida del mezclador de superposición al filtro de representador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="976f5-126">Then connect the Overlay Mixer's output pin to the Video Renderer filter.</span></span> <span data-ttu-id="976f5-127">Puede ocultar el vídeo mediante una llamada a los métodos visibles [**IVideoWindow::p UT \_ Autoshow**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) y [**IVideoWindow \_ ::P UT**](/windows/desktop/api/Control/nf-control-ivideowindow-put_visible) en Filter Graph Manager.</span><span class="sxs-lookup"><span data-stu-id="976f5-127">You can hide the video by calling the [**IVideoWindow::put\_AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) and [**IVideoWindow::put\_Visible**](/windows/desktop/api/Control/nf-control-ivideowindow-put_visible) methods on the Filter Graph Manager.</span></span>

<span data-ttu-id="976f5-128">En el caso de los sintonizadores de TV, el filtro de captura también puede tener un PIN de puerto de vídeo VBI (categoría de PIN de \_ \_ videopuerto \_ VBI).</span><span class="sxs-lookup"><span data-stu-id="976f5-128">For TV tuners, the capture filter might also have a video port VBI pin (PIN\_CATEGORY\_VIDEOPORT\_VBI).</span></span> <span data-ttu-id="976f5-129">Si es así, conecte ese pin al filtro de [asignador de superficie de VBI](vbi-surface-allocator.md) .</span><span class="sxs-lookup"><span data-stu-id="976f5-129">If so, connect that pin to the [VBI Surface Allocator](vbi-surface-allocator.md) filter.</span></span> <span data-ttu-id="976f5-130">Para obtener más información, vea [ver subtítulos cerrados](viewing-closed-captions.md).</span><span class="sxs-lookup"><span data-stu-id="976f5-130">For more information, see [Viewing Closed Captions](viewing-closed-captions.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="976f5-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="976f5-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="976f5-132">Temas de captura avanzada</span><span class="sxs-lookup"><span data-stu-id="976f5-132">Advanced Capture Topics</span></span>](advanced-capture-topics.md)
</dt> <dt>

[<span data-ttu-id="976f5-133">Usar el mezclador de superposición en la captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="976f5-133">Using the Overlay Mixer in Video Capture</span></span>](using-the-overlay-mixer-in-video-capture.md)
</dt> </dl>

 

 



