---
description: La Directiva de metadatos de la fotografía para la propiedad System. GPS. ImgDirection.
ms.assetid: c9a0f5de-4010-4251-a5d5-8728b7ae6d33
title: Directiva de metadatos de la foto System. GPS. ImgDirection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 013edd632f98f1359c4f3c04856b0409c70eaa56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716889"
---
# <a name="systemgpsimgdirection-photo-metadata-policy"></a>Directiva de metadatos de la foto System. GPS. ImgDirection

La Directiva de metadatos de la fotografía para la propiedad [System. GPS. ImgDirection](../properties/props-system-gps-imgdirection.md) .

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ ImgDirection

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

Sí

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de salida

VT \_ R8

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Este valor se puede escribir escribiendo en System. GPS. ImgDirectionNumerator y System. GPS. ImgDirectionDenominator. No se puede escribir directamente. Se reconcilian los valores de los distintos esquemas.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /app1/IFD/GPS/{ushort = 17} |             |
| 2     | /xmp/exif:GPSImgDirection |             |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /app1/IFD/GPS/{ushort = 17} |             |
| 2     | /xmp/exif:GPSImgDirection |             |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                      |
|-------|---------------------------|
| 1     | /app1/IFD/GPS/{ushort = 17} |
| 2     | /xmp/exif:gpsimgdirection |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 17}          |             |
| 2     | /ifd/xmp/exif:GPSImgDirection |             |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 17}          |             |
| 2     | /ifd/xmp/exif:GPSImgDirection |             |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                          |
|-------|-------------------------------|
| 1     | /IFD/GPS/{ushort = 17}          |
| 2     | /ifd/xmp/exif:gpsimgdirection |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System. GPS. ImgDirection](../properties/props-system-gps-imgdirection.md)
</dt> </dl>

 

 
