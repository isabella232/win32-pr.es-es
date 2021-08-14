---
description: Directiva de metadatos de fotos para la propiedad System.Photo.FlashEnergy.
ms.assetid: d10a4de9-16fe-4920-aa7f-b2f95fb23045
title: Directiva de metadatos de fotos System.Photo.FlashEnergy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1faebdcd32eaae346a44de9d1fa19f6954cb9d74ee9d79a09645216660845d16
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118204934"
---
# <a name="systemphotoflashenergy-photo-metadata-policy"></a>Directiva de metadatos de fotos System.Photo.FlashEnergy

Directiva de metadatos de fotos para [la propiedad System.Photo.FlashEnergy.](../properties/props-system-photo-flashenergy.md)

### <a name="pkey"></a>Pkey

PKEY \_ Photo \_ FlashEnergy

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

Sí

### <a name="input-type"></a>Tipo de entrada

Doble

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Los valores de esquemas diferentes se concilian.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta de acceso                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=41483} |             |
| 2     | /xmp/exif:FlashEnergy         |             |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Ruta de acceso                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=41483} |             |
| 2     | /xmp/exif:FlashEnergy         |             |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                          |
|-------|-------------------------------|
| 1     | /app1/ifd/exif/{ushort=41483} |
| 2     | /xmp/exif:flashenergy         |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta de acceso                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /ifd/exif/{ushort=41483}  |             |
| 2     | /ifd/xmp/exif:FlashEnergy |             |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Ruta de acceso                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /ifd/exif/{ushort=41483}  |             |
| 2     | /ifd/xmp/exif:FlashEnergy |             |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                      |
|-------|---------------------------|
| 1     | /ifd/exif/{ushort=41483}  |
| 2     | /ifd/xmp/exif:flashenergy |



 

## <a name="remarks"></a>Comentarios

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System.Photo.FlashEnergy](../properties/props-system-photo-flashenergy.md)
</dt> </dl>

 

 
