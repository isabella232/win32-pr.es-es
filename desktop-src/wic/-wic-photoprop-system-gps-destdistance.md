---
description: Directiva de metadatos de fotos para la propiedad System.GPS.DestDistance.
ms.assetid: 1bd72acb-f462-454d-aec2-72d5b4517de3
title: Directiva de metadatos de fotos System.GPS.DestDistance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecc71c89ae6270f5babf08637f54baaf2cb57aae
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127256478"
---
# <a name="systemgpsdestdistance-photo-metadata-policy"></a>Directiva de metadatos de fotos System.GPS.DestDistance

Directiva de metadatos de fotos para [la propiedad System.GPS.DestDistance.](../properties/props-system-gps-destdistance.md)

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ DestDistance

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

Sí

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de salida

VT \_ R8

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Este valor se genera a partir de System.GPS.DestDistanceNumerator y System.GPS.DestDistanceDenominator. No se puede escribir directamente. Los valores de esquemas diferentes se concilian.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta de acceso                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=26} |             |
| 2     | /xmp/exif:GPSDestDistance |             |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Ruta de acceso                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=26} |             |
| 2     | /xmp/exif:GPSDestDistance |             |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                      |
|-------|---------------------------|
| 1     | /app1/ifd/gps/{ushort=26} |
| 2     | /xmp/exif:gpsdestdistance |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta de acceso                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /ifd/gps/{ushort=26}          |             |
| 2     | /ifd/xmp/exif:GPSDestDistance |             |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Ruta de acceso                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /ifd/gps/{ushort=26}          |             |
| 2     | /ifd/xmp/exif:GPSDestDistance |             |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                          |
|-------|-------------------------------|
| 1     | /ifd/gps/{ushort=26}          |
| 2     | /ifd/xmp/exif:gpsdestdistance |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System.GPS.DestDistance](../properties/props-system-gps-destdistance.md)
</dt> </dl>

 

 
