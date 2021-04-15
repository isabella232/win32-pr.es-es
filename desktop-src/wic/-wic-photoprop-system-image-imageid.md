---
description: La Directiva de metadatos de la fotografía para la propiedad System. Image. ImageID.
ms.assetid: 2a092d16-e7b9-4ffe-9bdb-01ed328ca26f
title: Directiva de metadatos de la foto de System. Image. ImageID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bab812a8719c905002c91d33a65cc2b570d37cc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104545718"
---
# <a name="systemimageimageid-photo-metadata-policy"></a>Directiva de metadatos de la foto de System. Image. ImageID

La Directiva de metadatos de la fotografía para la propiedad [System. Image. ImageID](../properties/props-system-image-imageid.md) .

### <a name="pkey"></a>PKEY

PKEY \_ Image \_ ImageID

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

No

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de salida

VT \_ LPWStr

### <a name="input-type"></a>Tipo de entrada

String.

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Se reconcilian los valores de los distintos esquemas.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /app1/IFD/Exif/{ushort = 42016} | ascii       |
| 2     | /xmp/exif:ImageUniqueID       | unicode     |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /app1/IFD/Exif/{ushort = 42016} | ascii       |
| 2     | /xmp/exif:ImageUniqueID       | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                          |
|-------|-------------------------------|
| 1     | /app1/IFD/Exif/{ushort = 42016} |
| 2     | /xmp/exif:ImageUniqueID       |



 

### <a name="tiff-policy"></a>Directiva TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                        | Formato de disco |
|-------|-----------------------------|-------------|
|       | /IFD/Exif/{ushort = 42016}    | ascii       |
|       | /ifd/xmp/exif:ImageUniqueID | unicode     |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                        | Formato de disco |
|-------|-----------------------------|-------------|
|       | /IFD/Exif/{ushort = 42016}    | ascii       |
|       | /ifd/xmp/exif:ImageUniqueID | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                        |
|-------|-----------------------------|
|       | /IFD/Exif/{ushort = 42016}    |
|       | /ifd/xmp/exif:ImageUniqueID |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System. Image. ImageID](../properties/props-system-image-imageid.md)
</dt> </dl>

 

 
