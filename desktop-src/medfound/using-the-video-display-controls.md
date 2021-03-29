---
description: Usar los controles de presentación de vídeo
ms.assetid: 09501d67-effb-41ce-a7b7-d2415acdf3ac
title: Usar los controles de presentación de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bbb9c83485faebc873b3e92502122c5497b4bb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811521"
---
# <a name="using-the-video-display-controls"></a><span data-ttu-id="2e080-103">Usar los controles de presentación de vídeo</span><span class="sxs-lookup"><span data-stu-id="2e080-103">Using the Video Display Controls</span></span>

<span data-ttu-id="2e080-104">La interfaz [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) controla cómo el representador de vídeo mejorado (EVR) muestra el vídeo en una ventana de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2e080-104">The [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) interface controls how the enhanced video renderer (EVR) displays video inside an application window.</span></span> <span data-ttu-id="2e080-105">Esta interfaz se puede usar en DirectShow o en Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="2e080-105">This interface can be used in either DirectShow or Media Foundation.</span></span> <span data-ttu-id="2e080-106">Internamente, el presentador predeterminado de EVR proporciona los controles de presentación de vídeo.</span><span class="sxs-lookup"><span data-stu-id="2e080-106">Internally, the video display controls are provided by the EVR's default presenter.</span></span> <span data-ttu-id="2e080-107">Si escribe un presentador personalizado, puede proporcionar la misma interfaz o definir una interfaz personalizada.</span><span class="sxs-lookup"><span data-stu-id="2e080-107">If you write a custom presenter, you can provide the same interface or define a custom interface.</span></span>

<span data-ttu-id="2e080-108">La manera correcta de obtener un puntero a la interfaz [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) depende de si está usando la versión DIRECTSHOW de EVR o la versión media Foundation.</span><span class="sxs-lookup"><span data-stu-id="2e080-108">The correct way to get a pointer to the [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) interface depends on whether you are using the DirectShow version of the EVR or the Media Foundation version.</span></span> <span data-ttu-id="2e080-109">En el Media Foundation EVR, también depende de si usa el EVR directamente o lo usa a través de la sesión multimedia (que es más habitual).</span><span class="sxs-lookup"><span data-stu-id="2e080-109">For the Media Foundation EVR, it also depends on whether you are using the EVR directly or using it through the Media Session (which is more typical).</span></span>

<span data-ttu-id="2e080-110">Para obtener un puntero a la interfaz [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) , haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2e080-110">To get a pointer to the [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) interface, do the following:</span></span>

1.  <span data-ttu-id="2e080-111">Obtiene un puntero a la interfaz [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) .</span><span class="sxs-lookup"><span data-stu-id="2e080-111">Get a pointer to the [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) interface.</span></span>

    -   <span data-ttu-id="2e080-112">Si usa el filtro EVR de DirectShow, llame a **QueryInterface** en el filtro.</span><span class="sxs-lookup"><span data-stu-id="2e080-112">If you are using the DirectShow EVR filter, call **QueryInterface** on the filter.</span></span>

    -   <span data-ttu-id="2e080-113">Si usa el receptor de medios EVR directamente, llame a **QueryInterface** en el receptor de medios.</span><span class="sxs-lookup"><span data-stu-id="2e080-113">If you are using the EVR media sink directly, call **QueryInterface** on the media sink.</span></span>

    -   <span data-ttu-id="2e080-114">Si usa la sesión multimedia, llame a **QueryInterface** en la sesión multimedia.</span><span class="sxs-lookup"><span data-stu-id="2e080-114">If you are using the Media Session, call **QueryInterface** on the Media Session.</span></span>

2.  <span data-ttu-id="2e080-115">Si usa la sesión multimedia, espere a que la sesión multimedia envíe el evento [MESessionTopologyStatus](mesessiontopologystatus.md) con el valor de estado MF \_ TOPOSTATUS \_ listo.</span><span class="sxs-lookup"><span data-stu-id="2e080-115">If you are using the Media Session, wait for the Media Session to send the [MESessionTopologyStatus](mesessiontopologystatus.md) event with a status value of MF\_TOPOSTATUS\_READY.</span></span> <span data-ttu-id="2e080-116">(En caso contrario, omita este paso).</span><span class="sxs-lookup"><span data-stu-id="2e080-116">(Skip this step otherwise.)</span></span>

3.  <span data-ttu-id="2e080-117">Llame a [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) para obtener la interfaz [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) .</span><span class="sxs-lookup"><span data-stu-id="2e080-117">Call [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) to get the [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) interface.</span></span> <span data-ttu-id="2e080-118">El identificador de servicio es el \_ servicio de representación de vídeo Mr \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="2e080-118">The service identifier is MR\_VIDEO\_RENDER\_SERVICE.</span></span>

<span data-ttu-id="2e080-119">Puede usar la interfaz [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) para realizar las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="2e080-119">You can use the [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) interface to perform the following tasks:</span></span>

-   <span data-ttu-id="2e080-120">Establezca la ventana de recorte.</span><span class="sxs-lookup"><span data-stu-id="2e080-120">Set the clipping window.</span></span>

-   <span data-ttu-id="2e080-121">Establezca los rectángulos de origen y de destino.</span><span class="sxs-lookup"><span data-stu-id="2e080-121">Set the source and destination rectangles.</span></span>

-   <span data-ttu-id="2e080-122">Actualice la ventana de vídeo en respuesta a los mensajes de ventana.</span><span class="sxs-lookup"><span data-stu-id="2e080-122">Update the video window in response to window messages.</span></span>

-   <span data-ttu-id="2e080-123">Habilitar o deshabilitar el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="2e080-123">Enable or disable full-screen mode.</span></span>

## <a name="clipping-window"></a><span data-ttu-id="2e080-124">Ventana de recorte</span><span class="sxs-lookup"><span data-stu-id="2e080-124">Clipping Window</span></span>

<span data-ttu-id="2e080-125">La aplicación debe proporcionar una ventana en la que EVR dibuje el vídeo.</span><span class="sxs-lookup"><span data-stu-id="2e080-125">The application must provide a window where the EVR draws the video.</span></span> <span data-ttu-id="2e080-126">Para establecer la ventana de recorte, llame a [**IMFVideoDisplayControl:: SetVideoWindow**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow) con un identificador a la ventana de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2e080-126">To set the clipping window, call [**IMFVideoDisplayControl::SetVideoWindow**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow) with a handle to the application window.</span></span>

<span data-ttu-id="2e080-127">Si crea el receptor de medios de EVR a través de su objeto de activación, este paso no es necesario.</span><span class="sxs-lookup"><span data-stu-id="2e080-127">If you create the EVR media sink through its activation object, this step is not required.</span></span> <span data-ttu-id="2e080-128">El objeto de activación llama automáticamente a [**SetVideoWindow**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow), mediante el identificador de ventana que proporcionó en la función [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) .</span><span class="sxs-lookup"><span data-stu-id="2e080-128">The activation object automatically calls [**SetVideoWindow**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow), using the window handle that you provided in the [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) function.</span></span>

## <a name="source-and-destination-rectangles"></a><span data-ttu-id="2e080-129">Rectángulos de origen y de destino</span><span class="sxs-lookup"><span data-stu-id="2e080-129">Source and Destination Rectangles</span></span>

<span data-ttu-id="2e080-130">Durante la reproducción, el presentador toma una parte de la imagen de vídeo compuesta y la dibuja en un área de la ventana de vídeo.</span><span class="sxs-lookup"><span data-stu-id="2e080-130">During playback, the presenter takes a portion of the composited video image and draws it onto an area of the video window.</span></span> <span data-ttu-id="2e080-131">La parte de la imagen compuesta es el *rectángulo de origen* y el área de la ventana de vídeo es el *rectángulo de destino*.</span><span class="sxs-lookup"><span data-stu-id="2e080-131">The portion of the composited image is the *source rectangle*, and the area of the video window is the *destination rectangle*.</span></span>

<span data-ttu-id="2e080-132">El rectángulo de origen se define mediante coordenadas normalizadas en las que el punto (0,0, 0,0) corresponde a la esquina superior izquierda del vídeo y (1,0, 1,0) corresponde a la esquina inferior derecha del vídeo.</span><span class="sxs-lookup"><span data-stu-id="2e080-132">The source rectangle is defined using normalized coordinates where the point (0.0, 0.0) corresponds to the upper left corner of the video, and (1.0, 1.0) corresponds to the lower right corner of the video.</span></span> <span data-ttu-id="2e080-133">El rectángulo de origen puede ser cualquier región de este rectángulo.</span><span class="sxs-lookup"><span data-stu-id="2e080-133">The source rectangle can be any region within this rectangle.</span></span> <span data-ttu-id="2e080-134">El rectángulo de destino se especifica en píxeles, en relación con el área cliente de la ventana.</span><span class="sxs-lookup"><span data-stu-id="2e080-134">The destination rectangle is specified in pixels, relative to the client area of the window.</span></span> <span data-ttu-id="2e080-135">El rectángulo de origen predeterminado es la imagen completa y el rectángulo de destino predeterminado es un rectángulo vacío.</span><span class="sxs-lookup"><span data-stu-id="2e080-135">The default source rectangle is the entire image, and the default destination rectangle is an empty rectangle.</span></span>

<span data-ttu-id="2e080-136">Para establecer los rectángulos de origen y de destino, llame a [**IMFVideoDisplayControl:: SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition).</span><span class="sxs-lookup"><span data-stu-id="2e080-136">To set the source and destination rectangles, call [**IMFVideoDisplayControl::SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition).</span></span>

<span data-ttu-id="2e080-137">Si crea el receptor de medios de EVR a través de su objeto de activación, este paso no es necesario.</span><span class="sxs-lookup"><span data-stu-id="2e080-137">If you create the EVR media sink through its activation object, this step is not required.</span></span> <span data-ttu-id="2e080-138">El objeto de activación establece automáticamente el rectángulo de destino igual a todo el área cliente de la ventana.</span><span class="sxs-lookup"><span data-stu-id="2e080-138">The activation object automatically sets the destination rectangle equal to the entire client area of the window.</span></span> <span data-ttu-id="2e080-139">Sin embargo, debe llamar a [**SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) si desea cambiar el rectángulo de origen o establecer un rectángulo de destino diferente.</span><span class="sxs-lookup"><span data-stu-id="2e080-139">However, you should call [**SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) if you want to change the source rectangle or set a different destination rectangle.</span></span>

## <a name="window-messages"></a><span data-ttu-id="2e080-140">Mensajes de ventana</span><span class="sxs-lookup"><span data-stu-id="2e080-140">Window Messages</span></span>

<span data-ttu-id="2e080-141">Durante la reproducción, la aplicación debe responder a ciertos mensajes de ventana, como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="2e080-141">During playback, your application should respond to certain window messages, as follows:</span></span>

-   <span data-ttu-id="2e080-142">WM \_ Paint: llame a [**IMFVideoDisplayControl:: RepaintVideo**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo) para volver a dibujar el vídeo.</span><span class="sxs-lookup"><span data-stu-id="2e080-142">WM\_PAINT: Call [**IMFVideoDisplayControl::RepaintVideo**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo) to repaint the video.</span></span> <span data-ttu-id="2e080-143">Además, evite pintar el rectángulo de destino mientras se reproduce el vídeo, ya que esto puede provocar parpadeos.</span><span class="sxs-lookup"><span data-stu-id="2e080-143">Also, avoid painting over the destination rectangle while video is playing, because this can cause flickering.</span></span>

-   <span data-ttu-id="2e080-144">\_Tamaño de WM: puede que tenga que llamar a [**SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) para cambiar el tamaño del rectángulo de destino.</span><span class="sxs-lookup"><span data-stu-id="2e080-144">WM\_SIZE: You might need to call [**SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) to resize the destination rectangle.</span></span>

<span data-ttu-id="2e080-145">A diferencia del filtro del procesador de mezcla de vídeo (VMR) de DirectShow, no es necesario notificar a EVR cuando recibe un mensaje de DISPLAYCHANGE de WM \_ .</span><span class="sxs-lookup"><span data-stu-id="2e080-145">Unlike the Video Mixing Renderer (VMR) filter in DirectShow, you do not have to notify the EVR when you receive a WM\_DISPLAYCHANGE message.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2e080-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2e080-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2e080-147">Representador de vídeo mejorado</span><span class="sxs-lookup"><span data-stu-id="2e080-147">Enhanced Video Renderer</span></span>](enhanced-video-renderer.md)
</dt> </dl>

 

 



