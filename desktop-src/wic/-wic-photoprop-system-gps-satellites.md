---
description: La Directiva de metadatos de la fotografía para la propiedad System. GPS. Satellites.
ms.assetid: 5dbbbeaf-e67d-45f6-95b2-de3287202d41
title: Directiva de metadatos de fotografía de System. GPS. Satellites
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 980393accdb1bee3d2a44dd539f3c9fb169c648b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105677969"
---
# <a name="systemgpssatellites-photo-metadata-policy"></a>Directiva de metadatos de fotografía de System. GPS. Satellites

La Directiva de metadatos de la fotografía para la propiedad [System. GPS. Satellites](../properties/props-system-gps-satellites.md) .

### <a name="pkey"></a>PKEY

\_Satélites GPS de PKEY \_

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

No

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de salida

VT \_ LPWStr

### <a name="input-type"></a>Tipo de entrada

String.

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Se reconcilian los valores de los distintos esquemas.

### <a name="jpeg-policies"></a>Directivas JPEG

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                     | Formato de disco |
|-------|--------------------------|-------------|
| 1     | /app1/IFD/GPS/{ushort = 8} | ascii       |
| 2     | /xmp/exif:GPSSatellites  | unicode     |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                     | Formato de disco |
|-------|--------------------------|-------------|
| 1     | /app1/IFD/GPS/{ushort = 8} | ascii       |
| 2     | /xmp/exif:GPSSatellites  | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                     |
|-------|--------------------------|
| 1     | /app1/IFD/GPS/{ushort = 8} |
| 2     | /xmp/exif:gpssatellites  |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                        | Formato de disco |
|-------|-----------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 8}         | ascii       |
| 2     | /ifd/xmp/exif:GPSSatellites | unicode     |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                        | Formato de disco |
|-------|-----------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 8}         | ascii       |
| 2     | /ifd/xmp/exif:GPSSatellites | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                        |
|-------|-----------------------------|
| 1     | /IFD/GPS/{ushort = 8}         |
| 2     | /ifd/xmp/exif:gpssatellites |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System. GPS. satélites](../properties/props-system-gps-satellites.md)
</dt> </dl>

 

 
