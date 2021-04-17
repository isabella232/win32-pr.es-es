---
title: Ajustar una imagen y una ventana
description: Ajustar una imagen y una ventana
ms.assetid: 661992eb-b012-47eb-84bc-cd12834c6270
keywords:
- MCIWndGetDest (macro)
- MCIWndPutDest (macro)
- GetWindowRect (función)
- Función SetWindowPos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ee8ef0bd4d549e6fbe29ced52304cded4ce6979
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105665795"
---
# <a name="stretching-an-image-and-window"></a><span data-ttu-id="cdfb0-107">Ajustar una imagen y una ventana</span><span class="sxs-lookup"><span data-stu-id="cdfb0-107">Stretching an Image and Window</span></span>

<span data-ttu-id="cdfb0-108">En el ejemplo siguiente se ajustan las imágenes de un clip de vídeo y se cambia la relación de aspecto de los fotogramas mostrados.</span><span class="sxs-lookup"><span data-stu-id="cdfb0-108">The following example stretches the images of a video clip and changes the aspect ratio of the displayed frames.</span></span> <span data-ttu-id="cdfb0-109">Los fotogramas mostrados en la ventana de MCIWnd son dos veces el alto y tres veces el ancho del fotograma original.</span><span class="sxs-lookup"><span data-stu-id="cdfb0-109">The frames displayed in the MCIWnd window are twice the height and three times the width of the original frame.</span></span> <span data-ttu-id="cdfb0-110">Las macros [**MCIWndGetDest**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdest) y [**MCIWndPutDest**](/windows/desktop/api/Vfw/nf-vfw-mciwndputdest) recuperan y vuelven a definir las coordenadas del rectángulo de destino.</span><span class="sxs-lookup"><span data-stu-id="cdfb0-110">The [**MCIWndGetDest**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdest) and [**MCIWndPutDest**](/windows/desktop/api/Vfw/nf-vfw-mciwndputdest) macros retrieve and redefine the destination rectangle coordinates.</span></span> <span data-ttu-id="cdfb0-111">Las funciones [GetWindowRect](/windows/win32/api/winuser/nf-winuser-getwindowrect) y [SetWindowPos](/windows/win32/api/winuser/nf-winuser-setwindowpos) administran los cambios en las dimensiones de la ventana MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="cdfb0-111">The [GetWindowRect](/windows/win32/api/winuser/nf-winuser-getwindowrect) and [SetWindowPos](/windows/win32/api/winuser/nf-winuser-setwindowpos) functions manage changes to the MCIWnd window dimensions.</span></span>


```C++
// extern RECT rCurrent, rDest; 
 
case WM_COMMAND: 
   switch (wParam) 
   { 
       case IDM_CREATEMCIWND: 
           g_hwndMCIWnd = MCIWndCreate(hwnd, 
           g_hinst, 
           WS_CHILD | WS_VISIBLE, 
          "sample.avi"); 
           break;    
 
       case IDM_RESIZEWINDOW: // destination RECT and playback area
           GetWindowRect(g_hwndMCIWnd, &rWin);     // window size 
           MCIWndGetDest(g_hwndMCIWnd, &rCurrent); // destination RECT
           rDest.top = rCurrent.top;               // new boundaries 
           rDest.right = rCurrent.right; 
           rDest.left = rCurrent.left + 
               ((rCurrent.left - rCurrent.right) * 3); 
           rDest.bottom = rCurrent.top + 
               ((rCurrent.bottom - rCurrent.top) * 2); 
           MCIWndPutDest(g_hwndMCIWnd, &rDest); // new RECT
           SetWindowPos(g_hwndMCIWnd,           // window to resize 
               NULL,                          // z-order: don't care 
               0, 0,                          // position: don't care
               rDest.right - rDest.left,      // width 
               (rWin.bottom - rWin.top +           // height (window - 
               (rCurrent.bottom - rCurrent.top) +  //  original RECT +
               (rDest.bottom - rDest.top)),        //  new RECT
               SWP_NOMOVE | SWP_NOZORDER | SWP_NOACTIVATE); 
           break; 
   } 
   break; 
 
   // Handle other messages here. 
```



 

 