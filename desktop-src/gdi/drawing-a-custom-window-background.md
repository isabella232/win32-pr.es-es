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
# <a name="drawing-a-custom-window-background"></a><span data-ttu-id="55993-103">Dibujo de un fondo de ventana personalizado</span><span class="sxs-lookup"><span data-stu-id="55993-103">Drawing a Custom Window Background</span></span>

<span data-ttu-id="55993-104">Puede dibujar su propio fondo de la ventana en lugar de hacer que el sistema lo dibuje automáticamente.</span><span class="sxs-lookup"><span data-stu-id="55993-104">You can draw your own window background rather than having the system draw it for you.</span></span> <span data-ttu-id="55993-105">La mayoría de las aplicaciones especifican un identificador de pincel o un valor de color del sistema para el pincel de fondo de clase al registrar la clase de ventana. el sistema utiliza el pincel o el color para dibujar el fondo.</span><span class="sxs-lookup"><span data-stu-id="55993-105">Most applications specify a brush handle or system color value for the class background brush when registering the window class; the system uses the brush or color to draw the background.</span></span> <span data-ttu-id="55993-106">Sin embargo, si establece el pincel de fondo de clase en **null**, el sistema envía un mensaje de [**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md) al procedimiento de ventana cada vez que se debe dibujar el fondo de la ventana, lo que le permite dibujar un fondo personalizado.</span><span class="sxs-lookup"><span data-stu-id="55993-106">If you set the class background brush to **NULL**, however, the system sends a [**WM\_ERASEBKGND**](../winmsg/wm-erasebkgnd.md) message to your window procedure whenever the window background must be drawn, letting you draw a custom background.</span></span>

<span data-ttu-id="55993-107">En el ejemplo siguiente, el procedimiento de ventana dibuja un patrón de tablero de ajedrez grande que se adapta perfectamente a la ventana.</span><span class="sxs-lookup"><span data-stu-id="55993-107">In the following example, the window procedure draws a large checkerboard pattern that fits neatly in the window.</span></span> <span data-ttu-id="55993-108">El procedimiento rellena el área cliente con un pincel blanco y, a continuación, dibuja los rectángulos 13 20 por 20 con un pincel gris.</span><span class="sxs-lookup"><span data-stu-id="55993-108">The procedure fills the client area with a white brush and then draws thirteen 20-by-20 rectangles using a gray brush.</span></span> <span data-ttu-id="55993-109">El contexto de dispositivo de pantalla que se va a usar al dibujar el fondo se especifica en el parámetro *wParam* del mensaje.</span><span class="sxs-lookup"><span data-stu-id="55993-109">The display device context to use when drawing the background is specified in the *wParam* parameter for the message.</span></span>


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



<span data-ttu-id="55993-110">Si la aplicación dibuja su propia ventana minimizada, el sistema también envía el mensaje de [**\_ ERASEBKGND de WM**](../winmsg/wm-erasebkgnd.md) al procedimiento de ventana para dibujar el fondo de la ventana minimizada.</span><span class="sxs-lookup"><span data-stu-id="55993-110">If the application draws its own minimized window, the system also sends the [**WM\_ERASEBKGND**](../winmsg/wm-erasebkgnd.md) message to the window procedure to draw the background for the minimized window.</span></span> <span data-ttu-id="55993-111">Puede usar la misma técnica usada por [**WM \_ Paint**](wm-paint.md) para determinar si la ventana está minimizada es decir, llamar a la función [**IsIconic**](/windows/win32/api/winuser/nf-winuser-isiconic) y comprobar el valor devuelto **true**.</span><span class="sxs-lookup"><span data-stu-id="55993-111">You can use the same technique used by [**WM\_PAINT**](wm-paint.md) to determine whether the window is minimized that is, call the [**IsIconic**](/windows/win32/api/winuser/nf-winuser-isiconic) function and check for the return value **TRUE**.</span></span>

 

 
