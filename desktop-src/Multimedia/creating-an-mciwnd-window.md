---
title: Crear una ventana de MCIWnd
description: Crear una ventana de MCIWnd
ms.assetid: bd45e813-5807-43cd-bef1-03285df9a018
keywords:
- Ventana de MCIWnd, crear
- MCIWndCreate función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c205e87acf3e5f529d4b5cc9c9163b7fe887fe04
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105676133"
---
# <a name="creating-an-mciwnd-window"></a>Crear una ventana de MCIWnd

La función [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) se registra y crea una ventana MCIWnd. La ventana puede ser una ventana primaria, secundaria o emergente. En el ejemplo siguiente se crea una ventana de MCIWnd como una ventana secundaria y se permite que el usuario controle la reproducción mediante el acceso a la barra de menús y los botones de **reproducción**, **detención** y **menú** . En el ejemplo se especifica un identificador de una ventana primaria y se especifica **null** para los estilos de ventana, por lo que los estilos de ventana predeterminados WS \_ Child, WS \_ Border y WS \_ visible se usan para crear la ventana MCIWnd.


```C++
// Global variable and constants 
// extern HINSTANCE g_hinst;       instance handle 
// extern HWND g_hwndMCIWnd;       MCIWnd window handle 
 
case WM_COMMAND: 
    switch (wParam) { 
    case IDM_CREATEMCIWND: 
        g_hwndMCIWnd = MCIWndCreate(hwnd, g_hinst, NULL, 
            "sample.avi"); 
        break;    
    } 
    break; 
```



> [!Note]  
> También puede especificar **null** tanto para el identificador de ventana primario como para los estilos de ventana, en cuyo caso los estilos de ventana predeterminados SERÍAn WS \_ superpuesto y WS \_ visible.

 

 

 




