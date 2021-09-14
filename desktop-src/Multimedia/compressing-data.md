---
title: Comprimir datos
description: Comprimir datos
ms.assetid: b231316b-0c81-410a-b2fe-b58ab7aca02b
keywords:
- administrador de compresión de vídeo (VCM), comprimir datos
- VCM (administrador de compresión de vídeo), comprimir datos
- ICCompressBegin macro
- Función ICCompress
- Macro ICCompressEnd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0c08308b695bf022d2d2b76bda6727d9f9c1a9c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069547"
---
# <a name="compressing-data"></a>Comprimir datos

En el ejemplo siguiente se comprimen los datos de imagen para usarlos en un archivo AVI. Se da por supuesto que el resalte no admite las marcas TEMPORALES VIDCF CRUNCH o \_ VIDCF, pero sí admite \_ VIDCF \_ QUALITY. En el ejemplo se usa la macro [**ICCompressBegin,**](/windows/desktop/api/Vfw/nf-vfw-iccompressbegin) la [**función ICCompress**](/windows/desktop/api/Vfw/nf-vfw-iccompress) y la macro [**ICCompressEnd.**](/windows/desktop/api/Vfw/nf-vfw-iccompressend)


```C++
DWORD dwCkID; 
DWORD dwCompFlags; 
DWORD dwQuality; 
LONG  lNumFrames, lFrameNum; 
// Assume dwNumFrames is initialized to the total number of frames. 
// Assume dwQuality holds the proper quality value (0-10000). 
// Assume lpbiOut, lpOut, lpbiIn, and lpIn are initialized properly. 
 
// If OK to start, compress each frame. 
if (ICCompressBegin(hIC, lpbiIn, lpbiOut) == ICERR_OK)
{ 
    for ( lFrameNum = 0; lFrameNum < lNumFrames; lFrameNum++)
    { 
        if (ICCompress(hIC, 0, lpbiOut, lpOut, lpbiIn, lpIn, 
            &dwCkID, &dwCompFlags, lFrameNum, 
            0, dwQuality, NULL, NULL) == ICERR_OK)
        { 
            // Write compressed data to the AVI file. 
             
            // Set lpIn to the next frame in the sequence. 
             
        } 
        else 
        { 
            // Handle compressor error. 
        } 
    } 
    ICCompressEnd(hIC);    // terminate compression 
} 
else 
{ 
    // Handle the error identifying the unsupported format. 
} 
 
```



 

 




