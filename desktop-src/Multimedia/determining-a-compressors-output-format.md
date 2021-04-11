---
title: Determinar el formato de salida de un compresor
description: Determinar el formato de salida de un compresor
ms.assetid: 910bd77f-4c65-4ea2-bab2-96f42a2b6cf1
keywords:
- Administrador de compresión de vídeo (VCM), formato de salida
- VCM (Administrador de compresión de vídeo), formato de salida
- ICCompressGetFormat (macro)
- ICCompressQuery (macro)
- ICCompressGetSize (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c4356870598dc08ad84c4073be5ffa3c2ddbd5b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104149269"
---
# <a name="determining-a-compressors-output-format"></a><span data-ttu-id="e630d-108">Determinar el formato de salida de un compresor</span><span class="sxs-lookup"><span data-stu-id="e630d-108">Determining a Compressor's Output Format</span></span>

<span data-ttu-id="e630d-109">En el ejemplo siguiente se usa la macro [**ICCompressGetFormat**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetformat) size para determinar el tamaño de búfer necesario para los datos que especifican el formato de compresión, se asigna un búfer del tamaño adecuado mediante la función [GlobalAlloc](/windows/win32/api/winbase/nf-winbase-globalalloc) y se recupera la información del formato de compresión mediante la macro **ICCompressGetFormat** .</span><span class="sxs-lookup"><span data-stu-id="e630d-109">The following example uses the [**ICCompressGetFormat**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetformat) size macro to determine the buffer size needed for the data specifying the compression format, allocates a buffer of the appropriate size using the [GlobalAlloc](/windows/win32/api/winbase/nf-winbase-globalalloc) function, and retrieves the compression format information using the **ICCompressGetFormat** macro.</span></span>


```C++
LPBITMAPINFOHEADER   lpbiIn, lpbiOut; 
 
// *lpbiIn must be initialized to the input format. 
 
dwFormatSize = ICCompressGetFormatSize(hIC, lpbiIn); 
h = GlobalAlloc(GHND, dwFormatSize); 
lpbiOut = (LPBITMAPINFOHEADER)GlobalLock(h); 
ICCompressGetFormat(hIC, lpbiIn, lpbiOut); 
 
```



<span data-ttu-id="e630d-110">En el ejemplo siguiente se usa la macro [**ICCompressQuery**](/windows/desktop/api/Vfw/nf-vfw-iccompressquery) para determinar si un compresor puede controlar los formatos de entrada y salida.</span><span class="sxs-lookup"><span data-stu-id="e630d-110">The following example uses the [**ICCompressQuery**](/windows/desktop/api/Vfw/nf-vfw-iccompressquery) macro to determine whether a compressor can handle the input and output formats.</span></span>


```C++
LPBITMAPINFOHEADER   lpbiIn, lpbiOut; 
 
// Both *lpbiIn and *lpbiOut must be initialized to the respective
// formats.
 

if (ICCompressQuery(hIC, lpbiIn, lpbiOut) == ICERR_OK)
{ 
 
    // Format is supported; use the compressor. 
 
}
 
 
```



<span data-ttu-id="e630d-111">En el ejemplo siguiente se usa la macro [**ICCompressGetSize**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetsize) para determinar el tamaño del búfer y se asigna un búfer de ese tamaño mediante [GlobalAlloc](/windows/win32/api/winbase/nf-winbase-globalalloc).</span><span class="sxs-lookup"><span data-stu-id="e630d-111">The following example uses the [**ICCompressGetSize**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetsize) macro to determine the buffer size, and it allocates a buffer of that size using [GlobalAlloc](/windows/win32/api/winbase/nf-winbase-globalalloc).</span></span>


```C++
// Find the worst-case buffer size. 
dwCompressBufferSize = ICCompressGetSize(hIC, lpbiIn, lpbiOut); 
 
// Allocate a buffer and get lpOutput to point to it. 
h = GlobalAlloc(GHND, dwCompressBufferSize); 
lpOutput = (LPVOID)GlobalLock(h);
 
 
```



 

 