---
title: Directiva de metadatos de la foto System. Image. HorizontalResolution
description: La Directiva de metadatos de la fotografía para la propiedad System. Image. HorizontalResolution.
ms.assetid: 1fe73c50-4179-4ea4-be1c-9e103fb65d59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ade406e644524fea84ef6baf957aed661d2adf07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103814246"
---
# <a name="systemimagehorizontalresolution-photo-metadata-policy"></a>Directiva de metadatos de la foto System. Image. HorizontalResolution

La Directiva de metadatos de la fotografía para la propiedad [System. Image. HorizontalResolution](../properties/props-system-image-horizontalresolution.md) .

### <a name="pkey"></a>PKEY

PKEY \_ \_ rehorizontalresolution de imagen

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

Sí.

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de salida

VT \_ R8

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

El sistema genera este valor y no se puede escribir directamente. Se reconcilian los valores de los distintos esquemas.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                   | Formato de disco |
|-------|------------------------|-------------|
| 1     | /app1/IFD/{ushort = 282} |             |
| 2     | /xmp/tiff:XResolution  |             |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                        | Formato de disco |
|-------|-----------------------------|-------------|
| 1     | /app1/IFD/Exif/{ushort = 282} |             |
| 2     | /xmp/tiff:xresolution       |             |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /IFD/Exif/{ushort = 282}    |             |
| 2     | /ifd/xmp/tiff:XResolution |             |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /IFD/Exif/{ushort = 282}    |             |
| 2     | /ifd/xmp/tiff:xresolution |             |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System. Image. HorizontalResolution](../properties/props-system-image-horizontalresolution.md)
</dt> </dl>

 

 
