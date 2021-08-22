---
description: Directiva de metadatos de fotos para la propiedad System.Photo.SpeedSpeed.
ms.assetid: f320944c-978d-4a3c-9bf8-5c5652123e29
title: Directiva de metadatos de fotos System.Photo.Photo.Speed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ad11550a19cd043fd5d182b2cf508aec3e26c64a0dc2ee1d1c24576ebf18f8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118710104"
---
# <a name="systemphotoshutterspeed-photo-metadata-policy"></a>Directiva de metadatos de fotos System.Photo.Photo.Speed

Directiva de metadatos de fotos para [la propiedad System.Photo.SpeedSpeed.](../properties/props-system-photo-shutterspeed.md)

### <a name="pkey"></a>Pkey

PKEY \_ \_ PhotoSpeed

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

Sí

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de salida

VT \_ R8

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Este valor se genera a partir de System.Photo.SpeedNumerator y System.Photo.SpeedDenominator. No se puede escribir directamente. Se concilian los valores de esquemas diferentes.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Rutas de acceso de lectura



| Pedido | Ruta de acceso                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=37377} |             |
| 2     | /xmp/exif:SpeedValue   |             |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Ruta de acceso                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=37377} |             |
| 2     | /xmp/exif:SpeedValue   |             |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                          |
|-------|-------------------------------|
| 1     | /app1/ifd/exif/{ushort=37377} |
| 2     | /xmp/exif:speedvalue   |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Rutas de acceso de lectura



| Pedido | Ruta de acceso                            | Formato de disco |
|-------|---------------------------------|-------------|
| 1     | /ifd/exif/{ushort=37377}        |             |
| 2     | /ifd/xmp/exif:SpeedValue |             |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Ruta de acceso                            | Formato de disco |
|-------|---------------------------------|-------------|
| 1     | /ifd/exif/{ushort=37377}        |             |
| 2     | /ifd/xmp/exif:SpeedValue |             |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                            |
|-------|---------------------------------|
| 1     | /ifd/exif/{ushort=37377}        |
| 2     | /ifd/xmp/exif:speedvalue |



 

## <a name="remarks"></a>Comentarios

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System.Photo.Speed](../properties/props-system-photo-shutterspeed.md)
</dt> </dl>

 

 
