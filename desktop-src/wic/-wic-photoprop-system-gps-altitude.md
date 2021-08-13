---
description: Directiva de metadatos de fotos para la propiedad System.GPS.Altitude.
ms.assetid: 63d59aa3-52a6-4b6f-b6ec-a1c4abcee83f
title: Directiva de metadatos de fotos System.GPS.Altitude
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40a9209bfb0bbc1a4c6f95ce4a995d32d3f532c293dd2295c335eea61c22df89
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119442005"
---
# <a name="systemgpsaltitude-photo-metadata-policy"></a>Directiva de metadatos de fotos System.GPS.Altitude

Directiva de metadatos de fotos para [la propiedad System.GPS.Altitude.](../properties/props-system-gps-altitude.md)

### <a name="pkey"></a>Pkey

PKEY \_ GPS \_ Altitude

### <a name="description"></a>Descripción

La altitud se indica como un valor absoluto al que se hace referencia en metros.

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

Sí

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de salida

VT \_ R8

### <a name="input-propvariant-type"></a>Tipo PROPVARIANT de entrada

VT \_ R8

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Este valor se puede escribir escribiendo en System.GPS.Altitude.Numerator y System.GPS.Altitude.Denominator. No se puede escribir directamente. Las rutas de acceso de escritura de las tablas siguientes indican dónde se puede guardar el valor cuando se genera, no cuando se escribe directamente. Cuando se lee el valor, se concilian los valores de esquemas diferentes.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Rutas de acceso de lectura



| Pedido | Path                     | Formato de disco |
|-------|--------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=6} |             |
| 2     | /xmp/exif:GPSAltitude    |             |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Path                     | Formato de disco |
|-------|--------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=6} |             |
| 2     | /xmp/exif:GPSAltitude    |             |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Path                     |
|-------|--------------------------|
| 1     | /app1/ifd/gps/{ushort=6} |
| 2     | /xmp/exif:gpsaltitude    |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Rutas de acceso de lectura



| Pedido | Path                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /ifd/gps/{ushort=6}       |             |
| 2     | /ifd/xmp/exif:GPSAltitude |             |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Path                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /ifd/gps/{ushort=6}       |             |
| 2     | /ifd/xmp/exif:GPSAltitude |             |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Path                      |     |
|-------|---------------------------|-----|
| 1     | /ifd/gps/{ushort=6}       |     |
| 2     | /ifd/xmp/exif:gpsaltitude |     |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System.GPS.Altitude](../properties/props-system-gps-altitude.md)
</dt> </dl>

 

 
