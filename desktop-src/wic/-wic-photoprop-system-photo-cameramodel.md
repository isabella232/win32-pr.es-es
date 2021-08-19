---
description: Directiva de metadatos de fotos para la propiedad System.Photo.CameraModel.
ms.assetid: ff85e6ee-dc75-45bc-a406-2290b012c22d
title: Directiva de metadatos de fotos System.Photo.CameraModel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e205d4d886d050e45b958f2ba0f06c6411584c4a96a717378f243e5d1dd4fae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119882055"
---
# <a name="systemphotocameramodel-photo-metadata-policy"></a>Directiva de metadatos de fotos System.Photo.CameraModel

Directiva de metadatos de fotos para [la propiedad System.Photo.CameraModel.](../properties/props-system-photo-cameramodel.md)

### <a name="pkey"></a>Pkey

PKEY \_ Photo \_ CameraModel

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

No

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de salida

VT \_ LPWSTR

### <a name="input-type"></a>Tipo de entrada

String.

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Los valores de esquemas diferentes se concilian.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Rutas de acceso de lectura



| Pedido | Ruta de acceso                   | Formato de disco |
|-------|------------------------|-------------|
| 1     | /app1/ifd/{ushort=272} | ascii       |
| 2     | /xmp/tiff:Model        | unicode     |
| 3     | /xmp/tiff:model        | unicode     |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Ruta de acceso                   | Formato de disco |
|-------|------------------------|-------------|
| 1     | /app1/ifd/{ushort=272} | ascii       |
| 2     | /xmp/tiff:Model        | unicode     |
| 3     | /xmp/tiff:model        | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                   |
|-------|------------------------|
| 1     | /app1/ifd/{ushort=272} |
| 2     | /xmp/tiff:Model        |
| 3     | /xmp/tiff:model        |



 

### <a name="tiff-policy"></a>Directiva TIFF

### <a name="read-paths"></a>Rutas de acceso de lectura



| Pedido | Ruta de acceso                | Formato de disco |
|-------|---------------------|-------------|
| 1     | /ifd/{ushort=272}   | ascii       |
| 2     | /ifd/xmp/tiff:Model | unicode     |
| 3     | /ifd/xmp/tiff:model | unicode     |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Ruta de acceso                | Formato de disco |
|-------|---------------------|-------------|
| 1     | /ifd/{ushort=272}   | ascii       |
| 2     | /ifd/xmp/tiff:Model | unicode     |
| 3     | /ifd/xmp/tiff:model | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                |
|-------|---------------------|
| 1     | /ifd/{ushort=272}   |
| 2     | /ifd/xmp/tiff:Model |
| 3     | /ifd/xmp/tiff:model |



 

## <a name="remarks"></a>Comentarios

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System.Photo.CameraModel](../properties/props-system-photo-cameramodel.md)
</dt> </dl>

 

 
