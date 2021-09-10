---
title: 'Captura de vídeo: un enfoque mínimo'
description: 'Captura de vídeo: un enfoque mínimo'
ms.assetid: e39ff590-69c0-4927-90c2-786c6082068f
keywords:
- Vídeo para Windows (VFW), captura de vídeo
- VFW (vídeo para Windows),captura de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a65d5d5bbdc00dfd947c5d917e514d72e3ac069
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124372518"
---
# <a name="video-capture-a-minimal-approach"></a>Captura de vídeo: un enfoque mínimo

La captura de vídeo digitaliza una secuencia de datos de vídeo y audio y la almacena en un disco duro o en algún otro tipo de dispositivo de almacenamiento persistente. En esta sección se describe cómo agregar una forma sencilla de captura de vídeo a una aplicación mediante tres instrucciones de código. También se describe cómo finalizar o anular una sesión de captura mediante el envío de mensajes a la ventana de captura.

Una ventana de captura de AVICap controla los detalles de la captura de audio y vídeo de streaming en archivos AVI. Esto libera a la aplicación de la participación en el formato de archivo AVI, la administración de búferes de audio y vídeo, y el acceso de bajo nivel de los controladores de dispositivos de audio y vídeo. AVICap proporciona una interfaz flexible para las aplicaciones. Puede agregar la captura de vídeo a la aplicación con solo las siguientes líneas de código:


```C++
hWndC = capCreateCaptureWindow ( "My Own Capture Window", 
    WS_CHILD | WS_VISIBLE , 0, 0, 160, 120, hwndParent, nID);

SendMessage (hWndC, WM_CAP_DRIVER_CONNECT, 0 /* wIndex */, 0L);

SendMessage (hWndC, WM_CAP_SEQUENCE, 0, 0L);
 
```



También hay disponible una interfaz de macro que proporciona una alternativa al uso de la [función SendMessage](/windows/win32/api/winuser/nf-winuser-sendmessage) y mejora la legibilidad de una aplicación. En el ejemplo siguiente se usa la interfaz de macro para agregar la captura de vídeo a una aplicación.


```C++
hWndC = capCreateCaptureWindow (   "My Own Capture Window", 
    WS_CHILD | WS_VISIBLE ,   0, 0, 160, 120, hwndParent, nID);

capDriverConnect (hWndC, 0);

capCaptureSequence (hWndC); 
 
```



Una vez que la aplicación crea una ventana de captura de la clase de ventana AVICap y la conecta a un controlador de vídeo, la ventana de captura está lista para capturar datos. En este punto, la aplicación puede enviar simplemente el mensaje [**WM \_ CAP \_ SEQUENCE**](wm-cap-sequence.md) (o la macro [**capCaptureSequence)**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequence) para empezar a capturar.

Con la configuración predeterminada, WM CAP SEQUENCE inicia la captura de entrada de audio y \_ vídeo en un archivo denominado \_ CAPTURE.AVI. La captura continúa hasta que se produce uno de los siguientes eventos:

-   El usuario presiona la tecla ESC o un botón del mouse.
-   La aplicación detiene o anula la operación de captura.
-   El disco se llena.

En una aplicación, puede detener la transmisión de datos capturados a un archivo mediante el envío del mensaje [**WM \_ CAP \_ STOP**](wm-cap-stop.md) (o la macro [**capCaptureStop)**](/windows/desktop/api/Vfw/nf-vfw-capcapturestop) a una ventana de captura. También puede anular la operación de captura enviando el mensaje ABORT de [**WM \_ CAP \_**](wm-cap-abort.md) (o la macro [**capCaptureAbort)**](/windows/desktop/api/Vfw/nf-vfw-capcaptureabort) a una ventana de captura.

 

 