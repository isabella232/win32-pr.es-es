---
description: La Directiva de metadatos de la fotografía para la propiedad System. GPS. longitude.
ms.assetid: 36539e20-d00c-4bbb-b9ee-1cf5e4b8df4b
title: Directiva de metadatos de fotos de System. GPS. longitud
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25eb9869bc536f97adfc8f3c0f5b1f70c8bf030f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678369"
---
# <a name="systemgpslongitude-photo-metadata-policy"></a>Directiva de metadatos de fotos de System. GPS. longitud

La Directiva de metadatos de la fotografía para la propiedad [System. GPS. longitude](../properties/props-system-gps-longitude.md) .

### <a name="pkey"></a>PKEY

\_Longitud de GPS de PKEY \_

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

Sí

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de salida

VT \_ Vector \| VT \_ R8

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Este valor se puede escribir escribiendo en System. GPS. LongitudeNumerator y System. GPS. LongitudeDenominator. No se puede escribir directamente. Se reconcilian los valores de los distintos esquemas.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                     | Formato de disco |
|-------|--------------------------|-------------|
| 1     | /app1/IFD/GPS/{ushort = 4} |             |
| 2     | /xmp/exif:GPSLongitude   |             |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                     | Formato de disco |
|-------|--------------------------|-------------|
| 1     | /app1/IFD/GPS/{ushort = 4} |             |
| 2     | /xmp/exif:GPSLongitude   |             |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                     |
|-------|--------------------------|
| 1     | /app1/IFD/GPS/{ushort = 4} |
| 2     | /xmp/exif:gpslongitude   |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                       | Formato de disco |
|-------|----------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 4}        |             |
| 2     | /ifd/xmp/exif:GPSLongitude |             |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                       | Formato de disco |
|-------|----------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 4}        |             |
| 2     | /ifd/xmp/exif:GPSLongitude |             |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                       |
|-------|----------------------------|
| 1     | /IFD/GPS/{ushort = 4}        |
| 2     | /ifd/xmp/exif:gpslongitude |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System. GPS. longitud](../properties/props-system-gps-longitude.md)
</dt> </dl>

 

 
