---
description: La Directiva de metadatos de la fotografía para la propiedad System. Image. VerticalResolution.
ms.assetid: a58b7463-3572-4ca8-8299-93d92d2f06fb
title: Directiva de metadatos de la foto de System. Image. VerticalResolution
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02e895ef9e1181a3ec40b474940c6dfaaa3e1329
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706397"
---
# <a name="systemimageverticalresolution-photo-metadata-policy"></a>Directiva de metadatos de la foto de System. Image. VerticalResolution

La Directiva de metadatos de la fotografía para la propiedad [System. Image. VerticalResolution](../properties/props-system-image-verticalresolution.md) .

### <a name="pkey"></a>PKEY

PKEY \_ Image \_ VerticalResolution

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
| 1     | /app1/IFD/{ushort = 283} |             |
| 2     | /xmp/tiff:YResolution  |             |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                        |
|-------|-----------------------------|
| 1     | /app1/IFD/Exif/{ushort = 283} |
| 2     | /xmp/tiff:yresolution       |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /IFD/Exif/{ushort = 283}    |             |
| 2     | /ifd/xmp/tiff:YResolution |             |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                      |
|-------|---------------------------|
| 1     | /IFD/Exif/{ushort = 283}    |
| 2     | /ifd/xmp/tiff:yresolution |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System. Image. VerticalResolution](../properties/props-system-image-verticalresolution.md)
</dt> </dl>

 

 
