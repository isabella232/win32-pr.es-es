---
description: Directiva de metadatos de fotos para la propiedad System.GPS.Latitude.
ms.assetid: 0f8cea07-da96-4d2a-8444-6073b51e1236
title: Directiva de metadatos de fotos System.GPS.Latitude
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41dd1eb0ee21ab02eeb8c83d5ea84f28c07c2811929f2b8c973cace4a4a06fd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118710629"
---
# <a name="systemgpslatitude-photo-metadata-policy"></a>Directiva de metadatos de fotos System.GPS.Latitude

Directiva de metadatos de fotos para [la propiedad System.GPS.Latitude.](../properties/props-system-gps-latitude.md)

### <a name="pkey"></a>Pkey

Latitud gps de PKEY \_ \_

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

Sí

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de salida

VT \_ VECTOR \| VT \_ R8

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Este valor se puede escribir escribiendo en System.GPS.LatitudeNumerator y System.GPS.LatitudeDenominator. No se puede escribir directamente. Los valores de esquemas diferentes se concilian.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta de acceso                     | Formato de disco |
|-------|--------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=2} |             |
| 2     | /xmp/exif:GPSLatitude    |             |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Ruta de acceso                     | Formato de disco |
|-------|--------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=2} |             |
| 2     | /xmp/exif:GPSLatitude    |             |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                     |
|-------|--------------------------|
| 1     | /app1/ifd/gps/{ushort=2} |
| 2     | /xmp/exif:gpslatitude    |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta de acceso                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /ifd/gps/{ushort=2}       |             |
| 2     | /ifd/xmp/exif:GPSLatitude |             |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Ruta de acceso                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /ifd/gps/{ushort=2}       |             |
| 2     | /ifd/xmp/exif:GPSLatitude |             |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                      |
|-------|---------------------------|
| 1     | /ifd/gps/{ushort=2}       |
| 2     | /ifd/xmp/exif:gpslatitude |



 

## <a name="remarks"></a>Comentarios

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System.GPS.Latitude](../properties/props-system-gps-latitude.md)
</dt> </dl>

 

 
