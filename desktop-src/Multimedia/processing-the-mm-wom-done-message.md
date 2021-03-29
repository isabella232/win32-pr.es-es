---
title: Procesar el mensaje de MM_WOM_DONE
description: Procesamiento del \_ mensaje mm WOM \_ Done
ms.assetid: 215167d0-3020-453d-b6b3-cee5803836c9
keywords:
- audio de una onda, mensajes
- audio auxiliar, mensajes
- audio de una onda, MM_WOM_DONE mensaje
- audio auxiliar, mensaje de MM_WOM_DONE
- Mensaje MM_WOM_DONE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73e909777c115b6b10500e081a08bde6cfe24b00
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486787"
---
# <a name="processing-the-mm_wom_done-message"></a><span data-ttu-id="29964-108">Procesamiento del \_ mensaje mm WOM \_ Done</span><span class="sxs-lookup"><span data-stu-id="29964-108">Processing the MM\_WOM\_DONE Message</span></span>

<span data-ttu-id="29964-109">En el ejemplo siguiente se muestra cómo procesar el mensaje [**mm \_ WOM \_ Done**](mm-wom-done.md) .</span><span class="sxs-lookup"><span data-stu-id="29964-109">The following example shows how to process the [**MM\_WOM\_DONE**](mm-wom-done.md) message.</span></span> <span data-ttu-id="29964-110">En este ejemplo se da por supuesto que la aplicación no reproduce varios bloques de datos, por lo que puede cerrar el dispositivo de salida después de reproducir un único bloque de datos.</span><span class="sxs-lookup"><span data-stu-id="29964-110">This example assumes the application does not play multiple data blocks, so it can close the output device after playing a single data block.</span></span>


```C++
// WndProc--Main window procedure. 
LRESULT FAR PASCAL WndProc(HWND hWnd, UINT msg, WPARAM wParam, 
    LPARAM lParam) 
{ 
switch (msg) 
{ 
    case MM_WOM_DONE: 
 
    // A waveform-audio data block has been played and 
    // can now be freed. 
    waveOutUnprepareHeader((HWAVEOUT) wParam, 
        (LPWAVEHDR) lParam, sizeof(WAVEHDR) ); 
    
    // Free hData memory. 
    
    waveOutClose((HWAVEOUT) wParam); 
    break; 
    } 
    return DefWindowProc(hWnd, msg, wParam, lParam); 
} 
```



 

 




