---
description: La Directiva de metadatos de la fotografía para la propiedad System. title.
ms.assetid: 84da345e-ec03-48fe-8fda-043b706e4e1c
title: Directiva de metadatos de foto de System. title
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b02513f3f566576999e83b09c156d36ac480c17d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706833"
---
# <a name="systemtitle-photo-metadata-policy"></a>Directiva de metadatos de foto de System. title

La Directiva de metadatos de la fotografía para la propiedad [System. title](../properties/props-system-title.md) .

### <a name="pkey"></a>PKEY

Título de PKEY \_

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
| 1     | /app1/IFD/{ushort = 40091}            | \_bytes Unicode |
| 2     | /XMP/ <xmpalt> DC: title         | unicode        |
| 3     | /XMP/DC: título                       | unicode        |
| 4     | /app1/IFD/Exif/{ushort = 37510}       | unicode        |
| 5     | /app1/IFD/{ushort = 270}              | ascii          |
| 6     | /app13/irb/8bimiptc/iptc/caption    |                |
| 7     | /XMP/ <xmpalt> DC: Descripción   | unicode        |
| 8     | /XMP/DC: Descripción                 | unicode        |
| 9     | /app13/irb/8bimiptc/iptc/caption    |                |
| 10    | /XMP/ <xmpalt> Exif: UserComment | unicode        |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                                | Formato de disco    |
|-------|-------------------------------------|----------------|
| 1     | /app1/IFD/{ushort = 40091}            | \_bytes Unicode |
| 2     | /XMP/DC: título                       | unicode        |
| 3     | /XMP/ <xmpalt> DC: title         | unicode        |
| 4     | /app1/IFD/Exif/{ushort = 37510}       | unicode        |
| 5     | /XMP/ <xmpalt> Exif: UserComment | unicode        |
| 6     | /app1/IFD/{ushort = 270}              | ascii          |
| 7     | /app13/irb/8bimiptc/iptc/caption    |                |
| 8     | /XMP/DC: Descripción                 | unicode        |
| 9     | /XMP/ <xmpalt> DC: Descripción   | unicode        |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                                |
|-------|-------------------------------------|
| 1     | /app1/IFD/{ushort = 40091}            |
| 2     | /XMP/DC: título                       |
| 3     | /app1/IFD/Exif/{ushort = 37510}       |
| 4     | /XMP/ <xmpalt> Exif: UserComment |
| 5     | /app1/IFD/{ushort = 270}              |
| 6     | /app13/irb/8bimiptc/iptc/caption    |
| 7     | /XMP/DC: Descripción                 |



 

### <a name="tiff-policy"></a>Directiva TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                                    | Formato de disco    |
|-------|-----------------------------------------|----------------|
| 1     | /IFD/{ushort = 40091}                     | \_bytes Unicode |
| 2     | /IFD/XMP/ <xmpalt> DC: title         | unicode        |
| 3     | /IFD/XMP/DC: título                       | unicode        |
| 4     | /IFD/Exif/{ushort = 37510}                | unicode        |
| 5     | /IFD/{ushort = 270}                       | ascii          |
| 6     | /ifd/iptc/caption                       |                |
| 7     | /IFD/XMP/ <xmpalt> DC: Descripción   | unicode        |
| 8     | /IFD/XMP/DC: Descripción                 | unicode        |
| 9     | /ifd/iptc/caption                       |                |
| 10    | /ifd/irb/8bimiptc/iptc/caption          |                |
| 11    | /IFD/XMP/ <xmpalt> Exif: UserComment | unicode        |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                                    | Formato de disco    |
|-------|-----------------------------------------|----------------|
| 1     | /IFD/{ushort = 40091}                     | \_bytes Unicode |
| 2     | /IFD/XMP/DC: título                       | unicode        |
| 3     | /IFD/XMP/ <xmpalt> DC: title         | unicode        |
| 4     | /IFD/Exif/{ushort = 37510}                | unicode        |
| 5     | /IFD/XMP/ <xmpalt> Exif: UserComment | unicode        |
| 6     | /IFD/{ushort = 270}                       | ascii          |
| 7     | /ifd/iptc/caption                       |                |
| 8     | /ifd/irb/8bimiptc/iptc/caption          |                |
| 9     | /IFD/XMP/DC: Descripción                 | unicode        |
| 10    | /IFD/XMP/ <xmpalt> DC: Descripción   | unicode        |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                                    |
|-------|-----------------------------------------|
| 1     | /IFD/{ushort = 40091}                     |
| 2     | /IFD/XMP/DC: título                       |
| 3     | /IFD/Exif/{ushort = 37510}                |
| 4     | /IFD/XMP/ <xmpalt> Exif: UserComment |
| 5     | /IFD/{ushort = 270}                       |
| 6     | /ifd/iptc/caption                       |
| 7     | /ifd/irb/8bimiptc/iptc/caption          |
| 8     | /IFD/XMP/DC: Descripción                 |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System.Title](../properties/props-system-title.md)
</dt> </dl>

 

 
