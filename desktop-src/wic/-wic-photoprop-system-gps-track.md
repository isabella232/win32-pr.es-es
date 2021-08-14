---
description: Directiva de metadatos de fotos para la propiedad System.GPS.Track.
ms.assetid: ac9e14a0-55f1-437e-9d27-df0fa09671c1
title: Directiva de metadatos de fotos System.GPS.Track
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c89aee05d0c55e78fe4e55d7eacd8a8d0992fcb8d9f56312164c652cbc0bd81c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118205536"
---
# <a name="systemgpstrack-photo-metadata-policy"></a>Directiva de metadatos de fotos System.GPS.Track

Directiva de metadatos de fotos para [la propiedad System.GPS.Track.](../properties/props-system-gps-track.md)

### <a name="pkey"></a>Pkey

PKEY \_ GPS \_ Track

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

Sí

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de salida

VT \_ R8

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Este valor se genera a partir de System.GPS.TrackNumerator y System.GPS.TrackDenominator. No se puede escribir directamente. Se concilian los valores de esquemas diferentes.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Rutas de acceso de lectura



| Pedido | Ruta de acceso                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=15} |             |
| 2     | /xmp/exif:GPSTrack        |             |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Ruta de acceso                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=15} |             |
| 2     | /xmp/exif:GPSTrack        |             |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                      |
|-------|---------------------------|
| 1     | /app1/ifd/gps/{ushort=15} |
| 2     | /xmp/exif:gpstrack        |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Rutas de acceso de lectura



| Pedido | Ruta de acceso                   | Formato de disco |
|-------|------------------------|-------------|
| 1     | /ifd/gps/{ushort=15}   |             |
| 2     | /ifd/xmp/exif:GPSTrack |             |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Ruta de acceso                   | Formato de disco |
|-------|------------------------|-------------|
| 1     | /ifd/gps/{ushort=15}   |             |
| 2     | /ifd/xmp/exif:GPSTrack |             |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                   |
|-------|------------------------|
| 1     | /ifd/gps/{ushort=15}   |
| 2     | /ifd/xmp/exif:gpstrack |



 

## <a name="remarks"></a>Comentarios

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System.GPS.Track](../properties/props-system-gps-track.md)
</dt> </dl>

 

 
