---
description: Directiva de metadatos de fotos para la propiedad System.Title.
ms.assetid: 84da345e-ec03-48fe-8fda-043b706e4e1c
title: Directiva de metadatos de fotos System.Title
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa43b31595928fa3c2c936de8710131c20f17b1a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359984"
---
# <a name="systemtitle-photo-metadata-policy"></a>Directiva de metadatos de fotos System.Title

Directiva de metadatos de fotos para [la propiedad System.Title.](../properties/props-system-title.md)

### <a name="pkey"></a>PKEY

PKEY \_ Title

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



| Pedido | Path                                | Formato de disco    |
|-------|-------------------------------------|----------------|
| 1     | /app1/ifd/{ushort=40091}            | bytes \_ unicode |
| 2     | /xmp/ &lt; xmpalt &gt; dc:title         | unicode        |
| 3     | /xmp/dc:title                       | unicode        |
| 4     | /app1/ifd/exif/{ushort=37510}       | unicode        |
| 5     | /app1/ifd/{ushort=270}              | ascii          |
| 6     | /app13/irb/8bimiptc/iptc/caption    |                |
| 7     | /xmp/ &lt; xmpalt &gt; dc:description   | unicode        |
| 8     | /xmp/dc:description                 | unicode        |
| 9     | /app13/irb/8bimiptc/iptc/caption    |                |
| 10    | /xmp/ &lt; xmpalt &gt; exif:UserComment | unicode        |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Path                                | Formato de disco    |
|-------|-------------------------------------|----------------|
| 1     | /app1/ifd/{ushort=40091}            | bytes \_ unicode |
| 2     | /xmp/dc:title                       | unicode        |
| 3     | /xmp/ &lt; xmpalt &gt; dc:title         | unicode        |
| 4     | /app1/ifd/exif/{ushort=37510}       | unicode        |
| 5     | /xmp/ &lt; xmpalt &gt; exif:UserComment | unicode        |
| 6     | /app1/ifd/{ushort=270}              | ascii          |
| 7     | /app13/irb/8bimiptc/iptc/caption    |                |
| 8     | /xmp/dc:description                 | unicode        |
| 9     | /xmp/ &lt; xmpalt &gt; dc:description   | unicode        |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Path                                |
|-------|-------------------------------------|
| 1     | /app1/ifd/{ushort=40091}            |
| 2     | /xmp/dc:title                       |
| 3     | /app1/ifd/exif/{ushort=37510}       |
| 4     | /xmp/ &lt; xmpalt &gt; exif:UserComment |
| 5     | /app1/ifd/{ushort=270}              |
| 6     | /app13/irb/8bimiptc/iptc/caption    |
| 7     | /xmp/dc:description                 |



 

### <a name="tiff-policy"></a>Directiva TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Path                                    | Formato de disco    |
|-------|-----------------------------------------|----------------|
| 1     | /ifd/{ushort=40091}                     | bytes \_ unicode |
| 2     | /ifd/xmp/ &lt; xmpalt &gt; dc:title         | unicode        |
| 3     | /ifd/xmp/dc:title                       | unicode        |
| 4     | /ifd/exif/{ushort=37510}                | unicode        |
| 5     | /ifd/{ushort=270}                       | ascii          |
| 6     | /ifd/iptc/caption                       |                |
| 7     | /ifd/xmp/ &lt; xmpalt &gt; dc:description   | unicode        |
| 8     | /ifd/xmp/dc:description                 | unicode        |
| 9     | /ifd/iptc/caption                       |                |
| 10    | /ifd/irb/8bimiptc/iptc/caption          |                |
| 11    | /ifd/xmp/ &lt; xmpalt &gt; exif:UserComment | unicode        |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Path                                    | Formato de disco    |
|-------|-----------------------------------------|----------------|
| 1     | /ifd/{ushort=40091}                     | bytes \_ unicode |
| 2     | /ifd/xmp/dc:title                       | unicode        |
| 3     | /ifd/xmp/ &lt; xmpalt &gt; dc:title         | unicode        |
| 4     | /ifd/exif/{ushort=37510}                | unicode        |
| 5     | /ifd/xmp/ &lt; xmpalt &gt; exif:UserComment | unicode        |
| 6     | /ifd/{ushort=270}                       | ascii          |
| 7     | /ifd/iptc/caption                       |                |
| 8     | /ifd/irb/8bimiptc/iptc/caption          |                |
| 9     | /ifd/xmp/dc:description                 | unicode        |
| 10    | /ifd/xmp/ &lt; xmpalt &gt; dc:description   | unicode        |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Path                                    |
|-------|-----------------------------------------|
| 1     | /ifd/{ushort=40091}                     |
| 2     | /ifd/xmp/dc:title                       |
| 3     | /ifd/exif/{ushort=37510}                |
| 4     | /ifd/xmp/ &lt; xmpalt &gt; exif:UserComment |
| 5     | /ifd/{ushort=270}                       |
| 6     | /ifd/iptc/caption                       |
| 7     | /ifd/irb/8bimiptc/iptc/caption          |
| 8     | /ifd/xmp/dc:description                 |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System.Title](../properties/props-system-title.md)
</dt> </dl>

 

 
