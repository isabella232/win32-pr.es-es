---
description: El sistema no es el único origen de mensajes \_ WM PAINT. La función InvalidateRect o InvalidateRgn puede generar indirectamente mensajes WM \_ PAINT para las ventanas. Estas funciones marcan todo o parte de un área de cliente como no válida (que se debe volver a dibujar).
ms.assetid: 41c2bc07-768b-4d27-a869-69b072f3e033
title: Invalidación del área cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d94a3a5b4e6903c549331788f9e81947dca44e7a699bb1a633bce46525585b2d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119558665"
---
# <a name="invalidating-the-client-area"></a>Invalidación del área cliente

El sistema no es el único origen de [**mensajes \_ WM PAINT.**](wm-paint.md) La [**función InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) [**o InvalidateRgn**](/windows/desktop/api/Winuser/nf-winuser-invalidatergn) puede generar indirectamente mensajes **WM \_ PAINT** para las ventanas. Estas funciones marcan todo o parte de un área de cliente como no válida (que se debe volver a dibujar).

En el ejemplo siguiente, el procedimiento de ventana invalida todo el área de cliente al procesar [**mensajes WM \_ CHAR.**](../inputdev/wm-char.md) Esto permite al usuario cambiar la ilustración escribiendo un número y visualizando los resultados. Estos resultados se dibujan en cuanto no hay ningún otro mensaje en la cola de mensajes de la aplicación.


```C++
RECT rc;
POINT aptPentagon[6] = {50,2, 98,35, 79,90, 21,90, 2,35, 50,2}, 
      aptHexagon[7]  = {50,2, 93,25, 93,75, 50,98, 7,75, 7,25, 50,2}; 
POINT *ppt = aptPentagon; 
int cpt = 6; 
 
  . 
  . 
  . 
 
case WM_CHAR: 
    switch (wParam) 
    { 
        case '5': 
            ppt = aptPentagon; 
            cpt = 6; 
            break; 
        case '6': 
            ppt = aptHexagon; 
            cpt = 7; 
            break; 
    } 
    InvalidateRect(hwnd, NULL, TRUE); 
    return 0L; 
 
case WM_PAINT: 
    hdc = BeginPaint(hwnd, &ps); 
    GetClientRect(hwnd, &rc); 
    SetMapMode(hdc, MM_ANISOTROPIC); 
    SetWindowExtEx(hdc, 100, 100, NULL); 
    SetViewportExtEx(hdc, rc.right, rc.bottom, NULL); 
    Polyline(hdc, ppt, cpt); 
    EndPaint(hwnd, &ps); 
    return 0L; 
```



En este ejemplo, el **argumento NULL** utilizado [**por InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) especifica todo el área de cliente; El **argumento TRUE** hace que se borre el fondo. Si no desea que la aplicación espere hasta que la cola de mensajes de la aplicación no tenga ningún otro mensaje, use la función [**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow) para forzar el envío inmediato del mensaje [**WM \_ PAINT.**](wm-paint.md) Si hay alguna parte no válida del área de cliente, **UpdateWindow** envía el mensaje **WM \_ PAINT** de la ventana especificada directamente al procedimiento de ventana.

 

 
