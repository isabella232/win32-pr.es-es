---
title: Progreso del compresor y descompresor de supervisión
description: Progreso del compresor y descompresor de supervisión
ms.assetid: 7c87c688-75b6-4d3e-9dd5-5f509ff2e473
keywords:
- Administrador de compresión de vídeo (VCM), supervisión
- VCM (Administrador de compresión de vídeo), supervisar
- ICSetStatusProc función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beb86a40bb653380dc93e758ada1b2eef6ec9ca7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075601"
---
# <a name="monitoring-compressor-and-decompressor-progress"></a>Progreso del compresor y descompresor de supervisión

En el ejemplo siguiente se muestra cómo se usa la función [**ICSetStatusProc**](/windows/desktop/api/Vfw/nf-vfw-icsetstatusproc) para informar al compresor o descompresor de la dirección de la función de devolución de llamada:


```C++
ICSetStatusProc(compvars.hic, 0, (LPARAM) (UINT) hwndApp, 
    &PreviewStatusProc); 
 
```



En el ejemplo siguiente se muestra la función de devolución de llamada instalada por el fragmento anterior:


```C++
LONG CALLBACK export PreviewStatusProc(LPARAM lParam, 
    UINT message, LONG l) 
{ 
    switch (message) 
    { 
        MSG msg; 
        case ICSTATUS_START: 
         
        // Create and display status dialog box. 
         
            break; 
        case ICSTATUS_STATUS: 
            ProSetBarPos((int) l); // sets status bar positions 
 
        // Watch for abort message 
            while(PeekMessage(&msg, NULL, 0, 0, PM_REMOVE)) 
            { 
                if (msg.message == WM_KEYDOWN && msg.wParam == 
                    VK_ESCAPE) 
                    return 1; 
                if (msg.message == WM_SYSCOMMAND && 
                    (msg.wParam & 0xFFF0) == SC_CLOSE) 
                    return 1; 
 
                TranslateMessage(&msg); 
                DispatchMessage(&msg); 
            } 
            break; 
        case ICSTATUS_END: 
         
        // Close and destroy status dialog box. 
         
            break; 
        case ICSTATUS_YIELD: 
         
         
         
            break; 
    } 
    return 0; 
} 
 
```



 

 




