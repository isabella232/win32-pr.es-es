---
description: Directiva de metadatos de fotos para la propiedad System.GPS.ImgDirectionRef.
ms.assetid: 74ae0989-6d53-4d72-abe9-84f40c0c884a
title: Directiva de metadatos de fotos System.GPS.ImgDirectionRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e735f91133d4ec473537f063e30d2d48f801a99f8f6bc80fa228b98a9bd95437
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117667902"
---
# <a name="systemgpsimgdirectionref-photo-metadata-policy"></a>Directiva de metadatos de fotos System.GPS.ImgDirectionRef

Directiva de metadatos de fotos para [la propiedad System.GPS.ImgDirectionRef.](../properties/props-system-gps-imgdirectionref.md)

### <a name="pkey"></a>Pkey

PKEY \_ GPS. ImgDirectionRef

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

No

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de salida

VT \_ LPWSTR

### <a name="input-type"></a>Tipo de entrada

Se \_ prefiere VT LPWSTR, pero también se \_ acepta VT LPSTR.

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Los valores de esquemas diferentes se concilian.

### <a name="jpeg-policies"></a>Directivas JPEG

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta de acceso                         | Formato de disco |
|-------|------------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=16}    | ascii       |
| 2     | /xmp/exif:GPSImgDirectionRef | unicode     |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Ruta de acceso                         | Formato de disco |
|-------|------------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=16}    | ascii       |
| 2     | /xmp/exif:GPSImgDirectionRef | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                         |
|-------|------------------------------|
| 1     | /app1/ifd/gps/{ushort=16}    |
| 2     | /xmp/exif:gpsimgdirectionref |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta de acceso                             | Formato de disco |
|-------|----------------------------------|-------------|
| 1     | /ifd/gps/{ushort=16}             | ascii       |
| 2     | /ifd/xmp/exif:GPSImgDirectionRef | unicode     |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Ruta de acceso                             | Formato de disco |
|-------|----------------------------------|-------------|
| 1     | /ifd/gps/{ushort=16}             | ascii       |
| 2     | /ifd/xmp/exif:GPSImgDirectionRef | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                             |
|-------|----------------------------------|
| 1     | /ifd/gps/{ushort=16}             |
| 2     | /ifd/xmp/exif:gpsimgdirectionref |



 

## <a name="remarks"></a>Comentarios

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System.GPS.ImgDirectionRef](../properties/props-system-gps-imgdirectionref.md)
</dt> </dl>

 

 
