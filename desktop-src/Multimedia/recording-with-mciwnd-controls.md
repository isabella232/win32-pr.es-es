---
title: Grabar con controles MCIWnd
description: Grabar con controles MCIWnd
ms.assetid: 65a57400-aeea-4a27-8d51-37d3d9e9bd55
keywords:
- MCIWndCreate función)
- MCIWndNew (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 814bd9f92b895c03ccbb073f830dbf31dcd2e3c2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103993941"
---
# <a name="recording-with-mciwnd-controls"></a>Grabar con controles MCIWnd

En el ejemplo siguiente se registra el audio de una onda mediante los controles integrados de la ventana MCIWnd. En el ejemplo se crea una ventana de MCIWnd mediante el \_ estilo de ventana registro MCIWNDF con la función [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) para agregar un botón **registro** a la barra de herramientas. La macro [**MCIWndNew**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew) indica que un nuevo archivo está asociado a la ventana de MCIWnd y que un dispositivo de audio de forma de onda proporcionará su contenido. Un segundo comando de menú, \_ SAVEMCIWND de IDM, permite al usuario guardar la grabación y seleccionar un nombre de archivo mediante la macro [**MCIWndSaveDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndsavedialog) .


```C++
case WM_COMMAND: 
    switch (wParam) { 
    case IDM_CREATEMCIWND: 
        g_hwndMCIWnd = MCIWndCreate(hwnd, g_hinst, 
            WS_VISIBLE | MCIWNDF_RECORD, NULL); 
        MCIWndNew(g_hwndMCIWnd, "waveaudio"); 
        break;    
    case IDM_SAVEMCIWND: 
        MCIWndSaveDialog(g_hwndMCIWnd); 
        break; 
    } 
```



 

 




