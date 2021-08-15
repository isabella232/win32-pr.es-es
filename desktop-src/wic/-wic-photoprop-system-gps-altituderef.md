---
description: Directiva de metadatos de fotos para la propiedad System.GPS.AltitudeRef.
ms.assetid: abbb2441-25ca-484b-a744-620ff2794221
title: Directiva de metadatos de fotos System.GPS.AltitudeRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca49213754f605dcf6df40dfa3ff00e2b7aeaf765008037c23da21e35ab9ddee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118710702"
---
# <a name="systemgpsaltituderef-photo-metadata-policy"></a>Directiva de metadatos de fotos System.GPS.AltitudeRef

Directiva de metadatos de fotos para [la propiedad System.GPS.AltitudeRef.](../properties/props-system-gps-altituderef.md)

### <a name="pkey"></a>Pkey

PKEY \_ GPS \_ AltitudeRef

### <a name="description"></a>Descripción

Indica la altitud usada como altitud de referencia. Un valor de 0 indica que la altitud está por encima del nivel del mar. Un valor de 1 indica una altitud por debajo del nivel del mar.

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

No

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de salida

VT \_ UI1

### <a name="input-type"></a>Tipo de entrada

Byte.

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Los valores de esquemas diferentes se concilian.

### <a name="jpeg-policies"></a>Directivas JPEG

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Path                     | Formato de disco |
|-------|--------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=5} | byte        |
| 2     | /xmp/exif:GPSAltitudeRef | unicode     |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Path                     | Formato de disco |
|-------|--------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=5} | byte        |
| 2     | /xmp/exif:GPSAltitudeRef | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Path                     |
|-------|--------------------------|
| 1     | /app1/ifd/gps/{ushort=5} |
| 2     | /xmp/exif:gpsaltituderef |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Path                         | Formato de disco |
|-------|------------------------------|-------------|
| 1     | /ifd/gps/{ushort=5}          | byte        |
| 2     | /ifd/xmp/exif:GPSAltitudeRef | unicode     |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Path                         | Formato de disco |
|-------|------------------------------|-------------|
| 1     | /ifd/gps/{ushort=5}          | byte        |
| 2     | /ifd/xmp/exif:GPSAltitudeRef | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Path                         |
|-------|------------------------------|
| 1     | /ifd/gps/{ushort=5}          |
| 2     | /ifd/xmp/exif:gpsaltituderef |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System.GPS.AltitudeRef](../properties/props-system-gps-altituderef.md)
</dt> </dl>

 

 
