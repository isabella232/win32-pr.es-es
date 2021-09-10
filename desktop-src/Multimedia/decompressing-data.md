---
title: Descompresión de datos
description: Descompresión de datos
ms.assetid: 1faf0238-7bef-4363-9bbc-44737600c946
keywords:
- Administrador de compresión de vídeo (VCM), descomprimir datos
- VCM (administrador de compresión de vídeo), descomprimir datos
- MACRO ICDecompressBegin
- Función ICDecompress
- Macro ICDecompressEnd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03b44ea375bb1f2b5c41a361ca7f31387439b610
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370381"
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



 

 




