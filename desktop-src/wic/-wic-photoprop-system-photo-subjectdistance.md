---
description: Directiva de metadatos de fotos para la propiedad System.Photo.SubjectDistance.
ms.assetid: 8d5acd7e-7227-4a79-890a-43e6dace3864
title: Directiva de metadatos de fotos System.Photo.SubjectDistance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86ec1868b1e33c4bcaaaea9a9203cc73733646cc82dade52c86b0c8caec4a704
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964774"
---
# <a name="systemphotosubjectdistance-photo-metadata-policy"></a>Directiva de metadatos de fotos System.Photo.SubjectDistance

Directiva de metadatos de fotos para [la propiedad System.Photo.SubjectDistance.](../properties/props-system-photo-subjectdistance.md)

### <a name="pkey"></a>Pkey

PKEY \_ Photo \_ SubjectDistance

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

Sí

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de salida

VT \_ R8

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Este valor se genera a partir de System.Photo.SubjectDistanceNumerator y System.Photo.SubjectDistanceDenominator. No se puede escribir directamente. Se concilian los valores de esquemas diferentes.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Rutas de acceso de lectura



| Pedido | Ruta de acceso                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=37382} |             |
| 2     | /xmp/exif:SubjectDistance     |             |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Ruta de acceso                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=37382} |             |
| 2     | /xmp/exif:SubjectDistance     |             |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                          |
|-------|-------------------------------|
| 1     | /app1/ifd/exif/{ushort=37382} |
| 2     | /xmp/exif:subjectdistance     |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Rutas de acceso de lectura



| Pedido | Ruta de acceso                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /ifd/exif/{ushort=37382}      |             |
| 2     | /ifd/xmp/exif:SubjectDistance |             |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Ruta de acceso                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /ifd/exif/{ushort=37382}      |             |
| 2     | /ifd/xmp/exif:SubjectDistance |             |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                          |
|-------|-------------------------------|
| 1     | /ifd/exif/{ushort=37382}      |
| 2     | /ifd/xmp/exif:subjectdistance |



 

## <a name="remarks"></a>Comentarios

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System.Photo.SubjectDistance](../properties/props-system-photo-subjectdistance.md)
</dt> </dl>

 

 
