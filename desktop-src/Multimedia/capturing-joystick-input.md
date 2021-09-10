---
title: Captura de entrada de entradas de entrada
description: Captura de entrada de entradas de entrada
ms.assetid: 1214fe5a-5a6a-4c6c-9b77-94eeb73f60da
keywords:
- entradas de captura
- captura de entrada de input
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b23fd3717ad09fd2e52f1a815f7d13b91963a13e
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371161"
---
# <a name="capturing-joystick-input"></a>Captura de entrada de entradas de entrada

La mayor parte del código que controla el eje está en la función de ventana principal. En la siguiente parte del controlador de mensajes, la aplicación llama [**alegSetCapture para**](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture) capturar la entrada desde el valor DEONID1.


```C++
case WM_CREATE: 
    if(joySetCapture(hWnd, JOYSTICKID1, NULL, FALSE)) 
    { 
        MessageBeep(MB_ICONEXCLAMATION); 
        MessageBox(hWnd, "Couldn't capture the joystick.", NULL, 
            MB_OK | MB_ICONEXCLAMATION); 
        PostMessage(hWnd,WM_CLOSE,0,0L); 
    } 
    break; 
 
```



 

 