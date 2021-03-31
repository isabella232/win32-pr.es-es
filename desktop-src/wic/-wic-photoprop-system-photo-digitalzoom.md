---
description: La Directiva de metadatos de fotos para la propiedad System. Photo. DigitalZoom.
ms.assetid: 22a69d3e-4ec3-4652-b4bb-dfcfffc2322b
title: Directiva de metadatos de la foto de System. Photo. DigitalZoom
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bf440e92243eb2102ac6abaa349ea83e58d9a2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361084"
---
# <a name="systemphotodigitalzoom-photo-metadata-policy"></a>Directiva de metadatos de la foto de System. Photo. DigitalZoom

La Directiva de metadatos de fotos para la propiedad [System. Photo. DigitalZoom](../properties/props-system-photo-digitalzoom.md) .

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ DigitalZoom

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

Sí

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de salida

VT \_ R8

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Este valor se genera a partir de System. Photo. DigitalZoomNumerator y System. Photo. DigitalZoomDenominator. No se puede escribir directamente. Se reconcilian los valores de los distintos esquemas.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /app1/IFD/Exif/{ushort = 41988} |             |
| 2     | /xmp/exif:DigitalZoomRatio    |             |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /app1/IFD/Exif/{ushort = 41988} |             |
| 2     | /xmp/exif:DigitalZoomRatio    |             |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                          |
|-------|-------------------------------|
| 1     | /app1/IFD/Exif/{ushort = 41988} |
| 2     | /xmp/exif:digitalzoomratio    |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                           | Formato de disco |
|-------|--------------------------------|-------------|
| 1     | /IFD/Exif/{ushort = 41988}       |             |
| 2     | /ifd/xmp/exif:DigitalZoomRatio |             |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                           | Formato de disco |
|-------|--------------------------------|-------------|
| 1     | /IFD/Exif/{ushort = 41988}       |             |
| 2     | /ifd/xmp/exif:DigitalZoomRatio |             |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                           |
|-------|--------------------------------|
| 1     | /IFD/Exif/{ushort = 41988}       |
| 2     | /ifd/xmp/exif:digitalzoomratio |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System. Photo. DigitalZoom](../properties/props-system-photo-digitalzoom.md)
</dt> </dl>

 

 
