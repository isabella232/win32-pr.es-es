---
title: Preparación para dibujar datos
description: Preparación para dibujar datos
ms.assetid: 98adcee4-06c0-4684-bd9e-e030e3f9a59d
keywords:
- administrador de compresión de vídeo (VCM), dibujo
- VCM (administrador de compresión de vídeo), dibujo
- Macro ICDrawBegin
- Macro ICDrawEnd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c32c87c751705dea6dc6e00c2f48635d685d87f7d900422efb980b22012e052e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037905"
---
# <a name="preparing-to-draw-data"></a>Preparación para dibujar datos

En el ejemplo siguiente se muestra la secuencia de inicialización que indica al descomprimidor que dibuje a pantalla completa. Usa las macros [**ICDrawBegin**](/windows/desktop/api/Vfw/nf-vfw-icdrawbegin) [**e ICDrawEnd.**](/windows/desktop/api/Vfw/nf-vfw-icdrawend)


```C++
// Assume lpbiIn has the input format, dwRate has the data rate. 

if (ICDrawBegin(hIC, ICDRAW_QUERY | ICDRAW_FULLSCREEN, NULL, NULL, 
    NULL, 0, 0, 0, 0, lpbiIn, 0, 0, 0, 0, dwRate, 
    dwScale) == ICERR_OK) 
{ 
    // Decompressor supports this drawing so set up to draw. 
    ICDrawBegin(hIC, ICDRAW_FULLSCREEN, hPal, NULL, NULL, 0, 0, 0, 
        0, lpbiIn, 0, 0, lbpi->biWidth, lpbi->biHeight, dwRate, 
        dwScale); 
    . 
    . // Start decompressing and drawing frames. 
    . 
 
    // Drawing done. Terminate procedure. 
    ICDrawEnd(hIC); 
} 
else 
{ 
    
    // Use another renderer to draw data on the screen; 
    // ICDraw does not support the format. 
} 
 
```



 

 




