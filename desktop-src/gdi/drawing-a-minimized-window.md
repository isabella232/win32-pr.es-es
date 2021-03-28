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
# <a name="drawing-a-minimized-window"></a><span data-ttu-id="7b1df-103">Dibujar una ventana minimizada</span><span class="sxs-lookup"><span data-stu-id="7b1df-103">Drawing a Minimized Window</span></span>

<span data-ttu-id="7b1df-104">Puede dibujar sus propias ventanas minimizadas en lugar de que el sistema las dibuje automáticamente.</span><span class="sxs-lookup"><span data-stu-id="7b1df-104">You can draw your own minimized windows rather than having the system draw them for you.</span></span> <span data-ttu-id="7b1df-105">La mayoría de las aplicaciones definen un icono de clase al registrar la clase de ventana para la ventana y el sistema dibuja el icono cuando la ventana está minimizada.</span><span class="sxs-lookup"><span data-stu-id="7b1df-105">Most applications define a class icon when registering the window class for the window, and the system draws the icon when the window is minimized.</span></span> <span data-ttu-id="7b1df-106">Sin embargo, si establece el icono de clase en **null**, el sistema envía un mensaje de [**\_ dibujo de WM**](wm-paint.md) al procedimiento de ventana cada vez que se minimiza la ventana, lo que permite que el procedimiento de ventana dibuje en la ventana minimizada.</span><span class="sxs-lookup"><span data-stu-id="7b1df-106">If you set the class icon to **NULL**, however, the system sends a [**WM\_PAINT**](wm-paint.md) message to your window procedure whenever the window is minimized, enabling the window procedure to draw in the minimized window.</span></span>

<span data-ttu-id="7b1df-107">En el ejemplo siguiente, el procedimiento de ventana dibuja una estrella en la ventana minimizada.</span><span class="sxs-lookup"><span data-stu-id="7b1df-107">In the following example, the window procedure draws a star in the minimized window.</span></span> <span data-ttu-id="7b1df-108">El procedimiento usa la función [**IsIconic**](/windows/win32/api/winuser/nf-winuser-isiconic) para determinar cuándo se minimiza la ventana.</span><span class="sxs-lookup"><span data-stu-id="7b1df-108">The procedure uses the [**IsIconic**](/windows/win32/api/winuser/nf-winuser-isiconic) function to determine when the window is minimized.</span></span> <span data-ttu-id="7b1df-109">Esto garantiza que la estrella solo se dibuja cuando la ventana está minimizada.</span><span class="sxs-lookup"><span data-stu-id="7b1df-109">This ensures that the star is drawn only when the window is minimized.</span></span>


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



<span data-ttu-id="7b1df-110">Establezca el icono de clase en **null** estableciendo el miembro **hIcon** de la estructura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) en **null** antes de llamar a la función [**RegisterClass**](/windows/win32/api/winuser/nf-winuser-registerclassa) para la clase de ventana.</span><span class="sxs-lookup"><span data-stu-id="7b1df-110">You set the class icon to **NULL** by setting the **hIcon** member of the [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) structure to **NULL** before calling the [**RegisterClass**](/windows/win32/api/winuser/nf-winuser-registerclassa) function for the window class.</span></span>

 

 
