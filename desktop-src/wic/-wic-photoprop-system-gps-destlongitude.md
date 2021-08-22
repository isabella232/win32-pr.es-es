---
description: Directiva de metadatos de fotos para la propiedad System.GPS.DestLongitude.
ms.assetid: 885a522d-e1bf-43fb-a996-97e725b6cf0c
title: Directiva de metadatos de fotos System.GPS.DestLongitude
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 917c65dbd580b00cf25603e04050386383967e3a70c1896405346652667ef5f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119087846"
---
# <a name="systemgpsdestlongitude-photo-metadata-policy"></a>Directiva de metadatos de fotos System.GPS.DestLongitude

Directiva de metadatos de fotos para [la propiedad System.GPS.DestLongitude.](../properties/props-system-gps-destlongitude.md)

### <a name="pkey"></a>Pkey

PKEY \_ GPS \_ DestLongitude

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

Sí

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de salida

VT \_ VECTOR \| VT \_ R8

### <a name="input-propvariant-type"></a>Tipo PROPVARIANT de entrada

VT \_ VECTOR \| VT \_ R8

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Este valor se genera a partir de System.GPS.DestLongitudeNumerator y System.GPS.DestLongitudeDenominator. No se puede escribir directamente. Los valores de esquemas diferentes se concilian.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Rutas de acceso de lectura



| Pedido | Ruta de acceso                       | Formato de disco |
|-------|----------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=22}  |             |
| 2     | /xmp/exif:GPSDestLongitude |             |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Ruta de acceso                       | Formato de disco |
|-------|----------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=22}  |             |
| 2     | /xmp/exif:GPSDestLongitude |             |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                       |
|-------|----------------------------|
| 1     | /app1/ifd/gps/{ushort=22}  |
| 2     | /xmp/exif:gpsdestlongitude |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Rutas de acceso de lectura



| Pedido | Ruta de acceso                           | Formato de disco |
|-------|--------------------------------|-------------|
| 1     | /ifd/gps/{ushort=22}           |             |
| 2     | /ifd/xmp/exif:GPSDestLongitude |             |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Ruta de acceso                           | Formato de disco |
|-------|--------------------------------|-------------|
| 1     | /ifd/gps/{ushort=22}           |             |
| 2     | /ifd/xmp/exif:GPSDestLongitude |             |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                           |
|-------|--------------------------------|
| 1     | /ifd/gps/{ushort=22}           |
| 2     | /ifd/xmp/exif:gpsdestlongitude |



 

## <a name="remarks"></a>Comentarios

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System.GPS.DestLongitude](../properties/props-system-gps-destlongitude.md)
</dt> </dl>

 

 
