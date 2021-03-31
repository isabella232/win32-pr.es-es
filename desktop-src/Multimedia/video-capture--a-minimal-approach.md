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
# <a name="video-capture-a-minimal-approach"></a>Captura de vídeo: un enfoque mínimo

La captura de vídeo digitaliza un flujo de datos de vídeo y audio, y lo almacena en un disco duro o en algún otro tipo de dispositivo de almacenamiento persistente. En esta sección se describe cómo agregar una sencilla forma de captura de vídeo a una aplicación mediante tres instrucciones de código. También se describe cómo finalizar o anular una sesión de captura mediante el envío de mensajes a la ventana de captura.

Una ventana de captura de AVICap controla los detalles de la captura de audio y vídeo de transmisión por secuencias de archivos AVI. Esto libera a la aplicación de la implicación en el formato de archivo AVI, la administración de búfer de vídeo y audio, y el acceso de bajo nivel de los controladores de dispositivos de audio y vídeo. AVICap proporciona una interfaz flexible para las aplicaciones. Puede Agregar captura de vídeo a la aplicación con solo las siguientes líneas de código:


```C++
hWndC = capCreateCaptureWindow ( "My Own Capture Window", 
    WS_CHILD | WS_VISIBLE , 0, 0, 160, 120, hwndParent, nID);

SendMessage (hWndC, WM_CAP_DRIVER_CONNECT, 0 /* wIndex */, 0L);

SendMessage (hWndC, WM_CAP_SEQUENCE, 0, 0L);
 
```



También hay disponible una interfaz de macros que proporciona una alternativa al uso de la función [SendMessage](/windows/win32/api/winuser/nf-winuser-sendmessage) y mejora la legibilidad de una aplicación. En el ejemplo siguiente se usa la interfaz de macros para agregar captura de vídeo a una aplicación.


```C++
hWndC = capCreateCaptureWindow (   "My Own Capture Window", 
    WS_CHILD | WS_VISIBLE ,   0, 0, 160, 120, hwndParent, nID);

capDriverConnect (hWndC, 0);

capCaptureSequence (hWndC); 
 
```



Una vez que la aplicación crea una ventana de captura de la clase de ventana AVICap y la conecta a un controlador de vídeo, la ventana de captura está lista para capturar los datos. En este punto, la aplicación simplemente puede enviar el mensaje de [**\_ \_ secuencia de Cap de WM**](wm-cap-sequence.md) (o la macro [**capCaptureSequence**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequence) ) para comenzar la captura.

Con la configuración predeterminada, \_ \_ la secuencia de Cap de WM inicia la captura de vídeo y entrada de audio en un archivo denominado CAPTURE.AVI. La captura continúa hasta que se produce uno de los siguientes eventos:

-   El usuario presiona la tecla ESC o un botón del mouse.
-   La aplicación detiene o anula la operación de captura.
-   El disco se llena.

En una aplicación, puede detener la transmisión por secuencias de datos capturados a un archivo enviando el mensaje de [**\_ \_ detención de Cap de WM**](wm-cap-stop.md) (o la macro [**capCaptureStop**](/windows/desktop/api/Vfw/nf-vfw-capcapturestop) ) a una ventana de captura. También puede anular la operación de captura enviando el mensaje de [**\_ \_ anulación de Cap de WM**](wm-cap-abort.md) (o la macro [**capCaptureAbort**](/windows/desktop/api/Vfw/nf-vfw-capcaptureabort) ) a una ventana de captura.

 

 