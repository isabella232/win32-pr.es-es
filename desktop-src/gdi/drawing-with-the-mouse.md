---
description: Puede permitir que el usuario dibuje líneas con el mouse haciendo que el procedimiento de ventana dibuje mientras procesa el mensaje de Windows de WM \_ .
ms.assetid: 5e8a54b6-05cc-4446-b82e-2b3e550d780a
title: Dibujar con el mouse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0ad38e7ef8af5c39918bac7231aea4dde285caa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082364"
---
# <a name="drawing-with-the-mouse"></a>Dibujar con el mouse

Puede permitir que el usuario dibuje líneas con el mouse haciendo que el procedimiento de ventana dibuje mientras procesa el mensaje de Windows de [**WM \_**](../inputdev/wm-mousemove.md) . El sistema envía el mensaje del **\_ MOUSEMOVE de WM** al procedimiento de ventana siempre que el usuario mueve el cursor dentro de la ventana. Para dibujar líneas, el procedimiento de ventana puede recuperar un contexto de dispositivo de pantalla y dibujar una línea en la ventana entre las posiciones del cursor actual y anterior.

En el ejemplo siguiente, el procedimiento de ventana se prepara para dibujar cuando el usuario presiona y mantiene presionado el botón primario del mouse (enviando el mensaje de [**\_ LBUTTONDOWN de WM**](../inputdev/wm-lbuttondown.md) ). Cuando el usuario mueve el cursor dentro de la ventana, el procedimiento de ventana recibe una serie de mensajes del [**\_ MOUSEMOVE de WM**](../inputdev/wm-mousemove.md) . Para cada mensaje, el procedimiento de ventana dibuja una línea que conecta la posición anterior y la posición actual. Para dibujar la línea, el procedimiento usa [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) para recuperar un contexto de dispositivo de pantalla. después, en cuanto se complete el dibujo y antes de que se devuelva el mensaje, el procedimiento usa la función [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) para liberar el contexto de dispositivo de pantalla. En cuanto el usuario suelta el botón del mouse, el procedimiento de ventana borra la marca y el dibujo se detiene (que envía el mensaje de [**\_ LBUTTONUP de WM**](../inputdev/wm-lbuttonup.md) ).


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



Una aplicación que permite dibujar, como en este ejemplo, normalmente registra los puntos o las líneas para que se puedan volver a dibujar las líneas cada vez que se actualice la ventana. Las aplicaciones de dibujo suelen utilizar un contexto de dispositivo de memoria y un mapa de bits asociado para almacenar líneas dibujadas con un mouse.

 

 
