---
description: Directiva de metadatos de fotos para la propiedad System.Photo.Aperture.
ms.assetid: 3048eb9d-4ed4-4b5b-960e-9d0fd6704041
title: Directiva de metadatos de fotos System.Photo.Aperture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df4c4dca051678e70a28321d0bd079999ae6ff6bbf11945d87372be349f691c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119393505"
---
# <a name="systemphotoaperture-photo-metadata-policy"></a>Directiva de metadatos de fotos System.Photo.Aperture

Directiva de metadatos de fotos para [la propiedad System.Photo.Aperture.](../properties/props-system-photo-aperture.md)

### <a name="pkey"></a>Pkey

PKEY \_ Photo \_ Aperture

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

Sí

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de salida

VT \_ R8

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Este valor se genera a partir de System.Photo.ApertureNumerator y System.Photo.ApertureDenominator. No se puede escribir directamente. Se concilian los valores de esquemas diferentes.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Rutas de acceso de lectura



| Pedido | Ruta de acceso                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=37378} |             |
| 2     | /xmp/exif:ApertureValue       |             |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Ruta de acceso                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=37378} |             |
| 2     | /xmp/exif:ApertureValue       |             |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                          |
|-------|-------------------------------|
| 1     | /app1/ifd/exif/{ushort=37378} |
| 2     | /xmp/exif:aperturevalue       |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Rutas de acceso de lectura



| Pedido | Ruta de acceso                        | Formato de disco |
|-------|-----------------------------|-------------|
| 1     | /ifd/exif/{ushort=37378}    |             |
| 2     | /ifd/xmp/exif:ApertureValue |             |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Ruta de acceso                        | Formato de disco |
|-------|-----------------------------|-------------|
| 1     | /ifd/exif/{ushort=37378}    |             |
| 2     | /ifd/xmp/exif:ApertureValue |             |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                        |
|-------|-----------------------------|
| 1     | /ifd/exif/{ushort=37378}    |
| 2     | /ifd/xmp/exif:aperturevalue |



 

## <a name="remarks"></a>Comentarios

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System.Photo.Aperture](../properties/props-system-photo-aperture.md)
</dt> </dl>

 

 
