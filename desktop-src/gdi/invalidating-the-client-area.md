---
description: El sistema no es el único origen de mensajes de pintado de WM \_ . La función InvalidateRect o InvalidateRgn puede generar indirectamente \_ mensajes de WM Paint para las ventanas. Estas funciones marcan todo o parte de un área cliente como no válida (se debe volver a dibujar).
ms.assetid: 41c2bc07-768b-4d27-a869-69b072f3e033
title: Invalidar el área de cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76fb02be44f600b80f87ec8f05c022fa3c35d827
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997348"
---
# <a name="invalidating-the-client-area"></a><span data-ttu-id="14c27-105">Invalidar el área de cliente</span><span class="sxs-lookup"><span data-stu-id="14c27-105">Invalidating the Client Area</span></span>

<span data-ttu-id="14c27-106">El sistema no es el único origen de mensajes de [**\_ pintado de WM**](wm-paint.md) .</span><span class="sxs-lookup"><span data-stu-id="14c27-106">The system is not the only source of [**WM\_PAINT**](wm-paint.md) messages.</span></span> <span data-ttu-id="14c27-107">La función [**InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) o [**InvalidateRgn**](/windows/desktop/api/Winuser/nf-winuser-invalidatergn) puede generar indirectamente mensajes de **WM \_ Paint** para las ventanas.</span><span class="sxs-lookup"><span data-stu-id="14c27-107">The [**InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) or [**InvalidateRgn**](/windows/desktop/api/Winuser/nf-winuser-invalidatergn) function can indirectly generate **WM\_PAINT** messages for your windows.</span></span> <span data-ttu-id="14c27-108">Estas funciones marcan todo o parte de un área cliente como no válida (se debe volver a dibujar).</span><span class="sxs-lookup"><span data-stu-id="14c27-108">These functions mark all or part of a client area as invalid (that must be redrawn).</span></span>

<span data-ttu-id="14c27-109">En el ejemplo siguiente, el procedimiento de ventana invalida todo el área cliente cuando se procesan mensajes de [**WM \_ Char**](../inputdev/wm-char.md) .</span><span class="sxs-lookup"><span data-stu-id="14c27-109">In the following example, the window procedure invalidates the entire client area when processing [**WM\_CHAR**](../inputdev/wm-char.md) messages.</span></span> <span data-ttu-id="14c27-110">Esto permite al usuario cambiar la figura escribiendo un número y ver los resultados; Estos resultados se dibujan en cuanto no hay ningún otro mensaje en la cola de mensajes de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="14c27-110">This allows the user to change the figure by typing a number and view the results; these results are drawn as soon as there are no other messages in the application's message queue.</span></span>


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



<span data-ttu-id="14c27-111">En este ejemplo, el argumento **null** que usa [**InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) especifica el área de cliente completa; el argumento **true** hace que se borre el fondo.</span><span class="sxs-lookup"><span data-stu-id="14c27-111">In this example, the **NULL** argument used by [**InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) specifies the entire client area; the **TRUE** argument causes the background to be erased.</span></span> <span data-ttu-id="14c27-112">Si no desea que la aplicación espere hasta que la cola de mensajes de la aplicación no tenga ningún otro mensaje, utilice la función [**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow) para obligar a que el mensaje de [**\_ dibujo de WM**](wm-paint.md) se envíe inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="14c27-112">If you do not want the application to wait until the application's message queue has no other messages, use the [**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow) function to force the [**WM\_PAINT**](wm-paint.md) message to be sent immediately.</span></span> <span data-ttu-id="14c27-113">Si hay alguna parte no válida del área cliente, **UpdateWindow** envía el mensaje **de \_ dibujo de WM** para la ventana especificada directamente al procedimiento de ventana.</span><span class="sxs-lookup"><span data-stu-id="14c27-113">If there is any invalid part of the client area, **UpdateWindow** sends the **WM\_PAINT** message for the specified window directly to the window procedure.</span></span>

 

 
