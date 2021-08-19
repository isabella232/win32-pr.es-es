---
title: Dibujar datos
description: Dibujar datos
ms.assetid: cc4f383d-54d4-4027-ad6a-da19bb07c17f
keywords:
- administrador de compresión de vídeo (VCM), dibujo
- VCM (administrador de compresión de vídeo), dibujo
- Función ICDraw
- Macro ICDrawStart
- Macro ICDrawStop
- Macro ICDrawFlush
- Macro ICDrawEnd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dcbb9f0c9c39da17c4f60af3dfb9c3a7e0179ebf4c8ed6e5bcac4cdc6f24828
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119496715"
---
# <a name="drawing-data"></a>Dibujar datos

En el ejemplo siguiente se usa la [**función ICDraw**](/windows/desktop/api/Vfw/nf-vfw-icdraw) y las macros [**ICDrawStart**](/windows/desktop/api/Vfw/nf-vfw-icdrawstart), [**ICDrawStop,**](/windows/desktop/api/Vfw/nf-vfw-icdrawstop) [**ICDrawFlush**](/windows/desktop/api/Vfw/nf-vfw-icdrawflush)y [**ICDrawEnd**](/windows/desktop/api/Vfw/nf-vfw-icdrawend) para dibujar datos en la pantalla.


```C++
DWORD    dwNumBuffers; 
 
// Find out how many buffers need filling before drawing starts.

ICGetBuffersWanted(hIC, &dwNumBuffers); 
for (dw = 0; dw < dwNumBuffers; dw++)
{ 
    ICDraw(hIC, 0, lpFormat, lpData, cbData, dw); // fill the pipeline
    
    // Point lpFormat and lpData to next format and buffer.
    
} 
ICDrawStart(hIC);  // starts the clock 
dw = 0; 
while (fPlaying) 
{ 
    ICDraw(hIC, 0, lpFormat, lpData, chData, dw); // fill more buffers 
    
    // Point lpFormat and lpData to next format and buffer,
    // update dw.
} 
 
ICDrawStop(hIC);   // stops drawing and decompressing when done 
ICDrawFlush(hIC);  // flushes any existing buffers 
ICDrawEnd(hIC);    // ends decompression 
 
```



 

 




