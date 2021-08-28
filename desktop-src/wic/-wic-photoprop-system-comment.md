---
description: Directiva de metadatos de fotos para la propiedad System.Comment.
ms.assetid: 02a6ac18-ad69-4880-a267-8330d648c0d9
title: Directiva de metadatos de fotos System.Comment
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2aa1a62fd5afa131a714c365ed2fda2c307bc955
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883903"
---
# <a name="systemcomment-photo-metadata-policy"></a>Directiva de metadatos de fotos System.Comment

Directiva de metadatos de fotos para la [propiedad System.Comment.](../properties/props-system-comment.md)

### <a name="pkey"></a>PKEY

Comentario \_ PKEY

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

No

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de salida

VT \_ LPWSTR

### <a name="input-propvariant-type"></a>Tipo PROPVARIANT de entrada

VT \_ LPWSTR o VT \_ LPSTR

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Los valores de esquemas diferentes se concilian.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido de | Ruta de acceso                                | Formato de disco    |
|-------|-------------------------------------|----------------|
| 1     | /app1/ifd/{ushort=40092}            | bytes \_ unicode |
| 2     | /app1/ifd/{ushort=37510}            | unicode        |
| 3     | /xmp/ &lt; xmpalt &gt; exif:UserComment | unicode        |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido de | Ruta de acceso                     | Formato de disco    |
|-------|--------------------------|----------------|
| 1     | /app1/ifd/{ushort=40092} | bytes \_ unicode |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido de | Ruta de acceso                          |
|-------|-------------------------------|
| 1     | /app1/ifd/{ushort=40092}      |
| 2     | /app1/ifd/exif/{ushort=37510} |
| 3     | /xmp/exif:UserComment         |



 

### <a name="tiff-policy"></a>Directiva TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido de | Ruta de acceso                                    | Formato de disco    |
|-------|-----------------------------------------|----------------|
| 1     | /ifd/{ushort=40092}                     | bytes \_ unicode |
| 2     | /ifd/{ushort=37510}                     | unicode        |
| 3     | /ifd/xmp/ &lt; xmpalt &gt; exif:UserComment | unicode        |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido de | Ruta de acceso                | Formato de disco    |
|-------|---------------------|----------------|
| 1     | /ifd/{ushort=40092} | bytes \_ unicode |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido de | Ruta de acceso                      |
|-------|---------------------------|
| 1     | /ifd/{ushort=40092}       |
| 2     | /ifd/{ushort=37510}       |
| 3     | /ifd/xmp/exif:UserComment |



 

## <a name="remarks"></a>Comentarios

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System.Comment](../properties/props-system-comment.md)
</dt> </dl>

 

 
