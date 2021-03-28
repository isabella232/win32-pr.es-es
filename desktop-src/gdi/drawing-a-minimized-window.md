---
description: Puede dibujar sus propias ventanas minimizadas en lugar de que el sistema las dibuje automáticamente.
ms.assetid: 607d987a-5bdc-46bc-bde7-6dc52745ac79
title: Dibujar una ventana minimizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ced1f3205243ea098856517590d58caee851329a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423828"
---
# <a name="drawing-a-minimized-window"></a>Dibujar una ventana minimizada

Puede dibujar sus propias ventanas minimizadas en lugar de que el sistema las dibuje automáticamente. La mayoría de las aplicaciones definen un icono de clase al registrar la clase de ventana para la ventana y el sistema dibuja el icono cuando la ventana está minimizada. Sin embargo, si establece el icono de clase en **null**, el sistema envía un mensaje de [**\_ dibujo de WM**](wm-paint.md) al procedimiento de ventana cada vez que se minimiza la ventana, lo que permite que el procedimiento de ventana dibuje en la ventana minimizada.

En el ejemplo siguiente, el procedimiento de ventana dibuja una estrella en la ventana minimizada. El procedimiento usa la función [**IsIconic**](/windows/win32/api/winuser/nf-winuser-isiconic) para determinar cuándo se minimiza la ventana. Esto garantiza que la estrella solo se dibuja cuando la ventana está minimizada.


```C++
POINT aptStar[6] = {50,2, 2,98, 98,33, 2,33, 98,98, 50,2}; 
 
  . 
  . 
  . 
 
case WM_PAINT: 
    hdc = BeginPaint(hwnd, &ps); 
 
    // Determine whether the window is minimized.  
 
    if (IsIconic(hwnd)) 
    { 
        GetClientRect(hwnd, &rc); 
        SetMapMode(hdc, MM_ANISOTROPIC); 
        SetWindowExtEx(hdc, 100, 100, NULL); 
        SetViewportExtEx(hdc, rc.right, rc.bottom, NULL); 
        Polyline(hdc, aptStar, 6); 
    } 
    else 
    { 
        TextOut(hdc, 0,0, "Hello, Windows!", 15); 
    } 
    EndPaint(hwnd, &ps); 
    return 0L; 
```



Establezca el icono de clase en **null** estableciendo el miembro **hIcon** de la estructura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) en **null** antes de llamar a la función [**RegisterClass**](/windows/win32/api/winuser/nf-winuser-registerclassa) para la clase de ventana.

 

 
