---
description: La Directiva de metadatos de la fotografía para la propiedad System. GPS. DestDistanceRef.
ms.assetid: eb671f34-7366-4182-b72e-0dd7830751e0
title: Directiva de metadatos de la foto System. GPS. DestDistanceRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bba6e04bee00aaed868fcc02059403fe479f8cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688493"
---
# <a name="systemgpsdestdistanceref-photo-metadata-policy"></a>Directiva de metadatos de la foto System. GPS. DestDistanceRef

La Directiva de metadatos de la fotografía para la propiedad [System. GPS. DestDistanceRef](../properties/props-system-gps-destdistanceref.md) .

### <a name="pkey"></a>PKEY

PKEY \_ DestDistanceRef

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

No

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de salida

VT \_ LPWStr

### <a name="input-type"></a>Tipo de entrada

\_Se acepta VT LPWStr o VT \_ LPSTR.

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Se reconcilian los valores de los distintos esquemas.

### <a name="jpeg-policies"></a>Directivas JPEG

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                         | Formato de disco |
|-------|------------------------------|-------------|
| 1     | /app1/IFD/GPS/{ushort = 25}    | ascii       |
| 2     | /xmp/exif:GPSDestDistanceRef | unicode     |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                         | Formato de disco |
|-------|------------------------------|-------------|
| 1     | /app1/IFD/GPS/{ushort = 25}    | ascii       |
| 2     | /xmp/exif:GPSDestDistanceRef | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                         |
|-------|------------------------------|
| 1     | /app1/IFD/GPS/{ushort = 25}    |
| 2     | /xmp/exif:gpsdestdistanceref |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                             | Formato de disco |
|-------|----------------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 25}             | ascii       |
| 2     | /ifd/xmp/exif:GPSDestDistanceRef | unicode     |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                             | Formato de disco |
|-------|----------------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 25}             | ascii       |
| 2     | /ifd/xmp/exif:GPSDestDistanceRef | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                             |
|-------|----------------------------------|
| 1     | /IFD/GPS/{ushort = 25}             |
| 2     | /ifd/xmp/exif:gpsdestdistanceref |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System. GPS. DestDistanceRef](../properties/props-system-gps-destdistanceref.md)
</dt> </dl>

 

 
