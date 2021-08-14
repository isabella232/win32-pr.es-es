---
description: Para responder a un mensaje \_ WM PAINT, use código como el siguiente.
ms.assetid: 682d9bc6-8d74-48c4-80fb-bae73d409a6b
title: Pintar en un controlador de dominio que abarca varias pantallas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 550279d003c7d32fc97923ea6ebe4c95364773e514a69e4c66bdb4b100784384
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118759486"
---
# <a name="painting-on-a-dc-that-spans-multiple-displays"></a>Pintar en un controlador de dominio que abarca varias pantallas

Para responder a un **mensaje \_ WM PAINT,** use código como el siguiente.


```C++
case WM_PAINT:
hdc = BeginPaint(hwnd, &ps);
EnumDisplayMonitors(hdc, NULL, MyPaintEnumProc, 0);
EndPaint(hwnd, &ps);
 
```



Para pintar la mitad superior de una ventana, use código como el siguiente.


```C++
GetClient Rect(hwnd, &rc);
rc.bottom = (rc.bottom - rc.top) / 2;
hdc = GetDC(hwnd);
EnumDisplayMonitors(hdc, &rc, MyPaintEnumProc, 0);
ReleaseDC(hwnd, hdc);
```



Para pintar toda la pantalla virtual de forma óptima para cada monitor, use código como el siguiente.


```C++
hdc = GetDC(NULL);
EnumDisplayMonitors(hdc, NULL, MyPaintScreenEnumProc, 0);
ReleaseDC(NULL, hdc);
```



 

 



