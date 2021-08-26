---
description: Puede dibujar su propio fondo de ventana en lugar de hacer que el sistema lo dibuje por usted.
ms.assetid: 72a342dc-2766-4ec9-b4c6-5ac3c550ea25
title: Dibujar un fondo de ventana personalizado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4248f7d7a1ae27ae09c93e95734fd72285028e1185b6d35110e5141fcbf88c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966015"
---
# <a name="drawing-a-custom-window-background"></a>Dibujar un fondo de ventana personalizado

Puede dibujar su propio fondo de ventana en lugar de hacer que el sistema lo dibuje por usted. La mayoría de las aplicaciones especifican un identificador de pincel o un valor de color del sistema para el pincel de fondo de clase al registrar la clase de ventana; el sistema usa el pincel o el color para dibujar el fondo. Sin embargo, si establece el pincel de fondo de clase en **NULL,** el sistema envía un mensaje [**WM \_ ERASEB DOMAINND**](../winmsg/wm-erasebkgnd.md) al procedimiento de ventana cada vez que se debe dibujar el fondo de la ventana, lo que le permite dibujar un fondo personalizado.

En el ejemplo siguiente, el procedimiento de ventana dibuja un patrón de tablero de comprobación grande que se ajusta perfectamente en la ventana. El procedimiento rellena el área cliente con un pincel blanco y, a continuación, dibuja decimotercer rectángulos de 20 por 20 con un pincel gris. El contexto del dispositivo para mostrar que se va a usar al dibujar el fondo se especifica en el *parámetro wParam* del mensaje.


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



Si la aplicación dibuja su propia ventana minimizada, el sistema también envía el mensaje [**\_ WM ERASEB DOMAINND**](../winmsg/wm-erasebkgnd.md) al procedimiento de ventana para dibujar el fondo de la ventana minimizada. Puede usar la misma técnica que [**usa WM \_ PAINT**](wm-paint.md) para determinar si la ventana está minimizada, es decir, llamar a la función [**IsIconic**](/windows/win32/api/winuser/nf-winuser-isiconic) y comprobar el valor devuelto **TRUE.**

 

 
