---
title: Stretching an Image and Window
description: Stretching an Image and Window
ms.assetid: 661992eb-b012-47eb-84bc-cd12834c6270
keywords:
- Macro MCIWndGetDest
- Macro MCIWndPutDest
- Función GetWindowRect
- Función SetWindowPos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a38cc3072be387f549e77186886854c8cf6a40a466ca5014c4eb85469faf762b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119781865"
---
# <a name="stretching-an-image-and-window"></a>Stretching an Image and Window

En el ejemplo siguiente se extienden las imágenes de un clip de vídeo y se cambia la relación de aspecto de los fotogramas mostrados. Los fotogramas mostrados en la ventana MCIWnd tienen el doble de alto y tres veces el ancho del marco original. Las macros [**MCIWndGetDest**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdest) y [**MCIWndPutDest**](/windows/desktop/api/Vfw/nf-vfw-mciwndputdest) recuperan y redefinen las coordenadas del rectángulo de destino. Las [funciones GetWindowRect](/windows/win32/api/winuser/nf-winuser-getwindowrect) [y SetWindowPos](/windows/win32/api/winuser/nf-winuser-setwindowpos) administran los cambios en las dimensiones de ventana de MCIWnd.


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



 

 