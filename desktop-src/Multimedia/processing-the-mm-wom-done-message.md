---
title: Procesamiento del MM_WOM_DONE mensaje
description: Procesamiento del mensaje \_ DE MM WOM \_ DONE
ms.assetid: 215167d0-3020-453d-b6b3-cee5803836c9
keywords:
- audio de forma de onda, mensajes
- audio auxiliar, mensajes
- audio de forma de onda, MM_WOM_DONE mensaje
- audio auxiliar, MM_WOM_DONE mensaje
- MM_WOM_DONE mensaje
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73e909777c115b6b10500e081a08bde6cfe24b00
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169545"
---
# <a name="processing-the-mm_wom_done-message"></a>Procesamiento del mensaje \_ DE MM WOM \_ DONE

En el ejemplo siguiente se muestra cómo procesar el [**mensaje \_ MM WOM \_ DONE.**](mm-wom-done.md) En este ejemplo se supone que la aplicación no reproduce varios bloques de datos, por lo que puede cerrar el dispositivo de salida después de reproducir un único bloque de datos.


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



 

 




