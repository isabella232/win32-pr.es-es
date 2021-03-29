---
description: La Directiva de metadatos de la fotografía para la propiedad System. GPS. DestBearingRef.
ms.assetid: d1c8b3cc-ed52-43ca-a0ba-045a2c5fe274
title: Directiva de metadatos de la foto System. GPS. DestBearingRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f00d3083459fe365fc54e81dc485ddd26887a46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277620"
---
# <a name="systemgpsdestbearingref-photo-metadata-policy"></a>Directiva de metadatos de la foto System. GPS. DestBearingRef

La Directiva de metadatos de la fotografía para la propiedad [System. GPS. DestBearingRef](../properties/props-system-gps-destbearingref.md) .

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ DestBearingRef

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



| Pedido | Ruta                        | Formato de disco |
|-------|-----------------------------|-------------|
| 1     | /app1/IFD/GPS/{ushort = 23}   | ascii       |
| 2     | /xmp/exif:GPSDestBearingRef | unicode     |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                        | Formato de disco |
|-------|-----------------------------|-------------|
| 1     | /app1/IFD/GPS/{ushort = 23}   | ascii       |
| 2     | /xmp/exif:GPSDestBearingRef | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                        |
|-------|-----------------------------|
| 1     | /app1/IFD/GPS/{ushort = 23}   |
| 2     | /xmp/exif:gpsdestbearingref |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                            | Formato de disco |
|-------|---------------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 23}            | ascii       |
| 2     | /ifd/xmp/exif:GPSDestBearingRef | unicode     |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                            | Formato de disco |
|-------|---------------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 23}            | ascii       |
| 2     | /ifd/xmp/exif:GPSDestBearingRef | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| orden | path                            |
|-------|---------------------------------|
| 1     | /IFD/GPS/{ushort = 23}            |
| 2     | /ifd/xmp/exif:gpsdestbearingref |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System. GPS. DestBearingRef](../properties/props-system-gps-destbearingref.md)
</dt> </dl>

 

 
