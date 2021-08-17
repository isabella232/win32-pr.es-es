---
description: Directiva de metadatos de fotos para la propiedad System.Photo.Orientation.
ms.assetid: 27e6d4f5-39d5-4cb4-88bc-b0d61ccaa2f3
title: Directiva de metadatos de fotos System.Photo.Orientation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87f9496942e6be971e0e047596125669fc9112cf82bce6eb02ec7e1cdbddc4de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119087071"
---
# <a name="systemphotoorientation-photo-metadata-policy"></a>Directiva de metadatos de fotos System.Photo.Orientation

Directiva de metadatos de fotos para [la propiedad System.Photo.Orientation.](../properties/props-system-photo-meteringmode.md)

### <a name="pkey"></a>Pkey

Orientación de la foto PKEY \_ \_

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

No

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de salida

VT \_ UI2

### <a name="input-type"></a>Tipo de entrada

UShort

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Los valores de esquemas diferentes se concilian.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta de acceso                   | Formato de disco |
|-------|------------------------|-------------|
| 1     | /app1/ifd/{ushort=274} | ushort      |
| 2     | /xmp/tiff:Orientation  | unicode     |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Ruta de acceso                   | Formato de disco |
|-------|------------------------|-------------|
| 1     | /app1/ifd/{ushort=274} | ushort      |
| 2     | /xmp/tiff:Orientation  | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                   |
|-------|------------------------|
| 1     | /app1/ifd/{ushort=274} |
| 2     | /xmp/tiff:orientation  |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta de acceso                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /ifd/{ushort=274}         | ushort      |
| 2     | /ifd/xmp/tiff:Orientation | unicode     |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Ruta de acceso                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /ifd/{ushort=274}         | ushort      |
| 2     | /ifd/xmp/tiff:Orientation | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                      |
|-------|---------------------------|
| 1     | /ifd/{ushort=274}         |
| 2     | /ifd/xmp/tiff:orientation |



 

## <a name="remarks"></a>Comentarios

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System.Photo.Orientation](../properties/props-system-photo-meteringmode.md)
</dt> </dl>

 

 
