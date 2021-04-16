---
title: Crear una función de devolución de llamada de fotograma
description: Crear una función de devolución de llamada de fotograma
ms.assetid: 37002ee0-9907-4aab-93cc-50fe9cd21cff
keywords:
- capSetCallbackOnFrame (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07b2a921bfae235c50387c41865c44bb69b5c05a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356925"
---
# <a name="creating-a-frame-callback-function"></a><span data-ttu-id="08f20-104">Crear una función de devolución de llamada de fotograma</span><span class="sxs-lookup"><span data-stu-id="08f20-104">Creating a Frame Callback Function</span></span>

<span data-ttu-id="08f20-105">El ejemplo siguiente es una función de devolución de llamada de fotograma simple.</span><span class="sxs-lookup"><span data-stu-id="08f20-105">The following example is a simple frame callback function.</span></span> <span data-ttu-id="08f20-106">Registre esta devolución de llamada mediante la macro [**capSetCallbackOnFrame**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonframe) .</span><span class="sxs-lookup"><span data-stu-id="08f20-106">Register this callback by using the [**capSetCallbackOnFrame**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonframe) macro.</span></span>


```
TCHAR gachBuffer[100];  // Global buffer.
DWORD gdwFrameNum = 0;

// FrameCallbackProc: frame callback function. 
// hWnd:              capture window handle. 
// lpVHdr:            pointer to structure containing captured 
//                        frame information. 
// 
LRESULT PASCAL FrameCallbackProc(HWND hWnd, LPVIDEOHDR lpVHdr) 
{ 
    if (!hWnd) 
        return FALSE; 
 
    _stprintf_s(gachBuffer, TEXT("Preview frame# %ld "), gdwFrameNum++); 
    SetWindowText(hWnd, gachBuffer); 
    return (LRESULT) TRUE ; 
} 
```



## <a name="related-topics"></a><span data-ttu-id="08f20-107">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="08f20-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08f20-108">Uso de la captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="08f20-108">Using Video Capture</span></span>](using-video-capture.md)
</dt> </dl>

 

 




