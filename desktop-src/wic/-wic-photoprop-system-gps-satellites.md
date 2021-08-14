---
description: Directiva de metadatos de fotos para la propiedad System.GPS.Satellites.
ms.assetid: 5dbbbeaf-e67d-45f6-95b2-de3287202d41
title: Directiva de metadatos de fotos System.GPS.Satellites
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a65bdc244324df513b5029c682e9c2cb355da58f2c95d13910fe093ce2521c8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964844"
---
# <a name="systemgpssatellites-photo-metadata-policy"></a>Directiva de metadatos de fotos System.GPS.Satellites

Directiva de metadatos de fotos para [la propiedad System.GPS.Satellites.](../properties/props-system-gps-satellites.md)

### <a name="pkey"></a>Pkey

Satélites GPS PKEY \_ \_

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

### <a name="jpeg-policies"></a>Directivas JPEG

### <a name="read-paths"></a>Rutas de acceso de lectura



| Pedido | Ruta de acceso                     | Formato de disco |
|-------|--------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=8} | ascii       |
| 2     | /xmp/exif:GPSSatellites  | unicode     |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Ruta de acceso                     | Formato de disco |
|-------|--------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=8} | ascii       |
| 2     | /xmp/exif:GPSSatellites  | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                     |
|-------|--------------------------|
| 1     | /app1/ifd/gps/{ushort=8} |
| 2     | /xmp/exif:gpssatellites  |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Rutas de acceso de lectura



| Pedido | Ruta de acceso                        | Formato de disco |
|-------|-----------------------------|-------------|
| 1     | /ifd/gps/{ushort=8}         | ascii       |
| 2     | /ifd/xmp/exif:GPSSatellites | unicode     |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Ruta de acceso                        | Formato de disco |
|-------|-----------------------------|-------------|
| 1     | /ifd/gps/{ushort=8}         | ascii       |
| 2     | /ifd/xmp/exif:GPSSatellites | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                        |
|-------|-----------------------------|
| 1     | /ifd/gps/{ushort=8}         |
| 2     | /ifd/xmp/exif:gpssatellites |



 

## <a name="remarks"></a>Comentarios

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System.GPS.Satellites](../properties/props-system-gps-satellites.md)
</dt> </dl>

 

 
