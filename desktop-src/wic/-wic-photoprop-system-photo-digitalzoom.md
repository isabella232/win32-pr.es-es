---
description: Directiva de metadatos de fotos para la propiedad System.Photo.DigitalZoom.
ms.assetid: 22a69d3e-4ec3-4652-b4bb-dfcfffc2322b
title: Directiva de metadatos de fotos System.Photo.DigitalZoom
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19dfaf2838c8f321b1406d951fcc335076bcdfc00e3a17de0954f1a62022570e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118205381"
---
# <a name="systemphotodigitalzoom-photo-metadata-policy"></a>Directiva de metadatos de fotos System.Photo.DigitalZoom

Directiva de metadatos de fotos para [la propiedad System.Photo.DigitalZoom.](../properties/props-system-photo-digitalzoom.md)

### <a name="pkey"></a>Pkey

PKEY \_ Photo \_ DigitalZoom

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

Sí

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de salida

VT \_ R8

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Este valor se genera a partir de System.Photo.DigitalZoomNumerator y System.Photo.DigitalZoomDenominator. No se puede escribir directamente. Los valores de esquemas diferentes se concilian.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Rutas de acceso de lectura



| Pedido | Ruta de acceso                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=41988} |             |
| 2     | /xmp/exif:DigitalZoomRatio    |             |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Ruta de acceso                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=41988} |             |
| 2     | /xmp/exif:DigitalZoomRatio    |             |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                          |
|-------|-------------------------------|
| 1     | /app1/ifd/exif/{ushort=41988} |
| 2     | /xmp/exif:digitalzoomratio    |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Rutas de acceso de lectura



| Pedido | Ruta de acceso                           | Formato de disco |
|-------|--------------------------------|-------------|
| 1     | /ifd/exif/{ushort=41988}       |             |
| 2     | /ifd/xmp/exif:DigitalZoomRatio |             |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Ruta de acceso                           | Formato de disco |
|-------|--------------------------------|-------------|
| 1     | /ifd/exif/{ushort=41988}       |             |
| 2     | /ifd/xmp/exif:DigitalZoomRatio |             |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                           |
|-------|--------------------------------|
| 1     | /ifd/exif/{ushort=41988}       |
| 2     | /ifd/xmp/exif:digitalzoomratio |



 

## <a name="remarks"></a>Comentarios

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System.Photo.DigitalZoom](../properties/props-system-photo-digitalzoom.md)
</dt> </dl>

 

 
