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
# <a name="painting-on-a-dc-that-spans-multiple-displays"></a>Pintar en un controlador de dominio que abarca varias pantallas

Para responder a un mensaje de **\_ dibujo de WM** , use código similar al siguiente.


```C++
case WM_PAINT:
hdc = BeginPaint(hwnd, &ps);
EnumDisplayMonitors(hdc, NULL, MyPaintEnumProc, 0);
EndPaint(hwnd, &ps);
 
```



Para pintar la mitad superior de una ventana, use código similar al siguiente.


```C++
GetClient Rect(hwnd, &rc);
rc.bottom = (rc.bottom - rc.top) / 2;
hdc = GetDC(hwnd);
EnumDisplayMonitors(hdc, &rc, MyPaintEnumProc, 0);
ReleaseDC(hwnd, hdc);
```



Para pintar toda la pantalla virtual de forma óptima para cada monitor, use código similar al siguiente.


```C++
hdc = GetDC(NULL);
EnumDisplayMonitors(hdc, NULL, MyPaintScreenEnumProc, 0);
ReleaseDC(NULL, hdc);
```



 

 



