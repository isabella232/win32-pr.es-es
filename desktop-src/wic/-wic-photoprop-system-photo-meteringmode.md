---
description: Directiva de metadatos de fotos para la propiedad System.Photo.MeteringMode.
ms.assetid: cb0bf0d5-eccf-4345-a242-76769c34e02d
title: Directiva de metadatos de fotos System.Photo.MeteringMode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 424b14fa6216d5c88c350512d1583b311f92ef2f487e604760b1836b296d3bf2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964784"
---
# <a name="systemphotometeringmode-photo-metadata-policy"></a>Directiva de metadatos de fotos System.Photo.MeteringMode

Directiva de metadatos de fotos para [la propiedad System.Photo.MeteringMode.](../properties/props-system-photo-meteringmode.md)

### <a name="pkey"></a>Pkey

PKEY \_ Photo \_ MeteringMode

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

No

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de salida

VT \_ UI2

### <a name="input-type"></a>Tipo de entrada

UShort

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Los valores de esquemas diferentes se concilian.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta de acceso                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=37383} | ushort      |
| 2     | /xmp/exif:MeteringMode        | unicode     |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Ruta de acceso                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=37383} | ushort      |
| 2     | /xmp/exif:MeteringMode        | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                          |
|-------|-------------------------------|
| 1     | /app1/ifd/exif/{ushort=37383} |
| 2     | /xmp/exif:meteringmode        |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta de acceso                       | Formato de disco |
|-------|----------------------------|-------------|
| 1     | /ifd/exif/{ushort=37383}   | ushort      |
| 2     | /ifd/xmp/exif:MeteringMode | unicode     |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Ruta de acceso                       | Formato de disco |
|-------|----------------------------|-------------|
| 1     | /ifd/exif/{ushort=37383}   | ushort      |
| 2     | /ifd/xmp/exif:MeteringMode | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                       |
|-------|----------------------------|
| 1     | /ifd/exif/{ushort=37383}   |
| 2     | /ifd/xmp/exif:meteringmode |



 

## <a name="remarks"></a>Comentarios

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System.Photo.MeteringMode](../properties/props-system-photo-meteringmode.md)
</dt> </dl>

 

 
