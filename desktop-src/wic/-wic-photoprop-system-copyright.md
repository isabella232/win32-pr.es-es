---
description: Directiva de metadatos de fotos para la propiedad System.Copyright.
ms.assetid: 84d2f55b-5ca4-4912-b038-c18a72e6fc34
title: Directiva de metadatos de fotos System.Copyright
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b00b57bc3523feaa29da9008340bd34c32401879a8fc4e872082bbdcddd1fdf8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118710818"
---
# <a name="systemcopyright-photo-metadata-policy"></a>Directiva de metadatos de fotos System.Copyright

Directiva de metadatos de fotos para la [propiedad System.Copyright.](../properties/props-system-copyright.md)

### <a name="pkey"></a>Pkey

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
|       | /xmp/ <xmpalt> dc:rights              | unicode     |
|       | /xmp/dc:rights                            | unicode     |
|       | /app13/irb/8bimiptc/iptc/copyright notice |             |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Ruta de acceso                                      | Formato de disco |
|-------|-------------------------------------------|-------------|
|       | /xmp/dc:rights                            | unicode     |
|       | /xmp/ <xmpalt> dc:rights              | unicode     |
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
|       | /ifd/xmp/ <xmpalt> dc:rights        | unicode     |
|       | /ifd/xmp/dc:rights                      | unicode     |
|       | /ifd/iptc/aviso de copyright              |             |
|       | /ifd/irb/8bimiptc/iptc/copyright notice |             |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Ruta de acceso                                    | Formato de disco |
|-------|-----------------------------------------|-------------|
|       | /ifd/xmp/dc:rights                      | unicode     |
|       | /ifd/xmp/ <xmpalt> dc:rights        | unicode     |
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



 

## <a name="remarks"></a>Comentarios

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System.Copyright](../properties/props-system-copyright.md)
</dt> </dl>

 

 
