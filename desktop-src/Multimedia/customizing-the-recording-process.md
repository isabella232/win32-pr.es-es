---
title: Personalización del proceso de grabación
description: Personalización del proceso de grabación
ms.assetid: 9453b9d3-ae9c-4f57-8dd6-f84b9a76618e
keywords:
- Función MCIWndCreate
- Macro MCIWndNew
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 050b3b3f55fdd412a1c5ecab70cbb34fd63f85c0ea7144e1407a97f299444aaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119785465"
---
# <a name="customizing-the-recording-process"></a>Personalización del proceso de grabación

Puede personalizar el proceso de grabación, tomando el control completo de la mayoría de todo, desde la creación de la ventana MCIWnd hasta el guardado de la información registrada en un archivo. En el ejemplo siguiente se consulta el dispositivo MCI para registrar y guardar funcionalidades, e incluye comandos de menú para grabar al principio o al final del contenido.

En el ejemplo siguiente se usa la función [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) para crear una nueva ventana y se permite especificar un archivo existente para almacenar los datos registrados y la macro [**MCIWndNew**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew) para asociar un nuevo archivo a la ventana. Como alternativa, puede usar la macro [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen) o [**MCIWndOpenDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndopendialog) para especificar un archivo.

En el ejemplo se usa la macro [**MCIWndCanRecord**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanrecord) para comprobar que el dispositivo puede registrar y la macro [**MCIWndCanSave**](/windows/desktop/api/Vfw/nf-vfw-mciwndcansave) para comprobar que el dispositivo guarda la información. En el ejemplo se establece la posición de reproducción actual mediante las macros [**MCIWndHome**](/windows/desktop/api/Vfw/nf-vfw-mciwndhome) y [**MCIWndEnd.**](/windows/desktop/api/Vfw/nf-vfw-mciwndend) En el ejemplo se inicia la grabación mediante la macro [**MCIWndRecord.**](/windows/desktop/api/Vfw/nf-vfw-mciwndrecord) Una vez registrada la información, el ejemplo la guarda mediante la macro [**MCIWndSaveDialog.**](/windows/desktop/api/Vfw/nf-vfw-mciwndsavedialog)


```C++
case WM_COMMAND: 
    switch (wParam) 
    { 
        case IDM_CREATEMCIWND: 
            g_hwndMCIWnd = MCIWndCreate( hwnd, g_hinst, 
                WS_VISIBLE | WS_CHILD | 
                MCIWNDF_RECORD,                   // add Record button
                NULL ); 
 
            MCIWndNew(g_hwndMCIWnd, "waveaudio"); // new file 
 
            if( MCIWndCanRecord(g_hwndMCIWnd) ) 
            { 
                MessageBox( hwnd, 
                "Press the red button on the toolbar to record.", 
                "MCIWnd Record", 
                MB_OK ); 
            } 
            else 
            { 
                MessageBox( hwnd, 
                    "This device doesn't record.", 
                    "MCIWnd Record", 
                    MB_OK ); 
            } 
            break; 
        case IDM_RECORDATSTART: 
            if( MCIWndCanRecord(g_hwndMCIWnd) ) 
            { 
                MCIWndHome(g_hwndMCIWnd); 
                MCIWndRecord(g_hwndMCIWnd); 
            } 
            else 
            { 
                MessageBox( hwnd, 
                    "This device doesn't record.", 
                    "MCIWnd Record", 
                    MB_OK); 
            } 
            break; 
        case IDM_RECORDATEND: 
            if( MCIWndCanRecord(g_hwndMCIWnd) ) 
            { 
                MCIWndEnd(g_hwndMCIWnd); 
                MCIWndRecord(g_hwndMCIWnd); 
            } 
            else 
            { 
                MessageBox( hwnd, 
                    "This device doesn't record.", 
                    "MCIWnd Record", 
                    MB_OK); 
            } 
            break; 
        case IDM_SAVEMCIWND: 
            if( MCIWndCanSave(g_hwndMCIWnd) ) 
                MCIWndSaveDialog(g_hwndMCIWnd); 
    } 
    break; 
 
    // Handle other messages here. 
```



 

 




