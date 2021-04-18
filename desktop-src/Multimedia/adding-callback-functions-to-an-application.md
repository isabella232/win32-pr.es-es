---
title: Agregar funciones de devolución de llamada a una aplicación
description: Agregar funciones de devolución de llamada a una aplicación
ms.assetid: b7bde1be-b229-4e00-8906-22d7dcf9ea04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d4f5f3dc43227f92305032decaf917bf521d95b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532176"
---
# <a name="adding-callback-functions-to-an-application"></a><span data-ttu-id="c6851-103">Agregar funciones de devolución de llamada a una aplicación</span><span class="sxs-lookup"><span data-stu-id="c6851-103">Adding Callback Functions to an Application</span></span>

<span data-ttu-id="c6851-104">Una aplicación puede registrar funciones de devolución de llamada con la ventana de captura para notificar a la aplicación en las siguientes circunstancias:</span><span class="sxs-lookup"><span data-stu-id="c6851-104">An application can register callback functions with the capture window so that it notifies the application in the following circumstances:</span></span>

-   <span data-ttu-id="c6851-105">El estado cambia</span><span class="sxs-lookup"><span data-stu-id="c6851-105">The status changes</span></span>
-   <span data-ttu-id="c6851-106">Se producen errores</span><span class="sxs-lookup"><span data-stu-id="c6851-106">Errors occur</span></span>
-   <span data-ttu-id="c6851-107">Los búferes de audio y fotogramas de vídeo están disponibles</span><span class="sxs-lookup"><span data-stu-id="c6851-107">Video frame and audio buffers become available</span></span>
-   <span data-ttu-id="c6851-108">La aplicación debe producir durante la captura de streaming</span><span class="sxs-lookup"><span data-stu-id="c6851-108">The application should yield during streaming capture</span></span>

<span data-ttu-id="c6851-109">En el ejemplo siguiente se crea una ventana de captura y se registran las funciones de devolución de llamada de estado, de error, de secuencia de vídeo y de intervalo en el bucle de procesamiento de mensajes de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="c6851-109">The following example creates a capture window and registers status, error, video stream, and frame callback functions in the message-processing loop of an application.</span></span> <span data-ttu-id="c6851-110">También incluye una instrucción de ejemplo para deshabilitar una función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="c6851-110">It also includes a sample statement for disabling a callback function.</span></span> <span data-ttu-id="c6851-111">En los ejemplos siguientes se muestran las funciones de estado simple, error y devolución de llamada de fotograma.</span><span class="sxs-lookup"><span data-stu-id="c6851-111">Subsequent examples show simple status, error, and frame callback functions.</span></span>


```C++
case WM_CREATE: 
{ 
    char    achDeviceName[80] ; 
    char    achDeviceVersion[100] ; 
    char    achBuffer[100] ; 
    WORD    wDriverCount = 0 ; 
    WORD    wIndex ; 
    WORD    wError ; 
    HMENU   hMenu ; 
 
    // Create a capture window using the capCreateCaptureWindow macro.
    ghWndCap = capCreateCaptureWindow((LPSTR)"Capture Window", 
        WS_CHILD | WS_VISIBLE, 0, 0, 160, 120, (HWND) hWnd, (int) 0); 
 
    // Register the error callback function using the 
    // capSetCallbackOnError macro. 
    capSetCallbackOnError(ghWndCap, fpErrorCallback); 
 
    // Register the status callback function using the 
    // capSetCallbackOnStatus macro. 
    capSetCallbackOnStatus(ghWndCap, fpStatusCallback); 
 
    // Register the video-stream callback function using the
    // capSetCallbackOnVideoStream macro. 
    capSetCallbackOnVideoStream(ghWndCap, fpVideoCallback); 
 
    // Register the frame callback function using the
    // capSetCallbackOnFrame macro. 
    capSetCallbackOnFrame(ghWndCap, fpFrameCallback); 
 
    // Connect to a capture driver 

    break; 
} 
case WM_CLOSE: 
{ 
// Use the capSetCallbackOnFrame macro to 
// disable the frame callback. Similar calls exist for the other 
// callback functions.

    capSetCallbackOnFrame(ghWndCap, NULL); 

    break; 
} 
 
```



## <a name="related-topics"></a><span data-ttu-id="c6851-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c6851-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c6851-113">Uso de la captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="c6851-113">Using Video Capture</span></span>](using-video-capture.md)
</dt> </dl>

 

 




