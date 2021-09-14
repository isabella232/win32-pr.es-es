---
description: Directiva de metadatos de fotos para la propiedad System.Photo.Sharpness.
ms.assetid: 0fda4832-940b-4b5a-bd20-7e48c7800925
title: Directiva de metadatos de fotos System.Photo.Sharpness
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48d635691f0b0e0801c1e37a006faa686aff0a8c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127247533"
---
# <a name="systemphotosharpness-photo-metadata-policy"></a>Directiva de metadatos de fotos System.Photo.Sharpness

Directiva de metadatos de fotos para [la propiedad System.Photo.Sharpness.](../properties/props-system-photo-sharpness.md)

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ Sharpness

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

No

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de salida

VT \_ UI4

### <a name="input-type"></a>Tipo de entrada

UShort

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Los valores de esquemas diferentes se concilian.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Rutas de acceso de lectura



| Pedido | Path                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=41994} | ushort      |
| 2     | /xmp/exif:Sharpness           | unicode     |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Path                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=41994} | ushort      |
| 2     | /xmp/exif:Sharpness           | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Path                          |
|-------|-------------------------------|
| 1     | /app1/ifd/exif/{ushort=41994} |
| 2     | /xmp/exif:sharpness           |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Rutas de acceso de lectura



| Pedido | Path                     | Formato de disco |
|-------|--------------------------|-------------|
| 1     | /ifd/exif/{ushort=41994} | ushort      |
| 2     | /ifd/xmp/exif:Sharpness  | unicode     |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Path                     | Formato de disco |
|-------|--------------------------|-------------|
| 1     | /ifd/exif/{ushort=41994} | ushort      |
| 2     | /ifd/xmp/exif:Sharpness  | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Path                     |
|-------|--------------------------|
| 1     | /ifd/exif/{ushort=41994} |
| 2     | /ifd/xmp/exif:sharpness  |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System.Photo.Sharpness](../properties/props-system-photo-sharpness.md)
</dt> </dl>

 

 
