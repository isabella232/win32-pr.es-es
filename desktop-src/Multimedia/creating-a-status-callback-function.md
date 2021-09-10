---
title: Crear una función de devolución de llamada de estado
description: Crear una función de devolución de llamada de estado
ms.assetid: 9aa98340-a5a0-4084-9670-b3c27a1351ed
keywords:
- CapSetCallbackOnStatus macro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 592a5582bca37f644810f3496a39321d22da43be
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371366"
---
# <a name="creating-a-status-callback-function"></a>Crear una función de devolución de llamada de estado

El ejemplo siguiente es una función de devolución de llamada de estado simple. Registre esta devolución de llamada mediante la [**macro capSetCallbackOnStatus.**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonstatus)


```C++
TCHAR gachAppName[] = TEXT("Application Name");  // Application name.
TCHAR gachBuffer[100];  // Global buffer.

// StatusCallbackProc: status callback function. 
// hWnd:               capture window handle. 
// nID:                status code for the current status. 
// lpStatusText:       status text string for the current status. 
// 
LRESULT PASCAL StatusCallbackProc(HWND hWnd, int nID, 
    LPTSTR lpStatusText) 
{ 
    if (!hWnd) 
        return FALSE; 
 
    if (nID == 0) {
        // Clear old status messages.
        SetWindowText(hWnd, gachAppName); 
        return (LRESULT) TRUE; 
    } 
    // Show the status ID and status text. 
    _stprintf_s(gachBuffer, TEXT("Status# %d: %s"), nID, lpStatusText); 
 
    SetWindowText(hWnd, gachBuffer); 
    return (LRESULT) TRUE; 
} 
 
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de captura de vídeo](using-video-capture.md)
</dt> </dl>

 

 




