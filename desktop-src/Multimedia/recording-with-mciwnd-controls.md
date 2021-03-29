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
# <a name="recording-with-mciwnd-controls"></a><span data-ttu-id="27acc-105">Grabar con controles MCIWnd</span><span class="sxs-lookup"><span data-stu-id="27acc-105">Recording with MCIWnd Controls</span></span>

<span data-ttu-id="27acc-106">En el ejemplo siguiente se registra el audio de una onda mediante los controles integrados de la ventana MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="27acc-106">The following example records waveform audio using the built-in controls of the MCIWnd window.</span></span> <span data-ttu-id="27acc-107">En el ejemplo se crea una ventana de MCIWnd mediante el \_ estilo de ventana registro MCIWNDF con la función [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) para agregar un botón **registro** a la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="27acc-107">The example creates an MCIWnd window by using the MCIWNDF\_RECORD window style with the [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) function to add a **Record** button to the toolbar.</span></span> <span data-ttu-id="27acc-108">La macro [**MCIWndNew**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew) indica que un nuevo archivo está asociado a la ventana de MCIWnd y que un dispositivo de audio de forma de onda proporcionará su contenido.</span><span class="sxs-lookup"><span data-stu-id="27acc-108">The [**MCIWndNew**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew) macro indicates a new file is associated with the MCIWnd window and that a waveform-audio device will provide its content.</span></span> <span data-ttu-id="27acc-109">Un segundo comando de menú, \_ SAVEMCIWND de IDM, permite al usuario guardar la grabación y seleccionar un nombre de archivo mediante la macro [**MCIWndSaveDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndsavedialog) .</span><span class="sxs-lookup"><span data-stu-id="27acc-109">A second menu command, IDM\_SAVEMCIWND, lets the user save the recording and select a filename by using the [**MCIWndSaveDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndsavedialog) macro.</span></span>


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



 

 




