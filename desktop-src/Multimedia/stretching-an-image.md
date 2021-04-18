---
title: Ajustar una imagen
description: Ajustar una imagen
ms.assetid: 7cfd91c3-0ebd-47eb-a33d-c81a66f820e5
keywords:
- MCIWndGetDest (macro)
- MCIWndPutDest (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0296cd31988ba79aeab9221fb41b4fd150ffc09
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357496"
---
# <a name="stretching-an-image"></a><span data-ttu-id="d3a5e-105">Ajustar una imagen</span><span class="sxs-lookup"><span data-stu-id="d3a5e-105">Stretching an Image</span></span>

<span data-ttu-id="d3a5e-106">En el ejemplo siguiente se extienden las imágenes de un clip de vídeo.</span><span class="sxs-lookup"><span data-stu-id="d3a5e-106">The following example stretches the images of a video clip.</span></span> <span data-ttu-id="d3a5e-107">Aumenta las dimensiones del rectángulo de destino mediante la macro [**MCIWndPutDest**](/windows/desktop/api/Vfw/nf-vfw-mciwndputdest) .</span><span class="sxs-lookup"><span data-stu-id="d3a5e-107">It increases the dimensions of the destination rectangle by using the [**MCIWndPutDest**](/windows/desktop/api/Vfw/nf-vfw-mciwndputdest) macro.</span></span> <span data-ttu-id="d3a5e-108">El tamaño del área de reproducción permanece sin cambios, por lo que el resultado es una imagen distorsionada y ampliada.</span><span class="sxs-lookup"><span data-stu-id="d3a5e-108">The size of the playback area remains unchanged, so the result is a distorted, magnified image.</span></span> <span data-ttu-id="d3a5e-109">En los ejemplos se usa la función **MCIWndPutDest** para cambiar la posición del rectángulo de destino con respecto al área de reproducción, lo que proporciona una manera de ver distintas partes de la imagen ajustada.</span><span class="sxs-lookup"><span data-stu-id="d3a5e-109">The examples uses the **MCIWndPutDest** function to reposition the destination rectangle with respect to the playback area, providing a way to view different portions of the stretched image.</span></span>


```C++
extern RECT rCurrent, rDest; 
 
case WM_COMMAND: 
   switch (wParam) 
   { 
       case IDM_CREATEMCIWND: 
           g_hwndMCIWnd = MCIWndCreate(hwnd, 
               g_hinst, 
               WS_CHILD | WS_VISIBLE, 
               "sample.avi"); 
           break; 
 
       case  IDM_STRETCHIMAGE:      // stretch destination RECT 3:2, 
           MCIWndGetDest(g_hwndMCIWnd, &rCurrent); // destination RECT 
           rDest.top = rCurrent.top;               // new boundaries 
           rDest.right = rCurrent.right; 
           rDest.left = rCurrent.left + 
               ((rCurrent.left - rCurrent.right) * 3); 
           rDest.bottom = rCurrent.top + 
               ((rCurrent.bottom - rCurrent.top) * 2); 
           MCIWndPutDest(g_hwndMCIWnd, &rDest); // new destination 
           break; 
       case IDM_MOVEDOWN:           // move toward bottom of image 
           MCIWndGetDest(g_hwndMCIWnd, &rCurrent); // destination RECT 
           rCurrent.top -= 100;                    // new boundaries 
           rCurrent.bottom -= 100; 
           MCIWndPutDest(g_hwndMCIWnd, &rCurrent); // new destination
           break; 
       case IDM_MOVEUP:             // move toward top of image 
           MCIWndGetDest(g_hwndMCIWnd, &rCurrent); // destination RECT 
           rCurrent.top += 100;                    // new boundaries 
           rCurrent.bottom += 100; 
           MCIWndPutDest(g_hwndMCIWnd, &rCurrent); // new destination 
           break; 
       case IDM_MOVELEFT:           // move toward left edge of image
           MCIWndGetDest(g_hwndMCIWnd, &rCurrent); // destination RECT 
           rCurrent.right += 100;                  // new boundaries 
           rCurrent.left += 100; 
           MCIWndPutDest(g_hwndMCIWnd, &rCurrent); // new destination 
           break; 
       case  IDM_MOVERIGHT:         // move toward right edge of image
           MCIWndGetDest(g_hwndMCIWnd, &rCurrent); // destination RECT
           rCurrent.right -= 100;                  // new boundaries 
           rCurrent.left -= 100; 
           MCIWndPutDest(g_hwndMCIWnd, &rCurrent); // new destination 
           break; 
   } 
   break; 
 
   // Handle other messages here. 
```



 

 




