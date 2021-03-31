---
title: Captura de vídeo de un enfoque mínimo
description: Captura de vídeo de un enfoque mínimo
ms.assetid: e39ff590-69c0-4927-90c2-786c6082068f
keywords:
- Vídeo para Windows (VFW), captura de vídeo
- VFW (vídeo para Windows), captura de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a65d5d5bbdc00dfd947c5d917e514d72e3ac069
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103904544"
---
# <a name="video-capture-a-minimal-approach"></a><span data-ttu-id="4caab-105">Captura de vídeo: un enfoque mínimo</span><span class="sxs-lookup"><span data-stu-id="4caab-105">Video Capture: A Minimal Approach</span></span>

<span data-ttu-id="4caab-106">La captura de vídeo digitaliza un flujo de datos de vídeo y audio, y lo almacena en un disco duro o en algún otro tipo de dispositivo de almacenamiento persistente.</span><span class="sxs-lookup"><span data-stu-id="4caab-106">Video capture digitizes a stream of video and audio data, and stores it on a hard disk or some other type of persistent storage device.</span></span> <span data-ttu-id="4caab-107">En esta sección se describe cómo agregar una sencilla forma de captura de vídeo a una aplicación mediante tres instrucciones de código.</span><span class="sxs-lookup"><span data-stu-id="4caab-107">This section describes how to add a simple form of video capture to an application using three statements of code.</span></span> <span data-ttu-id="4caab-108">También se describe cómo finalizar o anular una sesión de captura mediante el envío de mensajes a la ventana de captura.</span><span class="sxs-lookup"><span data-stu-id="4caab-108">It also describes how to end or abort a capture session by sending messages to the capture window.</span></span>

<span data-ttu-id="4caab-109">Una ventana de captura de AVICap controla los detalles de la captura de audio y vídeo de transmisión por secuencias de archivos AVI.</span><span class="sxs-lookup"><span data-stu-id="4caab-109">An AVICap capture window handles the details of streaming audio and video capture to AVI files.</span></span> <span data-ttu-id="4caab-110">Esto libera a la aplicación de la implicación en el formato de archivo AVI, la administración de búfer de vídeo y audio, y el acceso de bajo nivel de los controladores de dispositivos de audio y vídeo.</span><span class="sxs-lookup"><span data-stu-id="4caab-110">This frees your application from involvement in the AVI file format, video and audio buffer management, and the low-level access of video and audio device drivers.</span></span> <span data-ttu-id="4caab-111">AVICap proporciona una interfaz flexible para las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="4caab-111">AVICap provides a flexible interface for applications.</span></span> <span data-ttu-id="4caab-112">Puede Agregar captura de vídeo a la aplicación con solo las siguientes líneas de código:</span><span class="sxs-lookup"><span data-stu-id="4caab-112">You can add video capture to your application, using only the following lines of code:</span></span>


```C++
hWndC = capCreateCaptureWindow ( "My Own Capture Window", 
    WS_CHILD | WS_VISIBLE , 0, 0, 160, 120, hwndParent, nID);

SendMessage (hWndC, WM_CAP_DRIVER_CONNECT, 0 /* wIndex */, 0L);

SendMessage (hWndC, WM_CAP_SEQUENCE, 0, 0L);
 
```



<span data-ttu-id="4caab-113">También hay disponible una interfaz de macros que proporciona una alternativa al uso de la función [SendMessage](/windows/win32/api/winuser/nf-winuser-sendmessage) y mejora la legibilidad de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="4caab-113">A macro interface is also available that provides an alternative to using the [SendMessage](/windows/win32/api/winuser/nf-winuser-sendmessage) function and improves the readability of an application.</span></span> <span data-ttu-id="4caab-114">En el ejemplo siguiente se usa la interfaz de macros para agregar captura de vídeo a una aplicación.</span><span class="sxs-lookup"><span data-stu-id="4caab-114">The following example uses the macro interface to add video capture to an application.</span></span>


```C++
hWndC = capCreateCaptureWindow (   "My Own Capture Window", 
    WS_CHILD | WS_VISIBLE ,   0, 0, 160, 120, hwndParent, nID);

capDriverConnect (hWndC, 0);

capCaptureSequence (hWndC); 
 
```



<span data-ttu-id="4caab-115">Una vez que la aplicación crea una ventana de captura de la clase de ventana AVICap y la conecta a un controlador de vídeo, la ventana de captura está lista para capturar los datos.</span><span class="sxs-lookup"><span data-stu-id="4caab-115">After your application creates a capture window of the AVICap window class and connects it to a video driver, the capture window is ready to capture data.</span></span> <span data-ttu-id="4caab-116">En este punto, la aplicación simplemente puede enviar el mensaje de [**\_ \_ secuencia de Cap de WM**](wm-cap-sequence.md) (o la macro [**capCaptureSequence**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequence) ) para comenzar la captura.</span><span class="sxs-lookup"><span data-stu-id="4caab-116">At this point, your application can simply send the [**WM\_CAP\_SEQUENCE**](wm-cap-sequence.md) message (or the [**capCaptureSequence**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequence) macro) to begin capturing.</span></span>

<span data-ttu-id="4caab-117">Con la configuración predeterminada, \_ \_ la secuencia de Cap de WM inicia la captura de vídeo y entrada de audio en un archivo denominado CAPTURE.AVI.</span><span class="sxs-lookup"><span data-stu-id="4caab-117">Using default settings, WM\_CAP\_SEQUENCE initiates the capture of video and audio input to a file named CAPTURE.AVI.</span></span> <span data-ttu-id="4caab-118">La captura continúa hasta que se produce uno de los siguientes eventos:</span><span class="sxs-lookup"><span data-stu-id="4caab-118">Capture continues until one of the following events occurs:</span></span>

-   <span data-ttu-id="4caab-119">El usuario presiona la tecla ESC o un botón del mouse.</span><span class="sxs-lookup"><span data-stu-id="4caab-119">The user presses the ESC key or a mouse button.</span></span>
-   <span data-ttu-id="4caab-120">La aplicación detiene o anula la operación de captura.</span><span class="sxs-lookup"><span data-stu-id="4caab-120">Your application stops or aborts capture operation.</span></span>
-   <span data-ttu-id="4caab-121">El disco se llena.</span><span class="sxs-lookup"><span data-stu-id="4caab-121">The disk becomes full.</span></span>

<span data-ttu-id="4caab-122">En una aplicación, puede detener la transmisión por secuencias de datos capturados a un archivo enviando el mensaje de [**\_ \_ detención de Cap de WM**](wm-cap-stop.md) (o la macro [**capCaptureStop**](/windows/desktop/api/Vfw/nf-vfw-capcapturestop) ) a una ventana de captura.</span><span class="sxs-lookup"><span data-stu-id="4caab-122">In an application, you can stop streaming captured data to a file by sending the [**WM\_CAP\_STOP**](wm-cap-stop.md) (or the [**capCaptureStop**](/windows/desktop/api/Vfw/nf-vfw-capcapturestop) macro) message to a capture window.</span></span> <span data-ttu-id="4caab-123">También puede anular la operación de captura enviando el mensaje de [**\_ \_ anulación de Cap de WM**](wm-cap-abort.md) (o la macro [**capCaptureAbort**](/windows/desktop/api/Vfw/nf-vfw-capcaptureabort) ) a una ventana de captura.</span><span class="sxs-lookup"><span data-stu-id="4caab-123">You can also abort the capture operation by sending the [**WM\_CAP\_ABORT**](wm-cap-abort.md) message (or the [**capCaptureAbort**](/windows/desktop/api/Vfw/nf-vfw-capcaptureabort) macro) to a capture window.</span></span>

 

 