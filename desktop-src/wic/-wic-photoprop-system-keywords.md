---
description: La Directiva de metadatos de la fotografía para la propiedad System. keywords.
ms.assetid: bc9de56f-444c-45a2-9822-fba2fe618d38
title: Directiva de metadatos de la foto System. keywords
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc5d25e7f1919527d474395397d6df62863f7b78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278636"
---
# <a name="systemkeywords-photo-metadata-policy"></a>Directiva de metadatos de la foto System. keywords

La Directiva de metadatos de la fotografía para la propiedad [System. keywords](../properties/props-system-keywords.md) .

### <a name="pkey"></a>PKEY

\_Palabras clave de PKEY

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

No

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de salida

VT \_ Vector \| VT \_ LPWStr

### <a name="input-propvariant-type"></a>Tipo de PROPVARIANT de entrada

\_ \| Se prefiere VT vector VT \_ LPWStr. \_También se acepta un VT LPWStr que contenga una cadena delimitada por punto y coma.

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Se combinan los valores de los distintos esquemas.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                              | Formato de disco    |
|-------|-----------------------------------|----------------|
| 1     | /XMP/ <xmpbag> DC: asunto     | unicode        |
| 2     | /app13/irb/8bimiptc/iptc/keywords |                |
| 3     | /app1/IFD/{ushort = 18247}          | \_bytes Unicode |
| 4     | /app1/IFD/{ushort = 40094}          | \_bytes Unicode |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                                              | Formato de disco    |
|-------|---------------------------------------------------|----------------|
| 1     | /XMP/ <xmpbag> DC: asunto                     | unicode        |
| 2     | /app13/irb/8bimiptc/iptc/keywords                 |                |
| 3     | /app1/IFD/{ushort = 18247}                          | \_bytes Unicode |
| 4     | /app1/IFD/{ushort = 40094}                          | \_bytes Unicode |
| 5     | /XMP/ <xmpbag> MicrosoftPhoto: LastKeywordXMP  | unicode        |
| 6     | /XMP/ <xmpbag> MicrosoftPhoto: LastKeywordIPTC | unicode        |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                                              |
|-------|---------------------------------------------------|
| 1     | /XMP/DC: asunto                                   |
| 2     | /app13/irb/8bimiptc/iptc/keywords                 |
| 3     | /app1/IFD/{ushort = 18247}                          |
| 4     | /app1/IFD/{ushort = 40094}                          |
| 5     | /XMP/ <xmpbag> MicrosoftPhoto: LastKeywordXMP  |
| 6     | /XMP/ <xmpbag> MicrosoftPhoto: LastKeywordIPTC |



 

### <a name="tiff-policy"></a>Directiva TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                              | Formato de disco    |
|-------|-----------------------------------|----------------|
| 1     | /IFD/XMP/ <xmpbag> DC: asunto | unicode        |
| 2     | /ifd/iptc/keywords                |                |
| 3     | /IFD/{ushort = 18247}               | \_bytes Unicode |
| 4     | /IFD/{ushort = 40094}               | \_bytes Unicode |
| 5     | /ifd/irb/8bimiptc/iptc/keywords   |                |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                                                             | Formato de disco    |
|-------|------------------------------------------------------------------|----------------|
| 1     | /IFD/XMP/ <xmpbag> DC: asunto                                | unicode        |
| 2     | /ifd/iptc/keywords                                               |                |
| 3     | /ifd/irb/8bimiptc/iptc/keywords                                  |                |
| 4     | /IFD/{ushort = 18247}                                              | \_bytes Unicode |
| 5     | /IFD/{ushort = 40094}                                              | \_bytes Unicode |
| 6     | /IFD/XMP/ <xmpbag> MicrosoftPhoto: LastKeywordXMP             | unicode        |
| 7     | /IFD/XMP/ <xmpbag> MicrosoftPhoto: LastKeywordIPTC            | unicode        |
| 8     | /IFD/XMP/ <xmpbag> MicrosoftPhoto: LastKeywordIPTC \_ TIFF \_ IRB | unicode        |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                                                             |
|-------|------------------------------------------------------------------|
| 1     | /IFD/XMP/DC: asunto                                              |
| 2     | /ifd/iptc/keywords                                               |
| 3     | /ifd/irb/8bimiptc/iptc/keywords                                  |
| 4     | /IFD/{ushort = 18247}                                              |
| 5     | /IFD/{ushort = 40094}                                              |
| 6     | /IFD/XMP/ <xmpbag> MicrosoftPhoto: LastKeywordXMP             |
| 7     | /IFD/XMP/ <xmpbag> MicrosoftPhoto: LastKeywordIPTC            |
| 8     | /IFD/XMP/ <xmpbag> MicrosoftPhoto: LastKeywordIPTC \_ TIFF \_ IRB |



 

### <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System.Keywords](../properties/props-system-keywords.md)
</dt> </dl>

 

 
