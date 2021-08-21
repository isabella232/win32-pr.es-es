---
description: Directiva de metadatos de fotos para la propiedad System.Image.VerticalResolution.
ms.assetid: a58b7463-3572-4ca8-8299-93d92d2f06fb
title: Directiva de metadatos de fotos System.Image.VerticalResolution
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9962a00be34d227756d295e992174d6e80b6d058fc32af29ad9cde58a04ed07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118710288"
---
# <a name="systemimageverticalresolution-photo-metadata-policy"></a>Directiva de metadatos de fotos System.Image.VerticalResolution

Directiva de metadatos de fotos para [la propiedad System.Image.VerticalResolution.](../properties/props-system-image-verticalresolution.md)

### <a name="pkey"></a>Pkey

Imagen PKEY \_ \_ VerticalResolution

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
| 1     | /app1/ifd/{ushort=283} |             |
| 2     | /xmp/tiff:YResolution  |             |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                        |
|-------|-----------------------------|
| 1     | /app1/ifd/exif/{ushort=283} |
| 2     | /xmp/tiff:yresolution       |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta de acceso                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /ifd/exif/{ushort=283}    |             |
| 2     | /ifd/xmp/tiff:YResolution |             |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                      |
|-------|---------------------------|
| 1     | /ifd/exif/{ushort=283}    |
| 2     | /ifd/xmp/tiff:yresolution |



 

## <a name="remarks"></a>Comentarios

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System.Image.VerticalResolution](../properties/props-system-image-verticalresolution.md)
</dt> </dl>

 

 
