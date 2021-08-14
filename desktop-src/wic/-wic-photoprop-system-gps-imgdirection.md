---
description: Directiva de metadatos de fotos para la propiedad System.GPS.ImgDirection.
ms.assetid: c9a0f5de-4010-4251-a5d5-8728b7ae6d33
title: Directiva de metadatos de fotos System.GPS.ImgDirection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43544458c4b6a64df1d396426ebbe487d80324d24dd10c2f8f6f0e548d9eca99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118710675"
---
# <a name="systemgpsimgdirection-photo-metadata-policy"></a>Directiva de metadatos de fotos System.GPS.ImgDirection

Directiva de metadatos de fotos para [la propiedad System.GPS.ImgDirection.](../properties/props-system-gps-imgdirection.md)

### <a name="pkey"></a>Pkey

PKEY \_ GPS \_ ImgDirection

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

Sí

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de salida

VT \_ R8

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Este valor se puede escribir escribiendo en System.GPS.ImgDirectionNumerator y System.GPS.ImgDirectionDenominator. No se puede escribir directamente. Se concilian los valores de esquemas diferentes.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Rutas de acceso de lectura



| Pedido | Path                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=17} |             |
| 2     | /xmp/exif:GPSImgDirection |             |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Path                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=17} |             |
| 2     | /xmp/exif:GPSImgDirection |             |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Path                      |
|-------|---------------------------|
| 1     | /app1/ifd/gps/{ushort=17} |
| 2     | /xmp/exif:gpsimgdirection |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Rutas de acceso de lectura



| Pedido | Path                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /ifd/gps/{ushort=17}          |             |
| 2     | /ifd/xmp/exif:GPSImgDirection |             |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Path                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /ifd/gps/{ushort=17}          |             |
| 2     | /ifd/xmp/exif:GPSImgDirection |             |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Path                          |
|-------|-------------------------------|
| 1     | /ifd/gps/{ushort=17}          |
| 2     | /ifd/xmp/exif:gpsimgdirection |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System.GPS.ImgDirection](../properties/props-system-gps-imgdirection.md)
</dt> </dl>

 

 
