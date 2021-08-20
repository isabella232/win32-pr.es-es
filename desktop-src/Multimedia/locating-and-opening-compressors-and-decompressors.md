---
title: Búsqueda y apertura de descomprimores y descompresión
description: Búsqueda y apertura de descomprimores y descompresión
ms.assetid: ed931f01-dbfc-4fdc-b725-c062302b037b
keywords:
- Administrador de compresión de vídeo (VCM), apertura de ingerentes
- VCM (administrador de compresión de vídeo), apertura de los comprimires
- Función ICLocate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c861c9fb5c317b6b0fc3a48552db200389739ebd8a53dbf15fbdbd0564ba8f76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118139306"
---
# <a name="locating-and-opening-compressors-and-decompressors"></a>Búsqueda y apertura de descomprimores y descompresión

En el ejemplo siguiente se usa [**la función ICLocate**](/windows/desktop/api/Vfw/nf-vfw-iclocate) para buscar un resultado que pueda comprimir un mapa de bits de 8 bits por píxel.


```C++
BITMAPINFOHEADER bih; 
HIC              hIC 
 
// Initialize the bitmap structure. 
bih.biSize = sizeof(BITMAPINFOHEADER); 
bih.biWidth = bih.biHeight = 0; 
bih.biPlanes = 1; 
bih.biCompression = BI_RGB;      // standard RGB bitmap 
bih.biBitcount = 8;              // 8 bits-per-pixel format 
bih.biSizeImage = 0; 
bih.biXPelsPerMeter = bih.biYPelsPerMeter = 0; 
bih.biClrUsed = bih.biClrImportant = 256; 
 
hIC = ICLocate (ICTYPE_VIDEO, 0L, (LPBITMAPINFOHEADER) &bih, 
    NULL, ICMODE_COMPRESS); 
 
```



En el ejemplo siguiente se enumeran los descompresores del sistema para buscar uno que pueda controlar el formato de sus imágenes. En este ejemplo se usa **ICTYPE \_ VIDEO** (que es equivalente al código de cuatro caracteres "VIDC") y la macro [**ICDecompressQuery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressquery) para determinar si un descomprimidor o un descomprimidor admiten el formato de imagen.


```C++
for (i=0; ICInfo(fccType, i, &icinfo); i++) 
{ 
    hic = ICOpen(icinfo.fccType, icinfo.fccHandler, ICMODE_QUERY); 
    if (hic) 
    { 
        // Skip this compressor if it can't handle the format. 
        if (fccType == ICTYPE_VIDEO && pvIn != NULL && 
            ICDecompressQuery(hic, pvIn, NULL) != ICERR_OK) 
        { 
            ICClose(hic); 
            continue; 
        } 
 
        // Find out the compressor name. 
        ICGetInfo(hic, &icinfo, sizeof(icinfo)); 
 
        // Add it to the combo box. 
        n = ComboBox_AddString(hwndC,icinfo.szDescription); 
        ComboBox_SetItemData(hwndC, n, hic); 
    } 
} 
 
```



En el ejemplo siguiente se intenta localizar un compresión específico para comprimir el formato RGB de 8 bits a un formato RLE de 8 bits.


```C++
BITMAPINFOHEADER    bihIn, bihOut; 
HIC                 hIC 
 
// Initialize the bitmap structure. 

biSize = bihOut.biSize = sizeof(BITMAPINFOHEADER); 
bihIn.biWidth = bihIn.biHeight = bihOut.biWidth = bihOut.biHeight = 0; 
bihIn.biPlanes = bihOut.biPlanes= 1; 
bihIn.biCompression = BI_RGB;        // standard RGB bitmap for input 
bihOut.biCompression = BI_RLE8;      // 8-bit RLE for output format 
bihIn.biBitcount = bihOut.biBitCount = 8;  // 8 bits-per-pixel format 
bihIn.biSizeImage = bihOut.biSizeImage = 0; 
bihIn.biXPelsPerMeter = bih.biYPelsPerMeter = 
    bihOut.biXPelsPerMeter = bihOut.biYPelsPerMeter = 0; 
bihIn.biClrUsed = bih.biClrImportant = 
    bihOut.biClrUsed = bihOut.biClrImportant = 256; 

hIC = ICLocate (ICTYPE_VIDEO, 0L, 
    (LPBITMAPINFOHEADER)&bihIn, 
    (LPBITMAPINFOHEADER)&bihOut, ICMODE_COMPRESS); 
 
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso del Administrador de compresión de vídeo](using-the-video-compression-manager.md)
</dt> </dl>

 

 




