---
description: Directiva de metadatos de fotos para la propiedad System.GPS.DestBearingRef.
ms.assetid: d1c8b3cc-ed52-43ca-a0ba-045a2c5fe274
title: Directiva de metadatos de fotos System.GPS.DestBearingRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26ee4b984d0a759769b80be76b53499690673c7ec630c759aa0371b53ea9368f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119087856"
---
# <a name="systemgpsdestbearingref-photo-metadata-policy"></a>Directiva de metadatos de fotos System.GPS.DestBearingRef

Directiva de metadatos de fotos para [la propiedad System.GPS.DestBearingRef.](../properties/props-system-gps-destbearingref.md)

### <a name="pkey"></a>Pkey

PKEY \_ GPS \_ DestBearingRef

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

No

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de salida

VT \_ LPWSTR

### <a name="input-type"></a>Tipo de entrada

String.

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Los valores de esquemas diferentes se concilian.

### <a name="jpeg-policies"></a>Directivas JPEG

### <a name="read-paths"></a>Rutas de acceso de lectura



| Pedido | Ruta de acceso                        | Formato de disco |
|-------|-----------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=23}   | ascii       |
| 2     | /xmp/exif:GPSDestBearingRef | unicode     |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Ruta de acceso                        | Formato de disco |
|-------|-----------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=23}   | ascii       |
| 2     | /xmp/exif:GPSDestBearingRef | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                        |
|-------|-----------------------------|
| 1     | /app1/ifd/gps/{ushort=23}   |
| 2     | /xmp/exif:gpsdestbearingref |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Rutas de acceso de lectura



| Pedido | Ruta de acceso                            | Formato de disco |
|-------|---------------------------------|-------------|
| 1     | /ifd/gps/{ushort=23}            | ascii       |
| 2     | /ifd/xmp/exif:GPSDestBearingRef | unicode     |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Ruta de acceso                            | Formato de disco |
|-------|---------------------------------|-------------|
| 1     | /ifd/gps/{ushort=23}            | ascii       |
| 2     | /ifd/xmp/exif:GPSDestBearingRef | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| orden | path                            |
|-------|---------------------------------|
| 1     | /ifd/gps/{ushort=23}            |
| 2     | /ifd/xmp/exif:gpsdestbearingref |



 

## <a name="remarks"></a>Comentarios

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System.GPS.DestBearingRef](../properties/props-system-gps-destbearingref.md)
</dt> </dl>

 

 
