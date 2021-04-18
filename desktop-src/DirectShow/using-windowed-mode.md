---
description: Usar el modo de ventana
ms.assetid: 09ee4568-348b-4cf9-bb38-dada291cdef9
title: Usar el modo de ventana
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95309f5546ce4f00a8dde029390b2edf48544f1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667847"
---
# <a name="using-windowed-mode"></a><span data-ttu-id="ddc02-103">Usar el modo de ventana</span><span class="sxs-lookup"><span data-stu-id="ddc02-103">Using Windowed Mode</span></span>

> [!Note]  
> <span data-ttu-id="ddc02-104">El [filtro de representador de vídeo](video-renderer-filter.md) heredado siempre usa el modo de ventana.</span><span class="sxs-lookup"><span data-stu-id="ddc02-104">The legacy [Video Renderer Filter](video-renderer-filter.md) always uses windowed mode.</span></span> <span data-ttu-id="ddc02-105">Los filtros VMR-7 y VMR-9 usan el modo de ventana de forma predeterminada, pero también admiten el modo sin ventanas.</span><span class="sxs-lookup"><span data-stu-id="ddc02-105">The VMR-7 and VMR-9 filters use windowed mode by default, but also support windowless mode.</span></span>

 

<span data-ttu-id="ddc02-106">En el modo de ventana, el representador de vídeo crea su propia ventana donde pinta los fotogramas de vídeo.</span><span class="sxs-lookup"><span data-stu-id="ddc02-106">In windowed mode, the video renderer creates its own window where it paints the video frames.</span></span> <span data-ttu-id="ddc02-107">A menos que especifique lo contrario, esta ventana es una ventana de nivel superior con sus propios bordes y barra de título.</span><span class="sxs-lookup"><span data-stu-id="ddc02-107">Unless you specify otherwise, this window is a top-level window with its own borders and title bar.</span></span> <span data-ttu-id="ddc02-108">Sin embargo, la mayoría de las veces se adjuntará la ventana de vídeo a una ventana de la aplicación, de modo que el vídeo se integre en la interfaz de usuario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ddc02-108">Most of the time, however, you will attach the video window to an application window, so that the video is integrated into your application UI.</span></span> <span data-ttu-id="ddc02-109">Para ello, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="ddc02-109">This requires the following steps:</span></span>

1.  <span data-ttu-id="ddc02-110">Consulta para **IVideoWindow**.</span><span class="sxs-lookup"><span data-stu-id="ddc02-110">Query for **IVideoWindow**.</span></span>
2.  <span data-ttu-id="ddc02-111">Establezca la ventana primaria.</span><span class="sxs-lookup"><span data-stu-id="ddc02-111">Set the parent window.</span></span>
3.  <span data-ttu-id="ddc02-112">Establecer nuevos estilos de ventana.</span><span class="sxs-lookup"><span data-stu-id="ddc02-112">Set new window styles.</span></span>
4.  <span data-ttu-id="ddc02-113">Coloque la ventana de vídeo dentro de la ventana propietaria.</span><span class="sxs-lookup"><span data-stu-id="ddc02-113">Position the video window inside the owner window.</span></span>
5.  <span data-ttu-id="ddc02-114">Notifique a la ventana de vídeo de \_ los mensajes de movimiento de WM.</span><span class="sxs-lookup"><span data-stu-id="ddc02-114">Notify the video window of WM\_MOVE messages.</span></span>

<span data-ttu-id="ddc02-115">**Consulta de IVideoWindow**</span><span class="sxs-lookup"><span data-stu-id="ddc02-115">**Query for IVideoWindow**</span></span>

<span data-ttu-id="ddc02-116">Antes de iniciar la reproducción, consulte el administrador de gráficos de filtro para la interfaz **IVideoWindow** :</span><span class="sxs-lookup"><span data-stu-id="ddc02-116">Before starting playback, query the Filter Graph Manager for the **IVideoWindow** interface:</span></span>


```C++
IVideoWindow *pVidWin = NULL;
pGraph->QueryInterface(IID_IVideoWindow, (void **)&pVidWin);
```



<span data-ttu-id="ddc02-117">**Establecer la ventana primaria**</span><span class="sxs-lookup"><span data-stu-id="ddc02-117">**Set the Parent Window**</span></span>

<span data-ttu-id="ddc02-118">Para establecer la ventana primaria, llame al método [**IVideoWindow::p UT \_ Owner**](/windows/desktop/api/Control/nf-control-ivideowindow-put_owner) con un identificador a la ventana de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ddc02-118">To set the parent window, call the [**IVideoWindow::put\_Owner**](/windows/desktop/api/Control/nf-control-ivideowindow-put_owner) method with a handle to your application window.</span></span> <span data-ttu-id="ddc02-119">Este método toma una variable de tipo [**OAHWND**](oahwnd.md), por lo que convierta el identificador a este tipo:</span><span class="sxs-lookup"><span data-stu-id="ddc02-119">This method takes a variable of type [**OAHWND**](oahwnd.md), so cast the handle to this type:</span></span>


```C++
pVidWin->put_Owner((OAHWND)hwnd);
```



<span data-ttu-id="ddc02-120">**Establecer nuevos estilos de ventana**</span><span class="sxs-lookup"><span data-stu-id="ddc02-120">**Set New Window Styles**</span></span>

<span data-ttu-id="ddc02-121">Cambie el estilo de la ventana de vídeo mediante una llamada al método [**IVideoWindow::p se ha UT \_ estiloVentana**](/windows/desktop/api/Control/nf-control-ivideowindow-put_windowstyle) :</span><span class="sxs-lookup"><span data-stu-id="ddc02-121">Change the style of the video window by calling the [**IVideoWindow::put\_WindowStyle**](/windows/desktop/api/Control/nf-control-ivideowindow-put_windowstyle) method:</span></span>


```C++
pVidWin->put_WindowStyle(WS_CHILD | WS_CLIPSIBLINGS);
```



<span data-ttu-id="ddc02-122">La \_ marca WS Child establece que la ventana sea una ventana secundaria y la marca WS \_ CLIPSIBLINGS impide que la ventana dibuje dentro del área cliente de otra ventana secundaria.</span><span class="sxs-lookup"><span data-stu-id="ddc02-122">The WS\_CHILD flag sets the window to be a child window, and the WS\_CLIPSIBLINGS flag prevents the window from drawing inside the client area of another child window.</span></span>

<span data-ttu-id="ddc02-123">**Colocar la ventana de vídeo**</span><span class="sxs-lookup"><span data-stu-id="ddc02-123">**Position the Video Window**</span></span>

<span data-ttu-id="ddc02-124">Para establecer la posición del vídeo en relación con el área de cliente de la ventana de la aplicación, llame al método [**IVideoWindow:: SetWindowPosition**](/windows/desktop/api/Control/nf-control-ivideowindow-setwindowposition) .</span><span class="sxs-lookup"><span data-stu-id="ddc02-124">To set the position of the video relative to the application window's client area, call the [**IVideoWindow::SetWindowPosition**](/windows/desktop/api/Control/nf-control-ivideowindow-setwindowposition) method.</span></span> <span data-ttu-id="ddc02-125">Este método toma un rectángulo que especifica el borde izquierdo, el borde superior, el ancho y el alto de la ventana de vídeo.</span><span class="sxs-lookup"><span data-stu-id="ddc02-125">This method takes a rectangle that specifies the left edge, top edge, width, and height of the video window.</span></span> <span data-ttu-id="ddc02-126">Por ejemplo, el código siguiente ajusta la ventana de vídeo para que se ajuste a todo el área cliente de la ventana primaria:</span><span class="sxs-lookup"><span data-stu-id="ddc02-126">For example, the following code stretches the video window to fit the entire client area of the parent window:</span></span>


```C++
RECT rc;
GetClientRect(hwnd, &rc);
pVidWin->SetWindowPosition(0, 0, rc.right, rc.bottom);
```



<span data-ttu-id="ddc02-127">Para obtener el tamaño nativo del vídeo, llame al método [**IBasicVideo:: GetVideoSize**](/windows/desktop/api/Control/nf-control-ibasicvideo-getvideosize) en el administrador de gráficos de filtro.</span><span class="sxs-lookup"><span data-stu-id="ddc02-127">To get the native size of the video, call the [**IBasicVideo::GetVideoSize**](/windows/desktop/api/Control/nf-control-ibasicvideo-getvideosize) method on the Filter Graph Manager.</span></span> <span data-ttu-id="ddc02-128">Puede usar esa información para escalar el vídeo y mantener la relación de aspecto correcta.</span><span class="sxs-lookup"><span data-stu-id="ddc02-128">You can use that information to scale the video and keep the correct aspect ratio.</span></span>

<span data-ttu-id="ddc02-129">**Respuesta a mensajes de movimiento de WM \_**</span><span class="sxs-lookup"><span data-stu-id="ddc02-129">**Respond to WM\_MOVE Messages**</span></span>

<span data-ttu-id="ddc02-130">Para obtener el mejor rendimiento, debe notificar al representador de vídeo cada vez que la ventana se mueva mientras el gráfico esté en pausa.</span><span class="sxs-lookup"><span data-stu-id="ddc02-130">For best performance, you should notify the video renderer whenever the window moves while the graph is paused.</span></span> <span data-ttu-id="ddc02-131">Llame al método [**IVideoWindow:: NotifyOwnerMessage**](/windows/desktop/api/Control/nf-control-ivideowindow-notifyownermessage) para reenviar el \_ mensaje de movimiento de WM:</span><span class="sxs-lookup"><span data-stu-id="ddc02-131">Call the [**IVideoWindow::NotifyOwnerMessage**](/windows/desktop/api/Control/nf-control-ivideowindow-notifyownermessage) method to forward the WM\_MOVE message:</span></span>


```C++
// (Inside your WindowProc)
case WM_MOVE:
    pVidWin->NotifyOwnerMessage((OAHWND)hWnd, msg, wParam, lParam);
    break;
```



<span data-ttu-id="ddc02-132">Si el representador usa una superposición de hardware, esta notificación hace que el representador actualice la posición de superposición.</span><span class="sxs-lookup"><span data-stu-id="ddc02-132">If the renderer is using a hardware overlay, this notification causes the renderer to update the overlay position.</span></span> <span data-ttu-id="ddc02-133">(VMR-9 no utiliza superposiciones, por lo que no es necesario llamar a este método si se usa VMR-9).</span><span class="sxs-lookup"><span data-stu-id="ddc02-133">(The VMR-9 does not use overlays, so you do not need to call this method if you are using the VMR-9.)</span></span>

<span data-ttu-id="ddc02-134">**Limpiar**</span><span class="sxs-lookup"><span data-stu-id="ddc02-134">**Clean Up**</span></span>

<span data-ttu-id="ddc02-135">Antes de que se cierre la aplicación, detenga el gráfico y restablezca el propietario de la ventana de vídeo en **null**.</span><span class="sxs-lookup"><span data-stu-id="ddc02-135">Before the application exits, stop the graph and reset the video window's owner to **NULL**.</span></span> <span data-ttu-id="ddc02-136">De lo contrario, es posible que los mensajes de ventana se envíen a una ventana incorrecta, lo que es probable que provoque errores.</span><span class="sxs-lookup"><span data-stu-id="ddc02-136">Otherwise, window messages might be sent to the wrong window, which is likely to cause errors.</span></span> <span data-ttu-id="ddc02-137">Además, oculte la ventana de vídeo o, de lo contrario, podría ver una imagen de vídeo parpadeando en la pantalla momentáneamente:</span><span class="sxs-lookup"><span data-stu-id="ddc02-137">Also, hide video window, or else you might see a video image flicker on the screen momentarily:</span></span>


```C++
pControl->Stop(); 
pVidWin->put_Visible(OAFALSE);
pVidWin->put_Owner(NULL);  
```



> [!Note]  
> <span data-ttu-id="ddc02-138">Si el elemento primario de la ventana de vídeo es un elemento secundario de la ventana principal de la aplicación (es decir, si la ventana de vídeo es un elemento secundario de un elemento secundario), debe crear la ventana de vídeo mediante **CoCreateInstance** y agregarla al gráfico, en lugar de permitir que el administrador de gráficos de filtros agregue el representador de vídeo durante la [conexión inteligente](intelligent-connect.md).</span><span class="sxs-lookup"><span data-stu-id="ddc02-138">If the parent of the video window is a child of your main application window (in other words, if the video window is a child of a child), you should create the video window using **CoCreateInstance** and add it to the graph, instead of letting the Filter Graph Manager add the video renderer during [Intelligent Connect](intelligent-connect.md).</span></span> <span data-ttu-id="ddc02-139">Esto garantiza que la ventana de vídeo y la ventana secundaria se repintan al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="ddc02-139">This ensures that the video window and your child window are repainted at the same time.</span></span> <span data-ttu-id="ddc02-140">De lo contrario, la ventana secundaria puede pintar sobre la ventana de vídeo.</span><span class="sxs-lookup"><span data-stu-id="ddc02-140">Otherwise, the child window may paint over the video window.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="ddc02-141">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ddc02-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ddc02-142">Representación de vídeo</span><span class="sxs-lookup"><span data-stu-id="ddc02-142">Video Rendering</span></span>](video-rendering.md)
</dt> </dl>

 

 



