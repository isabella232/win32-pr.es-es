---
title: Captura de entradas de entrada
description: Captura de entradas de entrada
ms.assetid: 1214fe5a-5a6a-4c6c-9b77-94eeb73f60da
keywords:
- entradas de captura
- captura de entrada de entrada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b23fd3717ad09fd2e52f1a815f7d13b91963a13e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127272359"
---
# <a name="capturing-joystick-input"></a>Captura de entradas de entrada

La mayor parte del código que controla el eje está en la función de ventana principal. En la siguiente parte del controlador de mensajes, la aplicación llama [**a hastasetCapture**](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture) para capturar la entrada de la entrada DELID1.


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



 

 