---
description: Directiva de metadatos de fotos para la propiedad System.Photo.FocalLengthInSimo.
ms.assetid: 3ad63a7a-5ced-4e7f-a4a0-e1463f3d3fa3
title: Directiva de metadatos de fotos System.Photo.FocalLengthInArt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5df46f3e52c447cb7902fe3cce2da201dae16d9c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127467927"
---
# <a name="systemphotofocallengthinfilm-photo-metadata-policy"></a>Directiva de metadatos de fotos System.Photo.FocalLengthInArt

Directiva de metadatos de fotos [para la propiedad System.Photo.FocalLengthInSimo.](../properties/props-system-photo-focallengthinfilm.md)

### <a name="pkey"></a>PKEY

PKEY \_ FocalLengthInLíning

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

No

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de salida

VT \_ UI4

### <a name="input-type"></a>Tipo de entrada

UShort

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Los valores de esquemas diferentes se concilian.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Path                            | Formato de disco |
|-------|---------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=41989}   | ushort      |
| 2     | /xmp/exif:FocalLengthIn35mmAca | unicode     |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Path                            | Formato de disco |
|-------|---------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=41989}   | ushort      |
| 2     | /xmp/exif:FocalLengthIn35mmAca | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Path                            |
|-------|---------------------------------|
| 1     | /app1/ifd/exif/{ushort=41989}   |
| 2     | /xmp/exif:focallengthin35mmhin |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Path                                | Formato de disco |
|-------|-------------------------------------|-------------|
| 1     | /ifd/exif/{ushort=41989}            | ushort      |
| 2     | /ifd/xmp/exif:FocalLengthIn35mmAca | unicode     |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Path                                | Formato de disco |
|-------|-------------------------------------|-------------|
| 1     | /ifd/exif/{ushort=41989}            | ushort      |
| 2     | /ifd/xmp/exif:FocalLengthIn35mmAca | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Path                                |
|-------|-------------------------------------|
| 1     | /ifd/exif/{ushort=41989}            |
| 2     | /ifd/xmp/exif:focallengthin35mmmpl |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System.Photo.FocalLengthInLín](../properties/props-system-photo-focallengthinfilm.md)
</dt> </dl>

 

 
