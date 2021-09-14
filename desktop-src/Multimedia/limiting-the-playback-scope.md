---
title: Limitar el ámbito de reproducción
description: Limitar el ámbito de reproducción
ms.assetid: 080ab96f-1cb5-48d4-ac0a-8fd9ba68a31a
keywords:
- Macro MCIWndPlayFrom
- Macro MCIWndPlayTo
- Macro MCIWndPlayFromTo
- Comandos de reproducción de MCI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 465bcf7a7b6b5811de8413a1c89f7befcf81037f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127246110"
---
# <a name="limiting-the-playback-scope"></a>Limitar el ámbito de reproducción

El control de la reproducción comienza con la macro [**MCIWndPlay,**](/windows/desktop/api/Vfw/nf-vfw-mciwndplay) que reproduce el contenido o archivo asociado a una ventana de MCIWnd desde la posición de reproducción actual hasta el final del contenido. Si desea limitar la reproducción a una parte específica del contenido o archivo, puede elegir entre las otras macros MCIWnd de reproducción: [**MCIWndPlayFrom**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfrom), [**MCIWndPlayTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto)y [**MCIWndPlayFromTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto).

También debe establecer un formato de hora adecuado. El formato de hora determina si el contenido se mide en fotogramas, milisegundos, pistas u otras unidades.

En el ejemplo siguiente se crea una ventana de MCIWnd y se proporcionan comandos de menú para reproducir el último tercero, primer tercero o tercer medio del contenido. Estos comandos de menú usan **MCIWndPlayFrom,** **MCIWndPlayTo** y **MCIWndPlayFromTo** para reproducir los segmentos de contenido. En el ejemplo también se usan las macros [**MCIWndGetStart**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstart) y [**MCIWndGetEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend) para identificar el principio y el final del contenido, y se usa la macro [**MCIWndHome**](/windows/desktop/api/Vfw/nf-vfw-mciwndhome) para mover la posición de reproducción al principio del contenido.

La función [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) usa los estilos WS CAPTION y MCIWNDF SHOWALL además de los estilos de ventana estándar para mostrar el nombre de archivo, el modo y la posición de reproducción actual en la barra de título de la \_ \_ ventana MCIWnd.


```C++
case WM_COMMAND: 
    switch (wParam) 
    { 
        case IDM_CREATEMCIWND: 
            g_hwndMCIWnd = MCIWndCreate(hwnd, 
                g_hinst, 
                WS_CHILD | WS_VISIBLE | WS_CAPTION | 
                MCIWNDF_SHOWALL, 
                "sample.avi"); 
            break;
        case IDM_PLAYFROM:                // plays last third of clip 
            MCIWndUseTime(g_hwndMCIWnd);  // millisecond format 
 
        // Get media start and end positions. 
            lStart = MCIWndGetStart(g_hwndMCIWnd); 
            lEnd = MCIWndGetEnd(g_hwndMCIWnd); 
 
        // Determine playback end position. 
            lPlayStart = 2 * (lEnd - lStart) / 3 + lStart; 
 
            MCIWndPlayFrom(g_hwndMCIWnd, lPlayStart); 
            break; 
        case IDM_PLAYTO:                  // plays first third of clip 
            MCIWndUseTime(g_hwndMCIWnd);  // millisecond format 
 
        // Get media start and end positions. 
            lStart = MCIWndGetStart(g_hwndMCIWnd); 
            lEnd = MCIWndGetEnd(g_hwndMCIWnd); 
 
        // Determine playback start position. 
            lPlayEnd = (lEnd - lStart) / 3 + lStart;
 
            MCIWndHome(g_hwndMCIWnd); 
            MCIWndPlayTo(g_hwndMCIWnd, lPlayEnd); 
            break; 
        case IDM_PLAYSOME:               // plays middle third of clip 
            MCIWndUseTime(g_hwndMCIWnd); // millisecond format 
 
        // Get media start and end positions. 
            lStart = MCIWndGetStart(g_hwndMCIWnd); 
            lEnd = MCIWndGetEnd(g_hwndMCIWnd); 
 
        // Determine playback start and end positions. 
            lPlayStart = (lEnd - lStart) / 3 + lStart;
            lPlayEnd = 2 * (lEnd - lStart) / 3 + lStart; 
 
            MCIWndPlayFromTo(g_hwndMCIWnd, lPlayStart, lPlayEnd); 
            break; 
    
    // Handle other commands here. 
    } 
```



 

 




