---
title: Creación de una ventana de MCIWnd
description: Creación de una ventana de MCIWnd
ms.assetid: bd45e813-5807-43cd-bef1-03285df9a018
keywords:
- Ventana de MCIWnd, crear
- Función MCIWndCreate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c205e87acf3e5f529d4b5cc9c9163b7fe887fe04
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071780"
---
# <a name="creating-an-mciwnd-window"></a>Creación de una ventana de MCIWnd

La [**función MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) registra y crea una ventana de MCIWnd. La ventana puede ser una ventana primaria, secundaria o emergente. En el ejemplo siguiente se crea una ventana MCIWnd como una ventana secundaria y permite al usuario controlar la reproducción proporcionando acceso a la barra de seguimiento y a los botones **Reproducir,** **Detener** y **Menú.** En el ejemplo se especifica un identificador de una ventana primaria y se especifica **NULL** para los estilos de ventana, por lo que se usan los estilos de ventana predeterminados de WS CHILD, WS BORDER y WS VISIBLE para crear la ventana \_ \_ \_ MCIWnd.


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
> También puede especificar **NULL para** el identificador de ventana primaria y los estilos de ventana, en cuyo caso los estilos de ventana predeterminados seríaN WS OVERLAPPED y \_ WS \_ VISIBLE.

 

 

 




