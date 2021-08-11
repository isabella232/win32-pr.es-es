---
description: Puede permitir que el usuario dibuje líneas con el mouse haciendo que el procedimiento de ventana se dibuje al procesar el mensaje \_ WM MOUSEMOVE.
ms.assetid: 5e8a54b6-05cc-4446-b82e-2b3e550d780a
title: Dibujar con el mouse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6de7c75c768dcdd330e04a0877bacf59b63d59a6eeb9707011faff6a6b15055c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118250407"
---
# <a name="drawing-with-the-mouse"></a>Dibujar con el mouse

Puede permitir que el usuario dibuje líneas con el mouse haciendo que el procedimiento de ventana se dibuje al procesar el [**mensaje \_ WM MOUSEMOVE.**](../inputdev/wm-mousemove.md) El sistema envía el **mensaje \_ WM MOUSEMOVE** al procedimiento de ventana cada vez que el usuario mueve el cursor dentro de la ventana. Para dibujar líneas, el procedimiento de ventana puede recuperar un contexto de dispositivo para mostrar y dibujar una línea en la ventana entre las posiciones del cursor actual y anterior.

En el ejemplo siguiente, el procedimiento de ventana se prepara para dibujar cuando el usuario presiona y mantiene presionado el botón izquierdo del mouse (enviando el [**mensaje \_ WM LBUTTONDOWN).**](../inputdev/wm-lbuttondown.md) A medida que el usuario mueve el cursor dentro de la ventana, el procedimiento de ventana recibe una serie de [**mensajes \_ MOUSEMOVE de WM.**](../inputdev/wm-mousemove.md) Para cada mensaje, el procedimiento de ventana dibuja una línea que conecta la posición anterior y la posición actual. Para dibujar la línea, el procedimiento usa [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) para recuperar un contexto de dispositivo de visualización; A continuación, en cuanto se completa el dibujo y antes de volver del mensaje, el procedimiento usa la [**función ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) para liberar el contexto del dispositivo de presentación. En cuanto el usuario suelta el botón del mouse, el procedimiento de ventana borra la marca y el dibujo se detiene (lo que envía el [**mensaje \_ LBUTTONUP de WM).**](../inputdev/wm-lbuttonup.md)


```C++
BOOL fDraw = FALSE; 
POINT ptPrevious; 
 
  . 
  . 
  . 
 
case WM_LBUTTONDOWN: 
    fDraw = TRUE; 
    ptPrevious.x = LOWORD(lParam); 
    ptPrevious.y = HIWORD(lParam); 
    return 0L; 
 
case WM_LBUTTONUP: 
    if (fDraw) 
    { 
        hdc = GetDC(hwnd); 
        MoveToEx(hdc, ptPrevious.x, ptPrevious.y, NULL); 
        LineTo(hdc, LOWORD(lParam), HIWORD(lParam)); 
        ReleaseDC(hwnd, hdc); 
    } 
    fDraw = FALSE; 
    return 0L; 
 
case WM_MOUSEMOVE: 
    if (fDraw) 
    { 
        hdc = GetDC(hwnd); 
        MoveToEx(hdc, ptPrevious.x, ptPrevious.y, NULL); 
        LineTo(hdc, ptPrevious.x = LOWORD(lParam), 
          ptPrevious.y = HIWORD(lParam)); 
        ReleaseDC(hwnd, hdc); 
    } 
    return 0L; 
```



Una aplicación que permite dibujar, como en este ejemplo, normalmente registra los puntos o líneas para que las líneas se puedan volver a dibujar cada vez que se actualice la ventana. Las aplicaciones de dibujo suelen usar un contexto de dispositivo de memoria y un mapa de bits asociado para almacenar líneas dibujadas con un mouse.

 

 
