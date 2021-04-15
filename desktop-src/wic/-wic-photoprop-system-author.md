---
description: La Directiva de metadatos de la fotografía para la propiedad System. Author.
ms.assetid: 2de9c452-93be-40a4-a72b-5da590534dfd
title: Directiva de metadatos de fotografía de System. Author
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb90345257ef1623f7cda1ce4318af7a9f472df5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720716"
---
# <a name="systemauthor-photo-metadata-policy"></a>Directiva de metadatos de fotografía de System. Author

La Directiva de metadatos de la fotografía para la propiedad [System. Author](../properties/props-system-author.md) .

### <a name="pkey"></a>PKEY

Autor de PKEY \_

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

No

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de salida

VT \_ Vector \| VT \_ LPWStr

### <a name="input-propvariant-type"></a>Tipo de PROPVARIANT de entrada

\_ \| Se prefiere VT vector VT \_ LPWStr, pero \_ también se acepta VT LPWStr.

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Se reconcilian los valores de los distintos esquemas.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                             | Formato de disco    |
|-------|----------------------------------|----------------|
| 1     | /app1/IFD/{ushort = 315}           | ascii          |
| 2     | /app13/irb/8bimiptc/iptc/by-line |                |
| 3     | /XMP/ <xmpseq> DC: creador    | unicode        |
| 4     | /app13/irb/8bimiptc/iptc/by-line |                |
| 5     | /app1/IFD/{ushort = 40093}         | \_bytes Unicode |
| 6     | /XMP/TIFF: artista                 | unicode        |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                             | Formato de disco    |
|-------|----------------------------------|----------------|
| 1     | /XMP/ <xmpseq> DC: creador    | unicode        |
| 2     | /XMP/TIFF: artista                 | unicode        |
| 3     | /app13/irb/8bimiptc/iptc/by-line |                |
| 4     | /app1/IFD/{ushort = 315}           | ascii          |
| 5     | /app1/IFD/{ushort = 40093}         | \_bytes Unicode |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                             |
|-------|----------------------------------|
| 1     | /XMP/DC: creador                  |
| 2     | /XMP/TIFF: artista                 |
| 3     | /app13/irb/8bimiptc/iptc/by-line |
| 4     | /app1/IFD/{ushort = 315}           |
| 5     | /app1/IFD/{ushort = 40093}         |



 

### <a name="tiff-policy"></a>Directiva TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                              | Formato de disco    |
|-------|-----------------------------------|----------------|
| 1     | /IFD/{ushort = 315}                 | ascii          |
| 2     | /ifd/iptc/by-line                 |                |
| 3     | /IFD/XMP/ <xmpseq> DC: creador | unicode        |
| 4     | /ifd/iptc/by-line                 |                |
| 5     | /IFD/{ushort = 40093}               | \_bytes Unicode |
| 6     | /ifd/irb/8bimiptc/iptc/by-line    |                |
| 7     | /IFD/XMP/TIFF: artista              | unicode        |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                              | Formato de disco    |
|-------|-----------------------------------|----------------|
| 1     | /IFD/XMP/ <xmpseq> DC: creador | unicode        |
| 2     | /IFD/XMP/TIFF: artista              | unicode        |
| 3     | /ifd/iptc/by-line                 |                |
| 4     | /IFD/{ushort = 315}                 | \_Vector ASCII  |
| 5     | /IFD/{ushort = 40093}               | \_bytes Unicode |
| 6     | /ifd/iptc/by-line                 |                |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                           |
|-------|--------------------------------|
| 1     | /IFD/XMP/DC: creador            |
| 2     | /IFD/XMP/TIFF: artista           |
| 3     | /ifd/iptc/by-line              |
| 4     | /ifd/irb/8bimiptc/iptc/by-line |
| 5     | /IFD/{ushort = 315}              |
| 6     | /IFD/{ushort = 40093}            |



 

### <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System.Author](../properties/props-system-author.md)
</dt> </dl>

 

 
