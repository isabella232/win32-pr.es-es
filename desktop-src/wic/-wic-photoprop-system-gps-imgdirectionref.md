---
description: La Directiva de metadatos de la fotografía para la propiedad System. GPS. ImgDirectionRef.
ms.assetid: 74ae0989-6d53-4d72-abe9-84f40c0c884a
title: Directiva de metadatos de la foto System. GPS. ImgDirectionRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80276ca8d1981935004dbec49fef588fcde330ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278837"
---
# <a name="systemgpsimgdirectionref-photo-metadata-policy"></a>Directiva de metadatos de la foto System. GPS. ImgDirectionRef

La Directiva de metadatos de la fotografía para la propiedad [System. GPS. ImgDirectionRef](../properties/props-system-gps-imgdirectionref.md) .

### <a name="pkey"></a>PKEY

PKEY \_ GPS. ImgDirectionRef

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

No

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de salida

VT \_ LPWStr

### <a name="input-type"></a>Tipo de entrada

\_Se prefiere VT LPWStr, pero \_ también se acepta VT LPSTR.

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Se reconcilian los valores de los distintos esquemas.

### <a name="jpeg-policies"></a>Directivas JPEG

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                         | Formato de disco |
|-------|------------------------------|-------------|
| 1     | /app1/IFD/GPS/{ushort = 16}    | ascii       |
| 2     | /xmp/exif:GPSImgDirectionRef | unicode     |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                         | Formato de disco |
|-------|------------------------------|-------------|
| 1     | /app1/IFD/GPS/{ushort = 16}    | ascii       |
| 2     | /xmp/exif:GPSImgDirectionRef | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                         |
|-------|------------------------------|
| 1     | /app1/IFD/GPS/{ushort = 16}    |
| 2     | /xmp/exif:gpsimgdirectionref |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                             | Formato de disco |
|-------|----------------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 16}             | ascii       |
| 2     | /ifd/xmp/exif:GPSImgDirectionRef | unicode     |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                             | Formato de disco |
|-------|----------------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 16}             | ascii       |
| 2     | /ifd/xmp/exif:GPSImgDirectionRef | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                             |
|-------|----------------------------------|
| 1     | /IFD/GPS/{ushort = 16}             |
| 2     | /ifd/xmp/exif:gpsimgdirectionref |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System. GPS. ImgDirectionRef](../properties/props-system-gps-imgdirectionref.md)
</dt> </dl>

 

 
