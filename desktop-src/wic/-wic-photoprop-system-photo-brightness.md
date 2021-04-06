---
description: La Directiva de metadatos de fotos para la propiedad System. Photo. Brightness.
ms.assetid: 3fd73845-f1d9-468c-abf8-081109880974
title: Directiva de metadatos de foto de System. Photo. Brightness
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acd7328b4d40b8d1582dcc17b317b706b2695c73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002794"
---
# <a name="systemphotobrightness-photo-metadata-policy"></a>Directiva de metadatos de foto de System. Photo. Brightness

La Directiva de metadatos de fotos para la propiedad [System. Photo. Brightness](../properties/props-system-photo-aperture.md) .

### <a name="pkey"></a>PKEY

Brillo de la \_ foto PKEY \_

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

Sí

### <a name="input-type"></a>Tipo de entrada

Doble

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Este valor se genera a partir de System. Photo. ApertureNumerator y System. Photo. ApertureDenominator. No se puede escribir directamente. Se reconcilian los valores de los distintos esquemas.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /app1/IFD/Exif/{ushort = 37379} |             |
| 2     | /xmp/exif:BrightnessValue     |             |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /app1/IFD/Exif/{ushort = 37379} |             |
| 2     | /xmp/exif:BrightnessValue     |             |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                          |
|-------|-------------------------------|
| 1     | /app1/IFD/Exif/{ushort = 37379} |
| 2     | /xmp/exif:brightnessvalue     |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /IFD/Exif/{ushort = 37379}      |             |
| 2     | /ifd/xmp/exif:BrightnessValue |             |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /IFD/Exif/{ushort = 37379}      |             |
| 2     | /ifd/xmp/exif:BrightnessValue |             |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                          |
|-------|-------------------------------|
| 1     | /IFD/Exif/{ushort = 37379}      |
| 2     | /ifd/xmp/exif:brightnessvalue |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System. Photo. Brightness](../properties/props-system-photo-aperture.md)
</dt> </dl>

 

 
