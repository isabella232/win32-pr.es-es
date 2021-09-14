---
description: Directiva de metadatos de fotos para la propiedad System.GPS.DestBearing.
ms.assetid: ccc31b3d-27fd-4a8c-a304-852cf6114ec5
title: Directiva de metadatos de fotos System.GPS.DestBearing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01a084a0633579afe646403fb4dcad0ca8a1b9ff
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127256491"
---
# <a name="systemgpsdestbearing-photo-metadata-policy"></a>Directiva de metadatos de fotos System.GPS.DestBearing

Directiva de metadatos de fotos para [la propiedad System.GPS.DestBearing.](../properties/props-system-gps-destbearing.md)

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ DestBearing

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

Sí

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de salida

VT \_ R8

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Este valor se puede escribir en System.GPS.DestBearingNumerator y System.GPS.DestBearingDenominator. No se puede escribir directamente. Los valores de esquemas diferentes se concilian.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta de acceso                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=24} |             |
| 2     | /xmp/exif:GPSDestBearing  |             |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Ruta de acceso                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=24} |             |
| 2     | /xmp/exif:GPSDestBearing  |             |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=24} |             |
| 2     | /xmp/exif:gpsdestbearing  |             |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta de acceso                         | Formato de disco |
|-------|------------------------------|-------------|
| 1     | /ifd/gps/{ushort=24}         |             |
| 2     | /ifd/xmp/exif:GPSDestBearing |             |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Ruta de acceso                         | Formato de disco |
|-------|------------------------------|-------------|
| 1     | /ifd/gps/{ushort=24}         |             |
| 2     | /ifd/xmp/exif:GPSDestBearing |             |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                         |
|-------|------------------------------|
| 1     | /ifd/gps/{ushort=24}         |
| 2     | /ifd/xmp/exif:gpsdestbearing |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System.GPS.DestBearing](../properties/props-system-gps-destbearing.md)
</dt> </dl>

 

 
