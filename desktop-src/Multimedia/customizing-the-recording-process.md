---
title: Personalización del proceso de grabación
description: Personalización del proceso de grabación
ms.assetid: 9453b9d3-ae9c-4f57-8dd6-f84b9a76618e
keywords:
- MCIWndCreate función)
- MCIWndNew (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec46f61ef4624ba613025f01b081ccc1ebda1cad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994202"
---
# <a name="customizing-the-recording-process"></a><span data-ttu-id="e3646-105">Personalización del proceso de grabación</span><span class="sxs-lookup"><span data-stu-id="e3646-105">Customizing the Recording Process</span></span>

<span data-ttu-id="e3646-106">Puede personalizar el proceso de grabación y tomar el control completo de la mayor parte de la creación de la ventana de MCIWnd para guardar la información grabada en un archivo.</span><span class="sxs-lookup"><span data-stu-id="e3646-106">You can customize the recording process, taking complete control of most everything — from creating the MCIWnd window to saving the recorded information in a file.</span></span> <span data-ttu-id="e3646-107">En el ejemplo siguiente se consulta el dispositivo MCI para grabar y guardar funciones, e incluye comandos de menú para grabar al principio o al final del contenido.</span><span class="sxs-lookup"><span data-stu-id="e3646-107">The following example queries the MCI device for recording and saving capabilities, and includes menu commands to record at the beginning or end of the content.</span></span>

<span data-ttu-id="e3646-108">En el ejemplo siguiente se usa la función [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) para crear una nueva ventana y le permite especificar un archivo existente para almacenar los datos grabados y la macro [**MCIWndNew**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew) para asociar un nuevo archivo a la ventana.</span><span class="sxs-lookup"><span data-stu-id="e3646-108">The following example uses the [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) function to create a new window and allows you to specify an existing file to store the recorded data and the [**MCIWndNew**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew) macro to associate a new file with the window.</span></span> <span data-ttu-id="e3646-109">Como alternativa, puede usar la macro [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen) o [**MCIWndOpenDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndopendialog) para especificar un archivo.</span><span class="sxs-lookup"><span data-stu-id="e3646-109">Alternatively, you can use the [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen) or [**MCIWndOpenDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndopendialog) macro to specify a file.</span></span>

<span data-ttu-id="e3646-110">En el ejemplo se usa la macro [**MCIWndCanRecord**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanrecord) para comprobar que el dispositivo puede grabar y la macro [**MCIWndCanSave**](/windows/desktop/api/Vfw/nf-vfw-mciwndcansave) para comprobar que el dispositivo guarda información.</span><span class="sxs-lookup"><span data-stu-id="e3646-110">The example uses the [**MCIWndCanRecord**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanrecord) macro to verify that the device can record and the [**MCIWndCanSave**](/windows/desktop/api/Vfw/nf-vfw-mciwndcansave) macro to verify that the device save information.</span></span> <span data-ttu-id="e3646-111">En el ejemplo se establece la posición de reproducción actual mediante el uso de las macros [**MCIWndHome**](/windows/desktop/api/Vfw/nf-vfw-mciwndhome) y [**MCIWndEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndend) .</span><span class="sxs-lookup"><span data-stu-id="e3646-111">The example sets the current playback position by using the [**MCIWndHome**](/windows/desktop/api/Vfw/nf-vfw-mciwndhome) and [**MCIWndEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndend) macros.</span></span> <span data-ttu-id="e3646-112">En el ejemplo se inicia la grabación mediante la macro [**MCIWndRecord**](/windows/desktop/api/Vfw/nf-vfw-mciwndrecord) .</span><span class="sxs-lookup"><span data-stu-id="e3646-112">The example starts recording by using the [**MCIWndRecord**](/windows/desktop/api/Vfw/nf-vfw-mciwndrecord) macro.</span></span> <span data-ttu-id="e3646-113">Una vez registrada la información, el ejemplo la guarda mediante la macro [**MCIWndSaveDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndsavedialog) .</span><span class="sxs-lookup"><span data-stu-id="e3646-113">After the information is recorded, the example saves it by using the [**MCIWndSaveDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndsavedialog) macro.</span></span>


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



 

 




