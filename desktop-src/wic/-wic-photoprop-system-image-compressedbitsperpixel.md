---
description: La Directiva de metadatos de la fotografía para la propiedad System. Image. CompressedBitsPerPixel.
ms.assetid: e97a5c68-6d4a-44af-8096-22680f8b16b8
title: Directiva de metadatos de la foto de System. Image. CompressedBitsPerPixel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b45b3b1e8b29cdf992cd3b451a2e8a43947139a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706404"
---
# <a name="systemimagecompressedbitsperpixel-photo-metadata-policy"></a>Directiva de metadatos de la foto de System. Image. CompressedBitsPerPixel

La Directiva de metadatos de la fotografía para la propiedad [System. Image. CompressedBitsPerPixel](../properties/props-system-image-compressedbitsperpixel.md) .

### <a name="pkey"></a>PKEY

PKEY \_ Image \_ CompressedBitsPerPixel

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

Sí

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de salida

VT \_ R8

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Este valor se genera a partir de System. Image. CompressedBitsPerPixelNumerator y System. Image. CompressedBitsPerPixelDenominator. No se puede escribir directamente. Se reconcilian los valores de los distintos esquemas.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                             | Formato de disco |
|-------|----------------------------------|-------------|
| 1     | /app1/IFD/Exif/{ushort = 37122}    |             |
| 2     | /xmp/exif:CompressedBitsPerPixel |             |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                             |
|-------|----------------------------------|
| 1     | /app1/IFD/Exif/{ushort = 37122}    |
| 2     | /xmp/exif:compressedbitsperpixel |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                                 | Formato de disco |
|-------|--------------------------------------|-------------|
| 1     | /IFD/Exif/{ushort = 37122}             |             |
| 2     | /ifd/xmp/exif:CompressedBitsPerPixel |             |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                                 |
|-------|--------------------------------------|
| 1     | /IFD/Exif/{ushort = 37122}             |
| 2     | /ifd/xmp/exif:compressedbitsperpixel |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System. Image. CompressedBitsPerPixel](../properties/props-system-image-compressedbitsperpixel.md)
</dt> </dl>

 

 
