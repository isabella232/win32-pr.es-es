---
description: Directiva de metadatos de fotos para la propiedad System.GPS.DestDistanceRef.
ms.assetid: eb671f34-7366-4182-b72e-0dd7830751e0
title: Directiva de metadatos de fotos System.GPS.DestDistanceRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bba6e04bee00aaed868fcc02059403fe479f8cd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127267375"
---
# <a name="systemgpsdestdistanceref-photo-metadata-policy"></a>Directiva de metadatos de fotos System.GPS.DestDistanceRef

Directiva de metadatos de fotos para [la propiedad System.GPS.DestDistanceRef.](../properties/props-system-gps-destdistanceref.md)

### <a name="pkey"></a>PKEY

PKEY \_ DestDistanceRef

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

No

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de salida

VT \_ LPWSTR

### <a name="input-type"></a>Tipo de entrada

Se \_ acepta VT LPWSTR o \_ VT LPSTR.

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Los valores de esquemas diferentes se concilian.

### <a name="jpeg-policies"></a>Directivas JPEG

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Path                         | Formato de disco |
|-------|------------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=25}    | ascii       |
| 2     | /xmp/exif:GPSDestDistanceRef | unicode     |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Path                         | Formato de disco |
|-------|------------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=25}    | ascii       |
| 2     | /xmp/exif:GPSDestDistanceRef | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Path                         |
|-------|------------------------------|
| 1     | /app1/ifd/gps/{ushort=25}    |
| 2     | /xmp/exif:gpsdestdistanceref |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Path                             | Formato de disco |
|-------|----------------------------------|-------------|
| 1     | /ifd/gps/{ushort=25}             | ascii       |
| 2     | /ifd/xmp/exif:GPSDestDistanceRef | unicode     |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Path                             | Formato de disco |
|-------|----------------------------------|-------------|
| 1     | /ifd/gps/{ushort=25}             | ascii       |
| 2     | /ifd/xmp/exif:GPSDestDistanceRef | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Path                             |
|-------|----------------------------------|
| 1     | /ifd/gps/{ushort=25}             |
| 2     | /ifd/xmp/exif:gpsdestdistanceref |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System.GPS.DestDistanceRef](../properties/props-system-gps-destdistanceref.md)
</dt> </dl>

 

 
