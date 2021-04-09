---
title: Determinar el formato de salida de un descompresor
description: Determinar el formato de salida de un descompresor
ms.assetid: afedef5e-a506-40bd-aaad-fd85b0468ed7
keywords:
- Administrador de compresión de vídeo (VCM), formato de salida
- VCM (Administrador de compresión de vídeo), formato de salida
- ICDecompressGetFormatSize (macro)
- ICDecompressQuery (macro)
- ICDecompressGetPalette (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fcb4140a4118cb2a36ccd75088556c53c55fdcb
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104149240"
---
# <a name="determining-a-decompressors-output-format"></a>Determinar el formato de salida de un descompresor

En el ejemplo siguiente se determina el tamaño de búfer necesario para los datos que especifican el formato de descompresión mediante la macro [**ICDecompressGetFormatSize**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformatsize) , se asigna un búfer del tamaño adecuado mediante la función [GlobalAlloc](/windows/win32/api/winbase/nf-winbase-globalalloc) y se recupera la información de formato de descompresión mediante la macro [**ICDecompressGetFormat**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformat) .


```C++
LPBITMAPINFOHEADER lpbiIn, lpbiOut; 
 
// Assume *lpbiIn points to the input (compressed) format. 
dwFormatSize = ICDecompressGetFormatSize(hIC, lpbiIn); 
h = GlobalAlloc(GHND, dwFormatSize); 
lpbiOut = (LPBITMAPINFOHEADER)GlobalLock(h); 
ICDecompressGetFormat(hIC, lpbiIn, lpbiOut); 
 
```



En el ejemplo siguiente se muestra cómo una aplicación puede usar la macro [**ICDecompressQuery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressquery) para determinar si un descompresor puede controlar los formatos de entrada y salida.


```C++
LPBITMAPINFOHEADER lpbiIn, lpbiOut; 
// Assume *lpbiIn & *lpbiOut are initialized to the respective 
// formats.
 
if (ICDecompressQuery(hIC, lpbiIn, lpbiOut) == ICERR_OK)
{ 
    
    // Format is supported - use the decompressor. 
    
} 
 
```



En el fragmento de código siguiente se muestra cómo obtener la información de la paleta mediante la macro [**ICDecompressGetPalette**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetpalette) .


```C++
ICDecompressGetPalette(hIC, lpbiIn, lpbiOut); 
 
// Move up to the palette. 
lpPalette = (LPBYTE)lpbiOut + lpbi->biSize;
 
 
```



 

 