---
title: Grabación con controles MCIWnd
description: Grabación con controles MCIWnd
ms.assetid: 65a57400-aeea-4a27-8d51-37d3d9e9bd55
keywords:
- Función MCIWndCreate
- Macro MCIWndNew
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 814bd9f92b895c03ccbb073f830dbf31dcd2e3c2
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370849"
---
# <a name="recording-with-mciwnd-controls"></a>Grabación con controles MCIWnd

En el ejemplo siguiente se registra el audio de forma de onda mediante los controles integrados de la ventana MCIWnd. En el ejemplo se crea una ventana MCIWnd mediante el estilo de ventana MCIWNDF RECORD con la función \_ [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) para agregar un botón **Registro** a la barra de herramientas. La [**macro MCIWndNew**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew) indica que un nuevo archivo está asociado a la ventana MCIWnd y que un dispositivo de audio de forma de onda proporcionará su contenido. Un segundo comando de menú, IDM SAVEMCIWND, permite al usuario guardar la grabación y seleccionar un nombre de archivo mediante la \_ macro [**MCIWndSaveDialog.**](/windows/desktop/api/Vfw/nf-vfw-mciwndsavedialog)


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



 

 




