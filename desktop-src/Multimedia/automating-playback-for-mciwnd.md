---
title: Automatizar la reproducción de MCIWnd
description: Automatizar la reproducción de MCIWnd
ms.assetid: 7e38e8b1-f56d-4008-83a7-4fba8333e328
keywords:
- MCIWndCreate (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b9224cfa4f5a93488f226d1aefa83201b8b0637
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357637"
---
# <a name="automating-playback-for-mciwnd"></a><span data-ttu-id="6968f-104">Automatizar la reproducción de MCIWnd</span><span class="sxs-lookup"><span data-stu-id="6968f-104">Automating Playback for MCIWnd</span></span>

<span data-ttu-id="6968f-105">Puede automatizar la reproducción de MCIWnd especificando ciertos estilos de ventana en la función [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) .</span><span class="sxs-lookup"><span data-stu-id="6968f-105">You can automate playback for MCIWnd by specifying certain window styles in the [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) function.</span></span> <span data-ttu-id="6968f-106">Para reproducir el dispositivo, la ventana necesita una ventana primaria para procesar los mensajes de notificación, un área de reproducción para reproducir archivos AVI y la notificación de los cambios en el modo de dispositivo para identificar cuándo se detiene la reproducción.</span><span class="sxs-lookup"><span data-stu-id="6968f-106">To play the device, the window needs a parent window to process notification messages, a playback area to play AVI files, and notification of device mode changes to identify when playback stops.</span></span> <span data-ttu-id="6968f-107">La ventana no necesita una barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="6968f-107">The window does not need a toolbar.</span></span> <span data-ttu-id="6968f-108">Puede establecer estas características especificando los estilos correspondientes en **MCIWndCreate**.</span><span class="sxs-lookup"><span data-stu-id="6968f-108">You can set these characteristics by specifying the appropriate styles in **MCIWndCreate**.</span></span>

<span data-ttu-id="6968f-109">En el ejemplo siguiente se usan comandos de menú para crear una ventana de MCIWnd para reproducir contenido de varios tipos diferentes de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="6968f-109">The following example uses menu commands to create an MCIWnd window to play content from several different types of devices.</span></span> <span data-ttu-id="6968f-110">La función **MCIWndCreate** crea la ventana MCIWnd, y los dispositivos y archivos se cargan mediante la macro [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen) en los comandos específicos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6968f-110">The **MCIWndCreate** function creates the MCIWnd window, and devices and files are loaded by using the [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen) macro in the device-specific commands.</span></span> <span data-ttu-id="6968f-111">Cuando un dispositivo termina de reproducirse, el dispositivo se cierra interceptando el mensaje [**\_ NOTIFYMODE de MCIWNDM**](mciwndm-notifymode.md) y emitiendo la macro [**MCIWndClose**](/windows/desktop/api/Vfw/nf-vfw-mciwndclose) .</span><span class="sxs-lookup"><span data-stu-id="6968f-111">When a device finishes playing, you close the device by trapping the [**MCIWNDM\_NOTIFYMODE**](mciwndm-notifymode.md) message and issuing the [**MCIWndClose**](/windows/desktop/api/Vfw/nf-vfw-mciwndclose) macro.</span></span>


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



 

 




