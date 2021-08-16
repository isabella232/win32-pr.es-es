---
description: Directiva de metadatos de fotos para la propiedad System.Photo.PhotometricInterpretation.
ms.assetid: ff36b2c3-8763-4640-a049-b5880fd26929
title: Directiva de metadatos de fotos System.Photo.PhotometricInterpretation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5479c747e2a1cc60a1867a7dc5906e5c4710abf9da33b5328980e0188403ecd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118204689"
---
# <a name="systemphotophotometricinterpretation-photo-metadata-policy"></a>Directiva de metadatos de fotos System.Photo.PhotometricInterpretation

Directiva de metadatos de fotos para [la propiedad System.Photo.PhotometricInterpretation.](../properties/props-system-photo-photometricinterpretation.md)

### <a name="pkey"></a>Pkey

PKEY \_ Photo \_ PhotometricInterpretation

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

Sí

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de salida

VT \_ UI2

### <a name="input-type"></a>Tipo de entrada

UShort

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Se concilian los valores de esquemas diferentes.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Rutas de acceso de lectura



| Pedido | Ruta de acceso                                | Formato de disco |
|-------|-------------------------------------|-------------|
| 1     | /app1/ifd/{ushort=262}              | ushort      |
| 2     | /xmp/tiff:PhotometricInterpretation | unicode     |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Ruta de acceso                                | Formato de disco |
|-------|-------------------------------------|-------------|
| 1     | /app1/ifd/{ushort=262}              | ushort      |
| 2     | /xmp/tiff:PhotometricInterpretation | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                                |
|-------|-------------------------------------|
| 1     | /app1/ifd/{ushort=262}              |
| 2     | /xmp/tiff:photometricinterpretation |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Rutas de acceso de lectura



| Pedido | Ruta de acceso                                    | Formato de disco |
|-------|-----------------------------------------|-------------|
| 1     | /ifd/{ushort=262}                       | ushort      |
| 2     | /ifd/xmp/tiff:PhotometricInterpretation | unicode     |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Ruta de acceso                                    | Formato de disco |
|-------|-----------------------------------------|-------------|
| 1     | /ifd/{ushort=262}                       | ushort      |
| 2     | /ifd/xmp/tiff:PhotometricInterpretation | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                                    |
|-------|-----------------------------------------|
| 1     | /ifd/{ushort=262}                       |
| 2     | /ifd/xmp/tiff:photometricinterpretation |



 

## <a name="remarks"></a>Comentarios

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System.Photo.PhotometricInterpretation](../properties/props-system-photo-photometricinterpretation.md)
</dt> </dl>

 

 
