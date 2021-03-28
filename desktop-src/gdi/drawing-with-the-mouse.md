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
# <a name="drawing-with-the-mouse"></a><span data-ttu-id="ee5d0-103">Dibujar con el mouse</span><span class="sxs-lookup"><span data-stu-id="ee5d0-103">Drawing with the Mouse</span></span>

<span data-ttu-id="ee5d0-104">Puede permitir que el usuario dibuje líneas con el mouse haciendo que el procedimiento de ventana dibuje mientras procesa el mensaje de Windows de [**WM \_**](../inputdev/wm-mousemove.md) .</span><span class="sxs-lookup"><span data-stu-id="ee5d0-104">You can permit the user to draw lines with the mouse by having your window procedure draw while processing the [**WM\_MOUSEMOVE**](../inputdev/wm-mousemove.md) message.</span></span> <span data-ttu-id="ee5d0-105">El sistema envía el mensaje del **\_ MOUSEMOVE de WM** al procedimiento de ventana siempre que el usuario mueve el cursor dentro de la ventana.</span><span class="sxs-lookup"><span data-stu-id="ee5d0-105">The system sends the **WM\_MOUSEMOVE** message to the window procedure whenever the user moves the cursor within the window.</span></span> <span data-ttu-id="ee5d0-106">Para dibujar líneas, el procedimiento de ventana puede recuperar un contexto de dispositivo de pantalla y dibujar una línea en la ventana entre las posiciones del cursor actual y anterior.</span><span class="sxs-lookup"><span data-stu-id="ee5d0-106">To draw lines, the window procedure can retrieve a display device context and draw a line in the window between the current and previous cursor positions.</span></span>

<span data-ttu-id="ee5d0-107">En el ejemplo siguiente, el procedimiento de ventana se prepara para dibujar cuando el usuario presiona y mantiene presionado el botón primario del mouse (enviando el mensaje de [**\_ LBUTTONDOWN de WM**](../inputdev/wm-lbuttondown.md) ).</span><span class="sxs-lookup"><span data-stu-id="ee5d0-107">In the following example, the window procedure prepares for drawing when the user presses and holds the left mouse button (sending the [**WM\_LBUTTONDOWN**](../inputdev/wm-lbuttondown.md) message).</span></span> <span data-ttu-id="ee5d0-108">Cuando el usuario mueve el cursor dentro de la ventana, el procedimiento de ventana recibe una serie de mensajes del [**\_ MOUSEMOVE de WM**](../inputdev/wm-mousemove.md) .</span><span class="sxs-lookup"><span data-stu-id="ee5d0-108">As the user moves the cursor within the window, the window procedure receives a series of [**WM\_MOUSEMOVE**](../inputdev/wm-mousemove.md) messages.</span></span> <span data-ttu-id="ee5d0-109">Para cada mensaje, el procedimiento de ventana dibuja una línea que conecta la posición anterior y la posición actual.</span><span class="sxs-lookup"><span data-stu-id="ee5d0-109">For each message, the window procedure draws a line connecting the previous position and the current position.</span></span> <span data-ttu-id="ee5d0-110">Para dibujar la línea, el procedimiento usa [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) para recuperar un contexto de dispositivo de pantalla. después, en cuanto se complete el dibujo y antes de que se devuelva el mensaje, el procedimiento usa la función [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) para liberar el contexto de dispositivo de pantalla.</span><span class="sxs-lookup"><span data-stu-id="ee5d0-110">To draw the line, the procedure uses [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) to retrieve a display device context; then, as soon as drawing is complete and before returning from the message, the procedure uses the [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) function to release the display device context.</span></span> <span data-ttu-id="ee5d0-111">En cuanto el usuario suelta el botón del mouse, el procedimiento de ventana borra la marca y el dibujo se detiene (que envía el mensaje de [**\_ LBUTTONUP de WM**](../inputdev/wm-lbuttonup.md) ).</span><span class="sxs-lookup"><span data-stu-id="ee5d0-111">As soon as the user releases the mouse button, the window procedure clears the flag, and the drawing stops (which sends the [**WM\_LBUTTONUP**](../inputdev/wm-lbuttonup.md) message).</span></span>


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



<span data-ttu-id="ee5d0-112">Una aplicación que permite dibujar, como en este ejemplo, normalmente registra los puntos o las líneas para que se puedan volver a dibujar las líneas cada vez que se actualice la ventana.</span><span class="sxs-lookup"><span data-stu-id="ee5d0-112">An application that enables drawing, as in this example, typically records either the points or lines so that the lines can be redrawn whenever the window is updated.</span></span> <span data-ttu-id="ee5d0-113">Las aplicaciones de dibujo suelen utilizar un contexto de dispositivo de memoria y un mapa de bits asociado para almacenar líneas dibujadas con un mouse.</span><span class="sxs-lookup"><span data-stu-id="ee5d0-113">Drawing applications often use a memory device context and an associated bitmap to store lines that were drawn by using a mouse.</span></span>

 

 
