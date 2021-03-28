---
description: Puede dibujar su propio fondo de la ventana en lugar de hacer que el sistema lo dibuje automáticamente.
ms.assetid: 72a342dc-2766-4ec9-b4c6-5ac3c550ea25
title: Dibujo de un fondo de ventana personalizado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 437a88bec680a6f35e84f5444fc90a45f98da533
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984986"
---
# <a name="drawing-a-custom-window-background"></a>Dibujo de un fondo de ventana personalizado

Puede dibujar su propio fondo de la ventana en lugar de hacer que el sistema lo dibuje automáticamente. La mayoría de las aplicaciones especifican un identificador de pincel o un valor de color del sistema para el pincel de fondo de clase al registrar la clase de ventana. el sistema utiliza el pincel o el color para dibujar el fondo. Sin embargo, si establece el pincel de fondo de clase en **null**, el sistema envía un mensaje de [**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md) al procedimiento de ventana cada vez que se debe dibujar el fondo de la ventana, lo que le permite dibujar un fondo personalizado.

En el ejemplo siguiente, el procedimiento de ventana dibuja un patrón de tablero de ajedrez grande que se adapta perfectamente a la ventana. El procedimiento rellena el área cliente con un pincel blanco y, a continuación, dibuja los rectángulos 13 20 por 20 con un pincel gris. El contexto de dispositivo de pantalla que se va a usar al dibujar el fondo se especifica en el parámetro *wParam* del mensaje.


```C++
HBRUSH hbrWhite, hbrGray; 
 
  . 
  . 
  . 
 
case WM_CREATE: 
    hbrWhite = GetStockObject(WHITE_BRUSH); 
    hbrGray  = GetStockObject(GRAY_BRUSH); 
    return 0L; 
 
case WM_ERASEBKGND: 
    hdc = (HDC) wParam; 
    GetClientRect(hwnd, &rc); 
    SetMapMode(hdc, MM_ANISOTROPIC); 
    SetWindowExtEx(hdc, 100, 100, NULL); 
    SetViewportExtEx(hdc, rc.right, rc.bottom, NULL); 
    FillRect(hdc, &rc, hbrWhite); 
 
    for (i = 0; i < 13; i++) 
    { 
        x = (i * 40) % 100; 
        y = ((i * 40) / 100) * 20; 
        SetRect(&rc, x, y, x + 20, y + 20); 
        FillRect(hdc, &rc, hbrGray); 
    } 
  return 1L; 
```



Si la aplicación dibuja su propia ventana minimizada, el sistema también envía el mensaje de [**\_ ERASEBKGND de WM**](../winmsg/wm-erasebkgnd.md) al procedimiento de ventana para dibujar el fondo de la ventana minimizada. Puede usar la misma técnica usada por [**WM \_ Paint**](wm-paint.md) para determinar si la ventana está minimizada es decir, llamar a la función [**IsIconic**](/windows/win32/api/winuser/nf-winuser-isiconic) y comprobar el valor devuelto **true**.

 

 
