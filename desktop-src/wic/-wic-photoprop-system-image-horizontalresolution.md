---
title: Directiva de metadatos de fotos System.Image.HorizontalResolution
description: Directiva de metadatos de fotos para la propiedad System.Image.HorizontalResolution.
ms.assetid: 1fe73c50-4179-4ea4-be1c-9e103fb65d59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 577c30c83110d2c486fcc36161965321faa7da5bf2f4932562296a4b5ff1d592
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117667615"
---
# <a name="systemimagehorizontalresolution-photo-metadata-policy"></a>Directiva de metadatos de fotos System.Image.HorizontalResolution

Directiva de metadatos de fotos para [la propiedad System.Image.HorizontalResolution.](../properties/props-system-image-horizontalresolution.md)

### <a name="pkey"></a>Pkey

Imagen PKEY \_ \_ HorizontalResolution

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

Sí.

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de salida

VT \_ R8

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

El sistema genera este valor y no se puede escribir directamente. Los valores de esquemas diferentes se concilian.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta de acceso                   | Formato de disco |
|-------|------------------------|-------------|
| 1     | /app1/ifd/{ushort=282} |             |
| 2     | /xmp/tiff:XResolution  |             |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                        | Formato de disco |
|-------|-----------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=282} |             |
| 2     | /xmp/tiff:xresolution       |             |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta de acceso                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /ifd/exif/{ushort=282}    |             |
| 2     | /ifd/xmp/tiff:XResolution |             |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /ifd/exif/{ushort=282}    |             |
| 2     | /ifd/xmp/tiff:xresolution |             |



 

## <a name="remarks"></a>Comentarios

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System.Image.HorizontalResolution](../properties/props-system-image-horizontalresolution.md)
</dt> </dl>

 

 
