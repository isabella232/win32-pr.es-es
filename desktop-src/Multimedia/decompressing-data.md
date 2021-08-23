---
title: Descompresión de datos
description: Descompresión de datos
ms.assetid: 1faf0238-7bef-4363-9bbc-44737600c946
keywords:
- Administrador de compresión de vídeo (VCM), descomprimir datos
- VCM (administrador de compresión de vídeo), descompresión de datos
- ICDecompressBegin macro
- Función ICDecompress
- MACRO ICDecompressEnd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a213a4d4762f782da817773aac6e8838155561ae47129dd998dad7a82ac5a4f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119785435"
---
# <a name="decompressing-data"></a>Descompresión de datos

En el ejemplo siguiente se muestra cómo una aplicación puede inicializar un descomprimidor mediante la macro [**ICDecompressBegin,**](/windows/desktop/api/Vfw/nf-vfw-icdecompressbegin) descomprimir una secuencia de fotogramas mediante la función [**ICDecompress**](/windows/desktop/api/Vfw/nf-vfw-icdecompress) y finalizar la descompresión mediante la macro [**ICDecompressEnd.**](/windows/desktop/api/Vfw/nf-vfw-icdecompressend)


```C++
LPBITMAPINFOHEADER lbpiIn, lpbiOut; 
LPVOID             lpIn, lpOut; 
LONG               lNumFrames, lFrameNum; 
 
// Assume lpbiIn and lpbiOut are initialized to the input and output 
// format and lpIn and lpOut are pointing to the buffers. 
if (ICDecompressBegin(hIC, lpbiIn, lpbiOut) == ICERR_OK)
{ 
    for (lFrameNum = 0; lFrameNum < lNumFrames, lFrameNum++)
    { 
        if (ICDecompress(hIC, 0, lpbiIn, lpIn, lpbiOut, 
            lpOut) == ICERR_OK) 
        { 
            // Frame decompressed OK so we can process it as required. 
        } 
        else 
        { 
            // Handle the decompression error that occurred. 
        } 
    } 
    ICDecompressEnd(hIC); 
} 
else 
{ 
    // Handle the error identifying an unsupported format. 
} 
 
```



 

 




