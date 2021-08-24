---
title: Determinar el formato de salida de un descomprimidor
description: Determinar el formato de salida de un descomprimidor
ms.assetid: afedef5e-a506-40bd-aaad-fd85b0468ed7
keywords:
- Administrador de compresión de vídeo (VCM), formato de salida
- VCM (administrador de compresión de vídeo), formato de salida
- Macro ICDecompressGetFormatSize
- Macro ICDecompressQuery
- Macro ICDecompressGetPalette
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cc17db0d7aa015c955825840fb70d12714be3c0a44a69bf5abc59290ebc633c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119497425"
---
# <a name="determining-a-decompressors-output-format"></a>Determinar el formato de salida de un descomprimidor

En el ejemplo siguiente se determina el tamaño de búfer necesario para los datos que especifican el formato de descompresión mediante la macro [**ICDecompressGetFormatSize,**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformatsize) se asigna un búfer del tamaño adecuado mediante la función [GlobalAlloc](/windows/win32/api/winbase/nf-winbase-globalalloc) y se recupera la información de formato de descompresión mediante la macro [**ICDecompressGetFormat.**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformat)


```C++
LPBITMAPINFOHEADER lpbiIn, lpbiOut; 
 
// Assume *lpbiIn points to the input (compressed) format. 
dwFormatSize = ICDecompressGetFormatSize(hIC, lpbiIn); 
h = GlobalAlloc(GHND, dwFormatSize); 
lpbiOut = (LPBITMAPINFOHEADER)GlobalLock(h); 
ICDecompressGetFormat(hIC, lpbiIn, lpbiOut); 
 
```



En el ejemplo siguiente se muestra cómo una aplicación puede usar la macro [**ICDecompressQuery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressquery) para determinar si un descomprimidor puede controlar los formatos de entrada y salida.


```C++
LPBITMAPINFOHEADER lpbiIn, lpbiOut; 
// Assume *lpbiIn & *lpbiOut are initialized to the respective 
// formats.
 
if (ICDecompressQuery(hIC, lpbiIn, lpbiOut) == ICERR_OK)
{ 
    
    // Format is supported - use the decompressor. 
    
} 
 
```



El fragmento de código siguiente muestra cómo obtener la información de la paleta mediante la macro [**ICDecompressGetPalette.**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetpalette)


```C++
ICDecompressGetPalette(hIC, lpbiIn, lpbiOut); 
 
// Move up to the palette. 
lpPalette = (LPBYTE)lpbiOut + lpbi->biSize;
 
 
```



 

 