---
title: Creación de una ventana de MCIWnd
description: Creación de una ventana de MCIWnd
ms.assetid: bd45e813-5807-43cd-bef1-03285df9a018
keywords:
- Ventana de MCIWnd, crear
- Función MCIWndCreate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2a44096f4edbf590416a98e83b0efc2408a4bee93ee3a2814996bcae466937d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119785805"
---
# <a name="creating-an-mciwnd-window"></a>Creación de una ventana de MCIWnd

La [**función MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) registra y crea una ventana MCIWnd. La ventana puede ser una ventana primaria, secundaria o emergente. En el ejemplo siguiente se crea una ventana MCIWnd como una ventana secundaria y se permite al usuario controlar la reproducción proporcionando acceso a la barra de seguimiento y a los botones **Reproducir,** **Detener** y **Menú.** En el ejemplo se especifica un identificador de una ventana primaria y se especifica **NULL** para los estilos de ventana, por lo que se usan los estilos de ventana predeterminados de WS CHILD, WS BORDER y WS VISIBLE para crear la ventana \_ \_ \_ MCIWnd.


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

 

 

 




