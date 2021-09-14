---
title: Automatización de la reproducción para MCIWnd
description: Automatización de la reproducción para MCIWnd
ms.assetid: 7e38e8b1-f56d-4008-83a7-4fba8333e328
keywords:
- MCIWndCreate macro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b9224cfa4f5a93488f226d1aefa83201b8b0637
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062961"
---
# <a name="automating-playback-for-mciwnd"></a>Automatización de la reproducción para MCIWnd

Puede automatizar la reproducción de MCIWnd especificando determinados estilos de ventana en la [**función MCIWndCreate.**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) Para reproducir el dispositivo, la ventana necesita una ventana primaria para procesar mensajes de notificación, un área de reproducción para reproducir archivos AVI y la notificación de cambios en el modo de dispositivo para identificar cuándo se detiene la reproducción. La ventana no necesita una barra de herramientas. Puede establecer estas características especificando los estilos adecuados en **MCIWndCreate**.

En el ejemplo siguiente se usan comandos de menú para crear una ventana MCIWnd para reproducir contenido de varios tipos diferentes de dispositivos. La **función MCIWndCreate** crea la ventana MCIWnd y los dispositivos y archivos se cargan mediante la macro [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen) en los comandos específicos del dispositivo. Cuando un dispositivo termina de reproducirse, cierra el dispositivo capturando el mensaje [**MCIWNDM \_ NOTIFYMODE**](mciwndm-notifymode.md) y emitiendo la macro [**MCIWndClose.**](/windows/desktop/api/Vfw/nf-vfw-mciwndclose)


```C++
case WM_COMMAND: 
    switch (wParam) 
    { 
        case IDM_CREATEMCIWND: 
            dwMCIWndStyle = WS_CHILD |     // child window
                WS_VISIBLE |               // visible
                MCIWNDF_NOTIFYMODE |       // notifies of mode changes
                MCIWNDF_NOPLAYBAR;            // hides toolbar 
            g_hwndMCIWnd = MCIWndCreate(hwnd, 
                g_hinst, dwMCIWndStyle, NULL); 
            break; 
        case IDM_PLAYCDA: 
            LoadNGoMCIWnd(hwnd, "CDAudio"); 
            break; 
        case IDM_PLAYWAVE: 
            LoadNGoMCIWnd(hwnd, "SoundWave.WAV"); 
            break; 
        case IDM_PLAYMIDI: 
            LoadNGoMCIWnd(hwnd, "MIDIFile.MID"); 
            break; 
        case IDM_PLAYAVI: 
            LoadNGoMCIWnd(hwnd, "AVIFile.AVI"); 
            break; 
        case IDM_EXIT: 
            MCIWndDestroy(g_hwndMCIWnd); 
            DestroyWindow(hwnd); 
            break; 
    } 
    break; 
 
case MCIWNDM_NOTIFYMODE: 
    if (lParam == MCI_MODE_STOP)  // device stopped
    { 
        MessageBox(hwnd,"","Closing Device",MB_OK); 
        MCIWndClose(g_hwndMCIWnd); 
    } 
    break; 

// Handle other messages here. 
 
// LoadNGoMCIWnd - automatically loads and plays a multimedia device 
// 
// hwnd -  handle to the parent window 
// lpstr - pointer to device or filename played by device 
// 
// Global variable 
// extern HINSTANCE g_hwndMCIWnd;  instance handle to MCIWnd window 
 
VOID LoadNGoMCIWnd(HWND hwnd, LPSTR lpstr) 
{ 
    MessageBox(hwnd, lpstr, "Loading Device", MB_OK); 
    MCIWndOpen(g_hwndMCIWnd, lpstr, NULL);   // new device in window 
    MCIWndPlay(g_hwndMCIWnd);                // plays device 
} 
```



 

 




