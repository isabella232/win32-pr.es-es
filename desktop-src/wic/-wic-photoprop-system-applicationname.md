---
description: La Directiva de metadatos de la fotografía para la propiedad System. ApplicationName.
ms.assetid: bf4b310a-7e63-45c5-a327-2638fb31d676
title: Directiva de metadatos de la foto de System. ApplicationName
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e36fac2a864cabfd7c1521d72357d187a8aea50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103817699"
---
# <a name="systemapplicationname-photo-metadata-policy"></a>Directiva de metadatos de la foto de System. ApplicationName

La Directiva de metadatos de la fotografía para la propiedad [System. ApplicationName](../properties/props-system-applicationname.md) .

### <a name="pkey"></a>PKEY

PKEY \_ ApplicationName

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

No

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de salida

VT \_ LPWStr

### <a name="input-type"></a>Tipo de entrada

String

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Se reconcilian los valores de los distintos esquemas.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                                         | Formato de disco |
|-------|----------------------------------------------|-------------|
|       | /app1/IFD/{ushort = 305}                       | ascii       |
|       | Programa/app13/irb/8bimiptc/iptc/Originating |             |
|       | /xmp/xmp:CreatorTool                         | unicode     |
|       | /xmp/xmp:creatortool                         | unicode     |
|       | /XMP/TIFF: software                           | unicode     |
|       | /XMP/TIFF: software                           | unicode     |
|       | Programa/app13/irb/8bimiptc/iptc/Originating |             |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                                         | Formato de disco |
|-------|----------------------------------------------|-------------|
|       | /app1/IFD/{ushort = 305}                       | ascii       |
|       | /xmp/xmp:CreatorTool                         | unicode     |
|       | /xmp/xmp:creatortool                         | unicode     |
|       | /XMP/TIFF: software                           | unicode     |
|       | /XMP/TIFF: software                           | unicode     |
|       | Programa/app13/irb/8bimiptc/iptc/Originating |             |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                                         |
|-------|----------------------------------------------|
|       | /app1/IFD/{ushort = 305}                       |
|       | /xmp/xmp:CreatorTool                         |
|       | /xmp/xmp:creatortool                         |
|       | /XMP/TIFF: software                           |
|       | /XMP/TIFF: software                           |
|       | Programa/app13/irb/8bimiptc/iptc/Originating |



 

### <a name="tiff-policy"></a>Directiva TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                                       | Formato de disco |
|-------|--------------------------------------------|-------------|
|       | /IFD/{ushort = 305}                          | ascii       |
|       | Programa/ifd/iptc/Originating              |             |
|       | /ifd/xmp/xmp:CreatorTool                   | unicode     |
|       | /ifd/xmp/xmp:creatortool                   | unicode     |
|       | /IFD/XMP/TIFF: software                     | unicode     |
|       | /IFD/XMP/TIFF: software                     | unicode     |
|       | Programa/ifd/iptc/Originating              |             |
|       | Programa/ifd/irb/8bimiptc/iptc/Originating |             |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                                       | Formato de disco |
|-------|--------------------------------------------|-------------|
|       | /IFD/{ushort = 305}                          | ascii       |
|       | /ifd/xmp/xmp:CreatorTool                   | unicode     |
|       | /ifd/xmp/xmp:creatortool                   | unicode     |
|       | /IFD/XMP/TIFF: software                     | unicode     |
|       | /IFD/XMP/TIFF: software                     | unicode     |
|       | Programa/ifd/iptc/Originating              |             |
|       | Programa/ifd/irb/8bimiptc/iptc/Originating |             |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                                       |
|-------|--------------------------------------------|
|       | /IFD/{ushort = 305}                          |
|       | /ifd/xmp/xmp:CreatorTool                   |
|       | /ifd/xmp/xmp:creatortool                   |
|       | /IFD/XMP/TIFF: software                     |
|       | /IFD/XMP/TIFF: software                     |
|       | Programa/ifd/iptc/Originating              |
|       | Programa/ifd/irb/8bimiptc/iptc/Originating |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System. ApplicationName](../properties/props-system-applicationname.md)
</dt> </dl>

 

 
