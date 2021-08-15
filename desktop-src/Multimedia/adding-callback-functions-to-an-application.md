---
title: Agregar funciones de devolución de llamada a una aplicación
description: Agregar funciones de devolución de llamada a una aplicación
ms.assetid: b7bde1be-b229-4e00-8906-22d7dcf9ea04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dcd72b1a95a416398f482b90d7cd15cd80e1698a66a4b1c482bc92fc523ab2f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118941833"
---
# <a name="adding-callback-functions-to-an-application"></a>Agregar funciones de devolución de llamada a una aplicación

Una aplicación puede registrar funciones de devolución de llamada con la ventana de captura para notificar a la aplicación en las siguientes circunstancias:

-   El estado cambia
-   Se producen errores
-   Los búferes de audio y fotogramas de vídeo están disponibles
-   La aplicación debe producir durante la captura de streaming

En el ejemplo siguiente se crea una ventana de captura y se registran las funciones de estado, error, secuencia de vídeo y devolución de llamada de fotogramas en el bucle de procesamiento de mensajes de una aplicación. También incluye una instrucción de ejemplo para deshabilitar una función de devolución de llamada. Los ejemplos posteriores muestran funciones simples de estado, error y devolución de llamada de marco.


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de captura de vídeo](using-video-capture.md)
</dt> </dl>

 

 




