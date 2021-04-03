---
title: Crear una función de devolución de llamada de estado
description: Crear una función de devolución de llamada de estado
ms.assetid: 9aa98340-a5a0-4084-9670-b3c27a1351ed
keywords:
- capSetCallbackOnStatus (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 592a5582bca37f644810f3496a39321d22da43be
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075445"
---
# <a name="creating-a-status-callback-function"></a><span data-ttu-id="3431c-104">Crear una función de devolución de llamada de estado</span><span class="sxs-lookup"><span data-stu-id="3431c-104">Creating a Status Callback Function</span></span>

<span data-ttu-id="3431c-105">El ejemplo siguiente es una función de devolución de llamada de estado simple.</span><span class="sxs-lookup"><span data-stu-id="3431c-105">The following example is a simple status callback function.</span></span> <span data-ttu-id="3431c-106">Registre esta devolución de llamada mediante la macro [**capSetCallbackOnStatus**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonstatus) .</span><span class="sxs-lookup"><span data-stu-id="3431c-106">Register this callback by using the [**capSetCallbackOnStatus**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonstatus) macro.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="3431c-107">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3431c-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3431c-108">Uso de la captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="3431c-108">Using Video Capture</span></span>](using-video-capture.md)
</dt> </dl>

 

 




