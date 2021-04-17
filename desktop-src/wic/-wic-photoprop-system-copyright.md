---
description: La Directiva de metadatos de la fotografía para la propiedad System. Copyright.
ms.assetid: 84d2f55b-5ca4-4912-b038-c18a72e6fc34
title: Directiva de metadatos de fotos de System. Copyright
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fc65024458d88088e3c0cbeccc3bc9ea0211910
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716897"
---
# <a name="systemcopyright-photo-metadata-policy"></a>Directiva de metadatos de fotos de System. Copyright

La Directiva de metadatos de la fotografía para la propiedad [System. Copyright](../properties/props-system-copyright.md) .

### <a name="pkey"></a>PKEY

Copyright de PKEY \_

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

No

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de salida

VT \_ LPWStr

### <a name="input-propvariant-type"></a>Tipo de PROPVARIANT de entrada

String

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Se reconcilian los valores de los distintos esquemas.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                                      | Formato de disco |
|-------|-------------------------------------------|-------------|
|       | /app1/IFD/{ushort = 33432}                  | ascii       |
|       | Aviso de/app13/IRB/8bimiptc/IPTC/Copyright |             |
|       | /XMP/ <xmpalt> DC: derechos              | unicode     |
|       | /XMP/DC: derechos                            | unicode     |
|       | Aviso de/app13/IRB/8bimiptc/IPTC/Copyright |             |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                                      | Formato de disco |
|-------|-------------------------------------------|-------------|
|       | /XMP/DC: derechos                            | unicode     |
|       | /XMP/ <xmpalt> DC: derechos              | unicode     |
|       | Aviso de/app13/IRB/8bimiptc/IPTC/Copyright |             |
|       | /app1/IFD/{ushort = 33432}                  | ascii       |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                                      |
|-------|-------------------------------------------|
|       | /XMP/DC: derechos                            |
|       | Aviso de/app13/IRB/8bimiptc/IPTC/Copyright |
|       | /app1/IFD/{ushort = 33432}                  |



 

### <a name="tiff-policy"></a>Directiva TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                                    | Formato de disco |
|-------|-----------------------------------------|-------------|
|       | /IFD/{ushort = 33432}                     | ascii       |
|       | Aviso de/IFD/IPTC/Copyright              |             |
|       | /IFD/XMP/ <xmpalt> DC: derechos        | unicode     |
|       | /IFD/XMP/DC: derechos                      | unicode     |
|       | Aviso de/IFD/IPTC/Copyright              |             |
|       | Aviso de/IFD/IRB/8bimiptc/IPTC/Copyright |             |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                                    | Formato de disco |
|-------|-----------------------------------------|-------------|
|       | /IFD/XMP/DC: derechos                      | unicode     |
|       | /IFD/XMP/ <xmpalt> DC: derechos        | unicode     |
|       | Aviso de/IFD/IPTC/Copyright              |             |
|       | Aviso de/IFD/IRB/8bimiptc/IPTC/Copyright |             |
|       | /IFD/{ushort = 33432}                     | ascii       |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                                    |
|-------|-----------------------------------------|
|       | /IFD/XMP/DC: derechos                      |
|       | Aviso de/IFD/IPTC/Copyright              |
|       | Aviso de/IFD/IRB/8bimiptc/IPTC/Copyright |
|       | /IFD/{ushort = 33432}                     |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System. Copyright](../properties/props-system-copyright.md)
</dt> </dl>

 

 
