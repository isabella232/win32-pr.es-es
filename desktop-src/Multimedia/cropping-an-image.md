---
title: Recortar una imagen
description: Recortar una imagen
ms.assetid: 6600751c-d4b6-481d-bf69-be2d34244c05
keywords:
- Macro MCIWndGetSource
- Macro MCIWndPutSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2d73eb37792c124ad907f660d4b906ca80e715d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074263"
---
# <a name="cropping-an-image"></a>Recortar una imagen

En el ejemplo siguiente se crea una ventana MCIWnd y se carga un archivo AVI. La ventana incluye un comando de recorte en el menú, que recorta un cuarto del alto o ancho de cada uno de los cuatro lados del marco. En el ejemplo se recuperan las dimensiones actuales (iniciales) del rectángulo de origen mediante la macro [**MCIWndGetSource.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetsource) El rectángulo de origen modificado es la mitad del alto y ancho originales y se centra en el marco original. La llamada a la [**macro MCIWndPutSource**](/windows/desktop/api/Vfw/nf-vfw-mciwndputsource) redefine las coordenadas del rectángulo de origen.


```C++
// extern RECT rSource, rDest; 
 
case WM_COMMAND: 
    switch (wParam) 
    { 
        case IDM_CREATEMCIWND: 
            g_hwndMCIWnd = MCIWndCreate( hwnd, 
                g_hinst, 
                WS_CHILD | WS_VISIBLE, 
                "sample.avi" ); 
            break; 
        case IDM_CROPIMAGE:                          // crops image 
            MCIWndGetSource(g_hwndMCIWnd, &rSource); // source rectangle
            rDest.left = rSource.left +              // new boundaries
                ((rSource.right - rSource.left) / 4); 
            rDest.right = rSource.right - 
                ((rSource.right - rSource.left) / 4); 
            rDest.top = rSource.top + 
                ((rSource.bottom - rSource.top) / 4); 
            rDest.bottom = rSource.bottom - 
                ((rSource.bottom - rSource.top) / 4); 
 
            MCIWndPutSource(g_hwndMCIWnd, &rDest);   // new source rectangle 
    } 
    break; 

    // Handle other messages here. 
```



 

 




