---
description: Directiva de metadatos de fotos para la propiedad System.Image.ImageID.
ms.assetid: 2a092d16-e7b9-4ffe-9bdb-01ed328ca26f
title: Directiva de metadatos de fotos System.Image.ImageID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17453b989aba5ab0c750138ec6802d1c67a82b936dd1747d7413e39b38ae2256
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117667605"
---
# <a name="systemimageimageid-photo-metadata-policy"></a>Directiva de metadatos de fotos System.Image.ImageID

Directiva de metadatos de fotos para [la propiedad System.Image.ImageID.](../properties/props-system-image-imageid.md)

### <a name="pkey"></a>Pkey

PKEY \_ Image \_ ImageID

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

No

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de salida

VT \_ LPWSTR

### <a name="input-type"></a>Tipo de entrada

String.

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Los valores de esquemas diferentes se concilian.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta de acceso                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=42016} | ascii       |
| 2     | /xmp/exif:ImageUniqueID       | unicode     |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Ruta de acceso                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=42016} | ascii       |
| 2     | /xmp/exif:ImageUniqueID       | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                          |
|-------|-------------------------------|
| 1     | /app1/ifd/exif/{ushort=42016} |
| 2     | /xmp/exif:ImageUniqueID       |



 

### <a name="tiff-policy"></a>Directiva TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta de acceso                        | Formato de disco |
|-------|-----------------------------|-------------|
|       | /ifd/exif/{ushort=42016}    | ascii       |
|       | /ifd/xmp/exif:ImageUniqueID | unicode     |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Ruta de acceso                        | Formato de disco |
|-------|-----------------------------|-------------|
|       | /ifd/exif/{ushort=42016}    | ascii       |
|       | /ifd/xmp/exif:ImageUniqueID | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                        |
|-------|-----------------------------|
|       | /ifd/exif/{ushort=42016}    |
|       | /ifd/xmp/exif:ImageUniqueID |



 

## <a name="remarks"></a>Comentarios

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System.Image.ImageID](../properties/props-system-image-imageid.md)
</dt> </dl>

 

 
