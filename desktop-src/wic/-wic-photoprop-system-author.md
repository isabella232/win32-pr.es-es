---
description: Directiva de metadatos de fotos para la propiedad System.Author.
ms.assetid: 2de9c452-93be-40a4-a72b-5da590534dfd
title: Directiva de metadatos de fotos de System.Author
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b898f450fe1d370f94a9be2922eb650db47ac8c2e414c27d9eede23f0dada276
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119088007"
---
# <a name="systemauthor-photo-metadata-policy"></a>Directiva de metadatos de fotos de System.Author

Directiva de metadatos de fotos para [la propiedad System.Author.](../properties/props-system-author.md)

### <a name="pkey"></a>Pkey

PKEY \_ Author

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

No

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de salida

VT \_ VECTOR \| VT \_ LPWSTR

### <a name="input-propvariant-type"></a>Tipo PROPVARIANT de entrada

Se \_ prefiere VT VECTOR VT \| \_ LPWSTR, pero \_ también se acepta VT LPWSTR.

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Los valores de esquemas diferentes se concilian.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Rutas de acceso de lectura



| Pedido | Ruta de acceso                             | Formato de disco    |
|-------|----------------------------------|----------------|
| 1     | /app1/ifd/{ushort=315}           | ascii          |
| 2     | /app13/irb/8bimiptc/iptc/by-line |                |
| 3     | /xmp/ <xmpseq> dc:creator    | unicode        |
| 4     | /app13/irb/8bimiptc/iptc/by-line |                |
| 5     | /app1/ifd/{ushort=40093}         | bytes \_ unicode |
| 6     | /xmp/tiff:artist                 | unicode        |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Ruta de acceso                             | Formato de disco    |
|-------|----------------------------------|----------------|
| 1     | /xmp/ <xmpseq> dc:creator    | unicode        |
| 2     | /xmp/tiff:artist                 | unicode        |
| 3     | /app13/irb/8bimiptc/iptc/by-line |                |
| 4     | /app1/ifd/{ushort=315}           | ascii          |
| 5     | /app1/ifd/{ushort=40093}         | bytes \_ unicode |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                             |
|-------|----------------------------------|
| 1     | /xmp/dc:creator                  |
| 2     | /xmp/tiff:artist                 |
| 3     | /app13/irb/8bimiptc/iptc/by-line |
| 4     | /app1/ifd/{ushort=315}           |
| 5     | /app1/ifd/{ushort=40093}         |



 

### <a name="tiff-policy"></a>Directiva TIFF

### <a name="read-paths"></a>Rutas de acceso de lectura



| Pedido | Ruta de acceso                              | Formato de disco    |
|-------|-----------------------------------|----------------|
| 1     | /ifd/{ushort=315}                 | ascii          |
| 2     | /ifd/iptc/by-line                 |                |
| 3     | /ifd/xmp/ <xmpseq> dc:creator | unicode        |
| 4     | /ifd/iptc/by-line                 |                |
| 5     | /ifd/{ushort=40093}               | bytes \_ unicode |
| 6     | /ifd/irb/8bimiptc/iptc/by-line    |                |
| 7     | /ifd/xmp/tiff:artist              | unicode        |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Ruta de acceso                              | Formato de disco    |
|-------|-----------------------------------|----------------|
| 1     | /ifd/xmp/ <xmpseq> dc:creator | unicode        |
| 2     | /ifd/xmp/tiff:artist              | unicode        |
| 3     | /ifd/iptc/by-line                 |                |
| 4     | /ifd/{ushort=315}                 | vector \_ ascii  |
| 5     | /ifd/{ushort=40093}               | bytes \_ unicode |
| 6     | /ifd/iptc/by-line                 |                |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                           |
|-------|--------------------------------|
| 1     | /ifd/xmp/dc:creator            |
| 2     | /ifd/xmp/tiff:artist           |
| 3     | /ifd/iptc/by-line              |
| 4     | /ifd/irb/8bimiptc/iptc/by-line |
| 5     | /ifd/{ushort=315}              |
| 6     | /ifd/{ushort=40093}            |



 

### <a name="remarks"></a>Comentarios

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System.Author](../properties/props-system-author.md)
</dt> </dl>

 

 
