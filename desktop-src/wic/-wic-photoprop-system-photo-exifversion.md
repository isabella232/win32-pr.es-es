---
description: Directiva de metadatos de fotos para la propiedad System.Photo.EXIFVersion.
ms.assetid: 0f9c5ea8-918f-4101-8492-3f408145a73e
title: Directiva de metadatos de fotos System.Photo.EXIFVersion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0eee0fdac7ba8e86321d4a055cb6c37c4e9c7bad3f5bcfced548cc2485b3347c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119882035"
---
# <a name="systemphotoexifversion-photo-metadata-policy"></a>Directiva de metadatos de fotos System.Photo.EXIFVersion

Directiva de metadatos de fotos para [la propiedad System.Photo.EXIFVersion.](../properties/props-system-photo-exifversion.md)

### <a name="pkey"></a>Pkey

PKEY \_ Photo \_ EXIFVersion

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

No

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de salida

VT \_ LPWSTR

### <a name="input-type"></a>Tipo de entrada

String.

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Se concilian los valores de esquemas diferentes.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Rutas de acceso de lectura



| Pedido | Ruta de acceso                          | Formato de disco   |
|-------|-------------------------------|---------------|
| 1     | /app1/ifd/exif/{ushort=36864} | exif \_ version |
| 2     | /xmp/exif:ExifVersion         | unicode       |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Ruta de acceso                          | Formato de disco   |
|-------|-------------------------------|---------------|
| 1     | /app1/ifd/exif/{ushort=36864} | exif \_ version |
| 2     | /xmp/exif:ExifVersion         | unicode       |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                          |
|-------|-------------------------------|
| 1     | /app1/ifd/exif/{ushort=36864} |
| 2     | /xmp/exif:ExifVersion         |



 

### <a name="tiff-policy"></a>Directiva TIFF

### <a name="read-paths"></a>Rutas de acceso de lectura



| Pedido | Ruta de acceso                      | Formato de disco   |
|-------|---------------------------|---------------|
| 1     | /ifd/exif/{ushort=36864}  | exif \_ version |
| 2     | /ifd/xmp/exif:ExifVersion | unicode       |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Ruta de acceso                      | Formato de disco   |
|-------|---------------------------|---------------|
| 1     | /ifd/exif/{ushort=36864}  | exif \_ version |
| 2     | /ifd/xmp/exif:ExifVersion | unicode       |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                      |
|-------|---------------------------|
| 1     | /ifd/exif/{ushort=36864}  |
| 2     | /ifd/xmp/exif:ExifVersion |



 

## <a name="remarks"></a>Comentarios

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System.Photo.EXIFVersion](../properties/props-system-photo-exifversion.md)
</dt> </dl>

 

 
