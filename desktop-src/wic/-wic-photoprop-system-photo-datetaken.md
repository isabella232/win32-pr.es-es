---
description: Directiva de metadatos de fotos para la propiedad System.Photo.DateTaken.
ms.assetid: 800aa01b-6064-45df-a40e-6537819df4d7
title: Directiva de metadatos de fotos System.Photo.DateTaken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 691476c704d3fdbc4ff5e01467031f2b41884ccb16be537904484a9d01c8fa18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119087081"
---
# <a name="systemphotodatetaken-photo-metadata-policy"></a>Directiva de metadatos de fotos System.Photo.DateTaken

Directiva de metadatos de fotos para [la propiedad System.Photo.DateTaken.](../properties/props-system-photo-datetaken.md)

### <a name="pkey"></a>Pkey

PKEY \_ Photo \_ DateTaken

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

No

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de salida

VT \_ FILETIME

### <a name="input-type"></a>Tipo de entrada

DateTime

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Los valores de esquemas diferentes se concilian.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta de acceso                                  | Formato de disco |
|-------|---------------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=36867}         | ascii       |
| 2     | /app13/irb/8bimiptc/iptc/date created | unicode     |
| 3     | /xmp/xmp:CreateDate                   | unicode     |
| 4     | /app1/ifd/exif/{ushort=36868}         | ascii       |
| 5     | /app13/irb/8bimiptc/iptc/date created | unicode     |
| 6     | /xmp/exif:DateTimeOriginal            | unicode     |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Ruta de acceso                                  | Formato de disco |
|-------|---------------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=36867}         | ascii       |
| 2     | /app13/irb/8bimiptc/iptc/date created | unicode     |
| 3     | /xmp/xmp:CreateDate                   | unicode     |
| 4     | /app1/ifd/exif/{ushort=36868}         | ascii       |
| 5     | /xmp/exif:DateTimeOriginal            | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                                  |
|-------|---------------------------------------|
| 1     | /app1/ifd/exif/{ushort=36867}         |
| 2     | /app1/ifd/exif/{ushort=37521}         |
| 3     | /app1/ifd/exif/{ushort=36868}         |
| 4     | /app1/ifd/exif/{ushort=37522}         |
| 5     | /xmp/exif:DateTimeOriginal            |
| 6     | /xmp/xmp:CreateDate                   |
| 7     | /app13/irb/8bimiptc/iptc/date created |
| 8     | /app13/irb/8bimiptc/iptc/time creado |



 

### <a name="tiff-policy"></a>Directiva TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta de acceso                                | Formato de disco |
|-------|-------------------------------------|-------------|
| 1     | /ifd/exif/{ushort=36867}            | ascii       |
| 2     | /ifd/iptc/date created              | unicode     |
| 3     | /ifd/xmp/xmp:CreateDate             | unicode     |
| 4     | /ifd/exif/{ushort=36868}            | ascii       |
| 5     | /ifd/iptc/date created              | unicode     |
| 6     | /ifd/irb/8bimiptc/iptc/date created | unicode     |
| 7     | /ifd/xmp/exif:DateTimeOriginal      | unicode     |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Ruta de acceso                                | Formato de disco |
|-------|-------------------------------------|-------------|
| 1     | /ifd/exif/{ushort=36867}            | ascii       |
| 2     | /ifd/iptc/date created              | unicode     |
| 3     | /ifd/xmp/xmp:CreateDate             | unicode     |
| 4     | /ifd/exif/{ushort=36868}            | ascii       |
| 5     | /ifd/irb/8bimiptc/iptc/date created | unicode     |
| 6     | /ifd/xmp/exif:DateTimeOriginal      | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                                |
|-------|-------------------------------------|
| 1     | /ifd/exif/{ushort=36867}            |
| 2     | /ifd/exif/{ushort=37521}            |
| 3     | /ifd/exif/{ushort=36868}            |
| 4     | /ifd/exif/{ushort=37522}            |
| 5     | /ifd/xmp/exif:DateTimeOriginal      |
| 6     | /ifd/xmp/xmp:CreateDate             |
| 7     | /ifd/iptc/date created              |
| 8     | /ifd/iptc/time creado              |
| 9     | /ifd/irb/8bimiptc/iptc/date created |
| 10    | /ifd/irb/8bimiptc/iptc/time creado |



 

### <a name="png-policy"></a>Directiva PNG

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta de acceso                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /\[\*\]tEXt/Hora de creación | ascii       |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Ruta de acceso                      | Formato de disco |
|-------|---------------------------|-------------|
| 2     | /\[\*\]tEXt/Hora de creación | ascii       |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                      |
|-------|---------------------------|
| 3     | /\[\*\]tEXt/Hora de creación |



 

## <a name="remarks"></a>Comentarios

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System.Photo.DateTaken](../properties/props-system-photo-datetaken.md)
</dt> </dl>

 

 
