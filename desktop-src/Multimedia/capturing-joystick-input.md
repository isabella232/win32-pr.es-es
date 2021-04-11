---
title: Captura de entradas de joystick
description: Captura de entradas de joystick
ms.assetid: 1214fe5a-5a6a-4c6c-9b77-94eeb73f60da
keywords:
- joysticks, capturar entradas
- captura de entradas de joystick
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b23fd3717ad09fd2e52f1a815f7d13b91963a13e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104149259"
---
# <a name="capturing-joystick-input"></a>Captura de entradas de joystick

La mayor parte del código que controla el joystick está en la función de ventana principal. En la siguiente parte del controlador de mensajes, la aplicación llama a [**joySetCapture**](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture) para capturar la entrada desde el joystick JOYSTICKID1.


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



 

 