---
title: Pausar y reanudar la reproducción
description: Pausar y reanudar la reproducción
ms.assetid: f5a7ef22-993c-4aab-bab0-2700289da7a7
keywords:
- Macro MCIWndPause
- Macro MCIWndResume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce70a95000cda6fc471967e5075b16fe7bad837c71eed4e6216ddeaddddc4508
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119805975"
---
# <a name="pausing-and-resuming-playback"></a>Pausar y reanudar la reproducción

Puede interrumpir la reproducción de un dispositivo o archivo asociado a una ventana de MCIWnd mediante la macro [**MCIWndPause.**](/windows/desktop/api/Vfw/nf-vfw-mciwndpause) A continuación, puede reiniciar la reproducción mediante la macro [**MCIWndResume.**](/windows/desktop/api/Vfw/nf-vfw-mciwndresume) Si el dispositivo no admite la reanudación o si se produce un error, puede usar la macro [**MCIWndPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndplay) para reiniciar la reproducción.

En el ejemplo siguiente se crea una ventana MCIWnd y se reproduce un archivo AVI. Los comandos de menú Pausar y reanudar están disponibles para que el usuario interrumpa y reinicie la reproducción.

Los estilos de ventana de MCIWnd se cambian temporalmente mediante la macro [**MCIWndChangeStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles) para impedir que se muestre un cuadro de diálogo de error de MCI si se produce un error en [**MCIWndResume.**](/windows/desktop/api/Vfw/nf-vfw-mciwndresume)


```C++
case WM_COMMAND: 
    switch (wParam) 
    { 
        case IDM_CREATEMCIWND:             // creates and plays clip 
            g_hwndMCIWnd = MCIWndCreate(hwnd,  
                g_hinst,                      
                WS_CHILD | WS_VISIBLE |    // standard styles
                MCIWNDF_NOPLAYBAR |        // hides toolbar 
                MCIWNDF_NOTIFYMODE,        // notifies of mode changes
                "sample.avi"); 
 
            MCIWndPlay(g_hwndMCIWnd); 
            break;    
        case IDM_PAUSEMCIWND:              // pauses playback 
            MCIWndPause(g_hwndMCIWnd); 
            MessageBox(hwnd, "MCIWnd", "Pausing Playback", MB_OK); 
            break; 
        case IDM_RESUMEMCIWND:          // resumes playback 
            MCIWndChangeStyles(      // hides error dialog messages
                g_hwndMCIWnd,        // MCIWnd window
                MCIWNDF_NOERRORDLG,  // mask of style to change
                MCIWNDF_NOERRORDLG); // suppresses MCI error dialogs 
 
            lResult = MCIWndResume(g_hwndMCIWnd); 
 
            if(lResult){                   // device doesn't resume 
                MessageBox(hwnd, "MCIWnd", 
                    "Resume with Stop and Play", MB_OK); 
                MCIWndStop(g_hwndMCIWnd); 
                MCIWndPlay(g_hwndMCIWnd); 
 
                MCIWndChangeStyles(        // resumes original styles
                    g_hwndMCIWnd, 
                    MCIWNDF_NOERRORDLG, 
                    NULL); 
        } 
        break; 
    } 
    break; 
 
// Handle other messages here. 
```



 

 




