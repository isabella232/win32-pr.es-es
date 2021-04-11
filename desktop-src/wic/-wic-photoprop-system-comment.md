---
description: La Directiva de metadatos de la fotografía para la propiedad System. comment.
ms.assetid: 02a6ac18-ad69-4880-a267-8330d648c0d9
title: Directiva de metadatos de la foto System. Comment
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db9d7526e05a72b073ac32bd8286a621b33ee62a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361318"
---
# <a name="systemcomment-photo-metadata-policy"></a>Directiva de metadatos de la foto System. Comment

La Directiva de metadatos de la fotografía para la propiedad [System. Comment](../properties/props-system-comment.md) .

### <a name="pkey"></a>PKEY

\_Comentario PKEY

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

No

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de salida

VT \_ LPWStr

### <a name="input-propvariant-type"></a>Tipo de PROPVARIANT de entrada

VT \_ LPWStr o VT \_ LPSTR

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Se reconcilian los valores de los distintos esquemas.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                                | Formato de disco    |
|-------|-------------------------------------|----------------|
| 1     | /app1/IFD/{ushort = 40092}            | \_bytes Unicode |
| 2     | /app1/IFD/{ushort = 37510}            | unicode        |
| 3     | /XMP/ <xmpalt> Exif: UserComment | unicode        |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                     | Formato de disco    |
|-------|--------------------------|----------------|
| 1     | /app1/IFD/{ushort = 40092} | \_bytes Unicode |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                          |
|-------|-------------------------------|
| 1     | /app1/IFD/{ushort = 40092}      |
| 2     | /app1/IFD/Exif/{ushort = 37510} |
| 3     | /xmp/exif:UserComment         |



 

### <a name="tiff-policy"></a>Directiva TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                                    | Formato de disco    |
|-------|-----------------------------------------|----------------|
| 1     | /IFD/{ushort = 40092}                     | \_bytes Unicode |
| 2     | /IFD/{ushort = 37510}                     | unicode        |
| 3     | /IFD/XMP/ <xmpalt> Exif: UserComment | unicode        |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                | Formato de disco    |
|-------|---------------------|----------------|
| 1     | /IFD/{ushort = 40092} | \_bytes Unicode |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                      |
|-------|---------------------------|
| 1     | /IFD/{ushort = 40092}       |
| 2     | /IFD/{ushort = 37510}       |
| 3     | /ifd/xmp/exif:UserComment |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System. Comment](../properties/props-system-comment.md)
</dt> </dl>

 

 
