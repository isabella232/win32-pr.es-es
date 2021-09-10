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
ms.openlocfilehash: de20d23c0ded51d1933918c16da3f8827b77f796
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370406"
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



 

 




