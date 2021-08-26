---
description: Directiva de metadatos de fotos para la propiedad System.GPS.Differential.
ms.assetid: 330d1f88-5f54-4e29-b57f-eb7112203e04
title: Directiva de metadatos de fotos System.GPS.Differential
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 728df47fd8e6e9748b7208b79444ba8fa257fa49c92587df199441de941f4fdd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119931805"
---
# <a name="systemgpsdifferential-photo-metadata-policy"></a>Directiva de metadatos de fotos System.GPS.Differential

Directiva de metadatos de fotos para [la propiedad System.GPS.Differential.](../properties/props-system-gps-differential.md)

### <a name="pkey"></a>Pkey

Diferencial gps PKEY \_ \_

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

No

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de salida

VT \_ UI2

### <a name="input-propvariant-type"></a>Tipo PROPVARIANT de entrada

Se \_ aceptan VT UI1, VT \_ UI2 y VT \_ UI4.

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Los valores de esquemas diferentes se concilian.

### <a name="jpeg-policies"></a>Directivas JPEG

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta de acceso                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=30} | ushort      |
| 2     | /xmp/exif:GPSDifferential | unicode     |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Ruta de acceso                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=30} | ushort      |
| 2     | /xmp/exif:GPSDifferential | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                      |
|-------|---------------------------|
| 1     | /app1/ifd/gps/{ushort=30} |
| 2     | /xmp/exif:gpsdifferential |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta de acceso                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /ifd/gps/{ushort=30}          | ushort      |
| 2     | /ifd/xmp/exif:GPSDifferential | unicode     |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Ruta de acceso                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /ifd/gps/{ushort=30}          | ushort      |
| 2     | /ifd/xmp/exif:GPSDifferential | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                          |
|-------|-------------------------------|
| 1     | /ifd/gps/{ushort=30}          |
| 2     | /ifd/xmp/exif:gpsdifferential |



 

## <a name="remarks"></a>Comentarios

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System.GPS.Differential](../properties/props-system-gps-differential.md)
</dt> </dl>

 

 
