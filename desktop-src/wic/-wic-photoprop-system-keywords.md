---
description: Directiva de metadatos de fotos para la propiedad System.Keywords.
ms.assetid: bc9de56f-444c-45a2-9822-fba2fe618d38
title: Directiva de metadatos de fotos System.Keywords
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2aa5387bfb8cca7fffe83f7615a979d8e23ae890
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886650"
---
# <a name="systemkeywords-photo-metadata-policy"></a>Directiva de metadatos de fotos System.Keywords

Directiva de metadatos de fotos para la [propiedad System.Keywords.](../properties/props-system-keywords.md)

### <a name="pkey"></a>PKEY

Palabras \_ clave PKEY

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

No

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de salida

VT \_ VECTOR \| VT \_ LPWSTR

### <a name="input-propvariant-type"></a>Tipo PROPVARIANT de entrada

Se \_ prefiere VT VECTOR VT \| \_ LPWSTR. También se acepta una VT LPWSTR que contiene una cadena delimitada por punto \_ y coma.

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Los valores de esquemas diferentes se combinan.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido de | Ruta de acceso                              | Formato de disco    |
|-------|-----------------------------------|----------------|
| 1     | /xmp/ &lt; xmpbag &gt; dc:subject     | unicode        |
| 2     | /app13/irb/8bimiptc/iptc/keywords |                |
| 3     | /app1/ifd/{ushort=18247}          | bytes \_ unicode |
| 4     | /app1/ifd/{ushort=40094}          | bytes \_ unicode |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido de | Ruta de acceso                                              | Formato de disco    |
|-------|---------------------------------------------------|----------------|
| 1     | /xmp/ &lt; xmpbag &gt; dc:subject                     | unicode        |
| 2     | /app13/irb/8bimiptc/iptc/keywords                 |                |
| 3     | /app1/ifd/{ushort=18247}                          | bytes \_ unicode |
| 4     | /app1/ifd/{ushort=40094}                          | bytes \_ unicode |
| 5     | /xmp/ &lt; xmpbag &gt; MicrosoftPhoto:LastKeywordXMP  | unicode        |
| 6     | /xmp/ &lt; xmpbag &gt; MicrosoftPhoto:LastKeywordIPTC | unicode        |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido de | Ruta de acceso                                              |
|-------|---------------------------------------------------|
| 1     | /xmp/dc:subject                                   |
| 2     | /app13/irb/8bimiptc/iptc/keywords                 |
| 3     | /app1/ifd/{ushort=18247}                          |
| 4     | /app1/ifd/{ushort=40094}                          |
| 5     | /xmp/ &lt; xmpbag &gt; MicrosoftPhoto:LastKeywordXMP  |
| 6     | /xmp/ &lt; xmpbag &gt; MicrosoftPhoto:LastKeywordIPTC |



 

### <a name="tiff-policy"></a>Directiva TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido de | Ruta de acceso                              | Formato de disco    |
|-------|-----------------------------------|----------------|
| 1     | /ifd/xmp/ &lt; xmpbag &gt; dc:subject | unicode        |
| 2     | /ifd/iptc/keywords                |                |
| 3     | /ifd/{ushort=18247}               | bytes \_ unicode |
| 4     | /ifd/{ushort=40094}               | bytes \_ unicode |
| 5     | /ifd/irb/8bimiptc/iptc/keywords   |                |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido de | Ruta de acceso                                                             | Formato de disco    |
|-------|------------------------------------------------------------------|----------------|
| 1     | /ifd/xmp/ &lt; xmpbag &gt; dc:subject                                | unicode        |
| 2     | /ifd/iptc/keywords                                               |                |
| 3     | /ifd/irb/8bimiptc/iptc/keywords                                  |                |
| 4     | /ifd/{ushort=18247}                                              | bytes \_ unicode |
| 5     | /ifd/{ushort=40094}                                              | bytes \_ unicode |
| 6     | /ifd/xmp/ &lt; xmpbag &gt; MicrosoftPhoto:LastKeywordXMP             | unicode        |
| 7     | /ifd/xmp/ &lt; xmpbag &gt; MicrosoftPhoto:LastKeywordIPTC            | unicode        |
| 8     | /ifd/xmp/ &lt; xmpbag &gt; MicrosoftPhoto:LastKeywordIPTC \_ TIFF \_ IRB | unicode        |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido de | Ruta de acceso                                                             |
|-------|------------------------------------------------------------------|
| 1     | /ifd/xmp/dc:subject                                              |
| 2     | /ifd/iptc/keywords                                               |
| 3     | /ifd/irb/8bimiptc/iptc/keywords                                  |
| 4     | /ifd/{ushort=18247}                                              |
| 5     | /ifd/{ushort=40094}                                              |
| 6     | /ifd/xmp/ &lt; xmpbag &gt; MicrosoftPhoto:LastKeywordXMP             |
| 7     | /ifd/xmp/ &lt; xmpbag &gt; MicrosoftPhoto:LastKeywordIPTC            |
| 8     | /ifd/xmp/ &lt; xmpbag &gt; MicrosoftPhoto:LastKeywordIPTC \_ TIFF \_ IRB |



 

### <a name="remarks"></a>Comentarios

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System.Keywords](../properties/props-system-keywords.md)
</dt> </dl>

 

 
