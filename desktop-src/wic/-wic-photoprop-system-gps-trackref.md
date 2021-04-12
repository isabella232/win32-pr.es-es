---
description: La Directiva de metadatos de la fotografía para la propiedad System. GPS. TrackRef.
ms.assetid: e6912177-8add-4520-b396-c28060b359c7
title: Directiva de metadatos de la foto System. GPS. TrackRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95fc63de6eaffd697798c08ff74a46c3d15c7818
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279375"
---
# <a name="systemgpstrackref-photo-metadata-policy"></a>Directiva de metadatos de la foto System. GPS. TrackRef

La Directiva de metadatos de la fotografía para la propiedad [System. GPS. TrackRef](../properties/props-system-gps-trackref.md) .

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ TrackRef

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

No

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de salida

VT \_ LPWStr

### <a name="input-type"></a>Tipo de entrada

String

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Se reconcilian los valores de los distintos esquemas.

### <a name="jpeg-policies"></a>Directivas JPEG

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /app1/IFD/GPS/{ushort = 14} | ascii       |
| 2     | /xmp/exif:GPSTrackRef     | unicode     |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /app1/IFD/GPS/{ushort = 14} | ascii       |
| 2     | /xmp/exif:GPSTrackRef     | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                      |
|-------|---------------------------|
| 1     | /app1/IFD/GPS/{ushort = 14} |
| 2     | /xmp/exif:gpstrackref     |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 14}      | ascii       |
| 2     | /ifd/xmp/exif:GPSTrackRef | unicode     |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 14}      | ascii       |
| 2     | /ifd/xmp/exif:GPSTrackRef | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                      |
|-------|---------------------------|
| 1     | /IFD/GPS/{ushort = 14}      |
| 2     | /ifd/xmp/exif:gpstrackref |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System. GPS. TrackRef](../properties/props-system-gps-trackref.md)
</dt> </dl>

 

 
