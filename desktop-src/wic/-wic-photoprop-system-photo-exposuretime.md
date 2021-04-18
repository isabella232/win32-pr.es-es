---
description: La Directiva de metadatos de fotos para la propiedad System. Photo. ExposureTime.
ms.assetid: 26f6ff27-b326-46f8-b4be-b091acbec575
title: Directiva de metadatos de la foto de System. Photo. ExposureTime
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea9078befd0cbc26272ff14ae023b1b22cb4f0f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678098"
---
# <a name="systemphotoexposuretime-photo-metadata-policy"></a>Directiva de metadatos de la foto de System. Photo. ExposureTime

La Directiva de metadatos de fotos para la propiedad [System. Photo. ExposureTime](../properties/props-system-photo-exposuretime.md) .

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ ExposureTime

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

Sí

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de salida

VT \_ R8

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Este valor se genera a partir de System. Photo. ExposureTimeNumerator y System. Photo. ExposureTimeDenominator. No se puede escribir directamente. Se reconcilian los valores de los distintos esquemas.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /app1/IFD/Exif/{ushort = 33434} |             |
| 2     | /xmp/exif:ExposureTime        |             |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /app1/IFD/Exif/{ushort = 33434} |             |
| 2     | /xmp/exif:ExposureTime        |             |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                          |
|-------|-------------------------------|
| 1     | /app1/IFD/Exif/{ushort = 33434} |
| 2     | /xmp/exif:exposuretime        |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                       | Formato de disco |
|-------|----------------------------|-------------|
| 1     | /IFD/Exif/{ushort = 33434}   |             |
| 2     | /ifd/xmp/exif:ExposureTime |             |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                       | Formato de disco |
|-------|----------------------------|-------------|
| 1     | /IFD/Exif/{ushort = 33434}   |             |
| 2     | /ifd/xmp/exif:ExposureTime |             |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                       |
|-------|----------------------------|
| 1     | /IFD/Exif/{ushort = 33434}   |
| 2     | /ifd/xmp/exif:exposuretime |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System. Photo. ExposureTime](../properties/props-system-photo-exposuretime.md)
</dt> </dl>

 

 
