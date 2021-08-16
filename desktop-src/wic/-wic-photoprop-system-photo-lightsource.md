---
description: Directiva de metadatos de fotos para la propiedad System.Photo.LightSource.
ms.assetid: 051a49ad-bb4c-459f-ae52-dc359a03a14a
title: Directiva de metadatos de fotos System.Photo.LightSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 195d165a6a929c8e0b4bf2dd165a5f22068a8b75e8ea4dfcddb5b8979900b035
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118204727"
---
# <a name="systemphotolightsource-photo-metadata-policy"></a>Directiva de metadatos de fotos System.Photo.LightSource

Directiva de metadatos de fotos para [la propiedad System.Photo.LightSource.](../properties/props-system-photo-lightsource.md)

### <a name="pkey"></a>Pkey

PKEY \_ Photo \_ LightSource

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



| Pedido | Ruta de acceso                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=37384} | ushort      |
| 2     | /xmp/exif:LightSource         | unicode     |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Ruta de acceso                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=37384} | ushort      |
| 2     | /xmp/exif:LightSource         | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                          |
|-------|-------------------------------|
| 1     | /app1/ifd/exif/{ushort=37384} |
| 2     | /xmp/exif:lightsource         |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta de acceso                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /ifd/exif/{ushort=37384}  | ushort      |
| 2     | /ifd/xmp/exif:LightSource | unicode     |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Ruta de acceso                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /ifd/exif/{ushort=37384}  | ushort      |
| 2     | /ifd/xmp/exif:LightSource | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                      |
|-------|---------------------------|
| 1     | /ifd/exif/{ushort=37384}  |
| 2     | /ifd/xmp/exif:lightsource |



 

## <a name="remarks"></a>Comentarios

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System.Photo.LightSource](../properties/props-system-photo-lightsource.md)
</dt> </dl>

 

 
