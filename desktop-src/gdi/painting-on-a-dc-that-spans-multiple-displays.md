---
description: Para responder a un mensaje de dibujo de WM \_ , use código similar al siguiente.
ms.assetid: 682d9bc6-8d74-48c4-80fb-bae73d409a6b
title: Pintar en un controlador de dominio que abarca varias pantallas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e5b1b85c8aab20b7ef2415c1d67188ecab7728c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544438"
---
# <a name="painting-on-a-dc-that-spans-multiple-displays"></a><span data-ttu-id="76b73-103">Pintar en un controlador de dominio que abarca varias pantallas</span><span class="sxs-lookup"><span data-stu-id="76b73-103">Painting on a DC That Spans Multiple Displays</span></span>

<span data-ttu-id="76b73-104">Para responder a un mensaje de **\_ dibujo de WM** , use código similar al siguiente.</span><span class="sxs-lookup"><span data-stu-id="76b73-104">To respond to a **WM\_PAINT** message, use code like the following.</span></span>


```C++
case WM_PAINT:
hdc = BeginPaint(hwnd, &ps);
EnumDisplayMonitors(hdc, NULL, MyPaintEnumProc, 0);
EndPaint(hwnd, &ps);
 
```



<span data-ttu-id="76b73-105">Para pintar la mitad superior de una ventana, use código similar al siguiente.</span><span class="sxs-lookup"><span data-stu-id="76b73-105">To paint the top half of a window, use code like the following.</span></span>


```C++
GetClient Rect(hwnd, &rc);
rc.bottom = (rc.bottom - rc.top) / 2;
hdc = GetDC(hwnd);
EnumDisplayMonitors(hdc, &rc, MyPaintEnumProc, 0);
ReleaseDC(hwnd, hdc);
```



<span data-ttu-id="76b73-106">Para pintar toda la pantalla virtual de forma óptima para cada monitor, use código similar al siguiente.</span><span class="sxs-lookup"><span data-stu-id="76b73-106">To paint the entire virtual screen optimally for each monitor, use code like the following.</span></span>


```C++
hdc = GetDC(NULL);
EnumDisplayMonitors(hdc, NULL, MyPaintScreenEnumProc, 0);
ReleaseDC(NULL, hdc);
```



 

 



