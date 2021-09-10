---
title: Determinar el formato de salida de un resalte
description: Determinar el formato de salida de un resalte
ms.assetid: 910bd77f-4c65-4ea2-bab2-96f42a2b6cf1
keywords:
- Administrador de compresión de vídeo (VCM), formato de salida
- VCM (administrador de compresión de vídeo), formato de salida
- Macro ICCompressGetFormat
- Macro ICCompressQuery
- Macro ICCompressGetSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c4356870598dc08ad84c4073be5ffa3c2ddbd5b
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370387"
---
# <a name="determining-a-compressors-output-format"></a>Determinar el formato de salida de un resalte

En el ejemplo siguiente se usa la macro de tamaño [**ICCompressGetFormat**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetformat) para determinar el tamaño de búfer necesario para los datos que especifican el formato de compresión, asigna un búfer del tamaño adecuado mediante la función [GlobalAlloc](/windows/win32/api/winbase/nf-winbase-globalalloc) y recupera la información de formato de compresión mediante la macro **ICCompressGetFormat.**


```C++
LPBITMAPINFOHEADER   lpbiIn, lpbiOut; 
 
// *lpbiIn must be initialized to the input format. 
 
dwFormatSize = ICCompressGetFormatSize(hIC, lpbiIn); 
h = GlobalAlloc(GHND, dwFormatSize); 
lpbiOut = (LPBITMAPINFOHEADER)GlobalLock(h); 
ICCompressGetFormat(hIC, lpbiIn, lpbiOut); 
 
```



En el ejemplo siguiente se usa la macro [**ICCompressQuery**](/windows/desktop/api/Vfw/nf-vfw-iccompressquery) para determinar si un asete puede controlar los formatos de entrada y salida.


```C++
LPBITMAPINFOHEADER   lpbiIn, lpbiOut; 
 
// Both *lpbiIn and *lpbiOut must be initialized to the respective
// formats.
 

if (ICCompressQuery(hIC, lpbiIn, lpbiOut) == ICERR_OK)
{ 
 
    // Format is supported; use the compressor. 
 
}
 
 
```



En el ejemplo siguiente se usa la macro [**ICCompressGetSize**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetsize) para determinar el tamaño del búfer y se asigna un búfer de ese tamaño mediante [GlobalAlloc](/windows/win32/api/winbase/nf-winbase-globalalloc).


```C++
// Find the worst-case buffer size. 
dwCompressBufferSize = ICCompressGetSize(hIC, lpbiIn, lpbiOut); 
 
// Allocate a buffer and get lpOutput to point to it. 
h = GlobalAlloc(GHND, dwCompressBufferSize); 
lpOutput = (LPVOID)GlobalLock(h);
 
 
```



 

 