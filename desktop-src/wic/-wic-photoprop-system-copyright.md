---
description: Directiva de metadatos de fotos para la propiedad System.Copyright.
ms.assetid: 84d2f55b-5ca4-4912-b038-c18a72e6fc34
title: Directiva de metadatos de fotos System.Copyright
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3e17190205b3df5c2ede9b1a7db231d0fdbbe21
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127572277"
---
# <a name="systemcopyright-photo-metadata-policy"></a>Directiva de metadatos de fotos System.Copyright

Directiva de metadatos de fotos para la [propiedad System.Copyright.](../properties/props-system-copyright.md)

### <a name="pkey"></a>PKEY

PKEY \_ Copyright

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

No

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de salida

VT \_ LPWSTR

### <a name="input-propvariant-type"></a>Tipo PROPVARIANT de entrada

String

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Los valores de esquemas diferentes se concilian.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta de acceso                                      | Formato de disco |
|-------|-------------------------------------------|-------------|
|       | /app1/ifd/{ushort=33432}                  | ascii       |
|       | /app13/irb/8bimiptc/iptc/copyright notice |             |
|       | /xmp/ &lt; xmpalt &gt; dc:rights              | unicode     |
|       | /xmp/dc:rights                            | unicode     |
|       | /app13/irb/8bimiptc/iptc/copyright notice |             |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Ruta de acceso                                      | Formato de disco |
|-------|-------------------------------------------|-------------|
|       | /xmp/dc:rights                            | unicode     |
|       | /xmp/ &lt; xmpalt &gt; dc:rights              | unicode     |
|       | /app13/irb/8bimiptc/iptc/copyright notice |             |
|       | /app1/ifd/{ushort=33432}                  | ascii       |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                                      |
|-------|-------------------------------------------|
|       | /xmp/dc:rights                            |
|       | /app13/irb/8bimiptc/iptc/copyright notice |
|       | /app1/ifd/{ushort=33432}                  |



 

### <a name="tiff-policy"></a>Directiva TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta de acceso                                    | Formato de disco |
|-------|-----------------------------------------|-------------|
|       | /ifd/{ushort=33432}                     | ascii       |
|       | /ifd/iptc/aviso de copyright              |             |
|       | /ifd/xmp/ &lt; xmpalt &gt; dc:rights        | unicode     |
|       | /ifd/xmp/dc:rights                      | unicode     |
|       | /ifd/iptc/aviso de copyright              |             |
|       | /ifd/irb/8bimiptc/iptc/copyright notice |             |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Ruta de acceso                                    | Formato de disco |
|-------|-----------------------------------------|-------------|
|       | /ifd/xmp/dc:rights                      | unicode     |
|       | /ifd/xmp/ &lt; xmpalt &gt; dc:rights        | unicode     |
|       | /ifd/iptc/aviso de copyright              |             |
|       | /ifd/irb/8bimiptc/iptc/copyright notice |             |
|       | /ifd/{ushort=33432}                     | ascii       |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                                    |
|-------|-----------------------------------------|
|       | /ifd/xmp/dc:rights                      |
|       | /ifd/iptc/aviso de copyright              |
|       | /ifd/irb/8bimiptc/iptc/copyright notice |
|       | /ifd/{ushort=33432}                     |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System.Copyright](../properties/props-system-copyright.md)
</dt> </dl>

 

 
