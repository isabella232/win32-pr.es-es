---
description: La Directiva de metadatos de fotos para la propiedad System. Photo. DateTaken.
ms.assetid: 800aa01b-6064-45df-a40e-6537819df4d7
title: Directiva de metadatos de la foto de System. Photo. DateTaken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc1d3fb50a9a94e4bb13b35a0a5726572d78429f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717149"
---
# <a name="systemphotodatetaken-photo-metadata-policy"></a>Directiva de metadatos de la foto de System. Photo. DateTaken

La Directiva de metadatos de fotos para la propiedad [System. Photo. DateTaken](../properties/props-system-photo-datetaken.md) .

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ DateTaken

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

No

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de salida

VT \_ FILETIME

### <a name="input-type"></a>Tipo de entrada

DateTime

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Se reconcilian los valores de los distintos esquemas.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                                  | Formato de disco |
|-------|---------------------------------------|-------------|
| 1     | /app1/IFD/Exif/{ushort = 36867}         | ascii       |
| 2     | /app13/IRB/8bimiptc/IPTC/Date creado | unicode     |
| 3     | /XMP/XMP: CreateDate                   | unicode     |
| 4     | /app1/IFD/Exif/{ushort = 36868}         | ascii       |
| 5     | /app13/IRB/8bimiptc/IPTC/Date creado | unicode     |
| 6     | /xmp/exif:DateTimeOriginal            | unicode     |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                                  | Formato de disco |
|-------|---------------------------------------|-------------|
| 1     | /app1/IFD/Exif/{ushort = 36867}         | ascii       |
| 2     | /app13/IRB/8bimiptc/IPTC/Date creado | unicode     |
| 3     | /XMP/XMP: CreateDate                   | unicode     |
| 4     | /app1/IFD/Exif/{ushort = 36868}         | ascii       |
| 5     | /xmp/exif:DateTimeOriginal            | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                                  |
|-------|---------------------------------------|
| 1     | /app1/IFD/Exif/{ushort = 36867}         |
| 2     | /app1/IFD/Exif/{ushort = 37521}         |
| 3     | /app1/IFD/Exif/{ushort = 36868}         |
| 4     | /app1/IFD/Exif/{ushort = 37522}         |
| 5     | /xmp/exif:DateTimeOriginal            |
| 6     | /XMP/XMP: CreateDate                   |
| 7     | /app13/IRB/8bimiptc/IPTC/Date creado |
| 8     | /app13/IRB/8bimiptc/IPTC/Time creado |



 

### <a name="tiff-policy"></a>Directiva TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                                | Formato de disco |
|-------|-------------------------------------|-------------|
| 1     | /IFD/Exif/{ushort = 36867}            | ascii       |
| 2     | /IFD/IPTC/Date creado              | unicode     |
| 3     | /IFD/XMP/XMP: CreateDate             | unicode     |
| 4     | /IFD/Exif/{ushort = 36868}            | ascii       |
| 5     | /IFD/IPTC/Date creado              | unicode     |
| 6     | /IFD/IRB/8bimiptc/IPTC/Date creado | unicode     |
| 7     | /ifd/xmp/exif:DateTimeOriginal      | unicode     |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                                | Formato de disco |
|-------|-------------------------------------|-------------|
| 1     | /IFD/Exif/{ushort = 36867}            | ascii       |
| 2     | /IFD/IPTC/Date creado              | unicode     |
| 3     | /IFD/XMP/XMP: CreateDate             | unicode     |
| 4     | /IFD/Exif/{ushort = 36868}            | ascii       |
| 5     | /IFD/IRB/8bimiptc/IPTC/Date creado | unicode     |
| 6     | /ifd/xmp/exif:DateTimeOriginal      | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                                |
|-------|-------------------------------------|
| 1     | /IFD/Exif/{ushort = 36867}            |
| 2     | /IFD/Exif/{ushort = 37521}            |
| 3     | /IFD/Exif/{ushort = 36868}            |
| 4     | /IFD/Exif/{ushort = 37522}            |
| 5     | /ifd/xmp/exif:DateTimeOriginal      |
| 6     | /IFD/XMP/XMP: CreateDate             |
| 7     | /IFD/IPTC/Date creado              |
| 8     | /IFD/IPTC/Time creado              |
| 9     | /IFD/IRB/8bimiptc/IPTC/Date creado |
| 10    | /IFD/IRB/8bimiptc/IPTC/Time creado |



 

### <a name="png-policy"></a>Directiva PNG

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /\[\*\]Hora de creación y texto | ascii       |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                      | Formato de disco |
|-------|---------------------------|-------------|
| 2     | /\[\*\]Hora de creación y texto | ascii       |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                      |
|-------|---------------------------|
| 3     | /\[\*\]Hora de creación y texto |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System. Photo. DateTaken](../properties/props-system-photo-datetaken.md)
</dt> </dl>

 

 
