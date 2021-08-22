---
description: Directiva de metadatos de fotos para la propiedad System.ApplicationName.
ms.assetid: bf4b310a-7e63-45c5-a327-2638fb31d676
title: Directiva de metadatos de fotos System.ApplicationName
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3084f21453a82c79925d4a164f5f847c3a24968009b7b8c4236ce3a40872dad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118710924"
---
# <a name="systemapplicationname-photo-metadata-policy"></a>Directiva de metadatos de fotos System.ApplicationName

Directiva de metadatos de fotos para [la propiedad System.ApplicationName.](../properties/props-system-applicationname.md)

### <a name="pkey"></a>Pkey

PKEY \_ ApplicationName

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

No

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de salida

VT \_ LPWSTR

### <a name="input-type"></a>Tipo de entrada

String

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Los valores de esquemas diferentes se concilian.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Rutas de acceso de lectura



| Pedido | Ruta de acceso                                         | Formato de disco |
|-------|----------------------------------------------|-------------|
|       | /app1/ifd/{ushort=305}                       | ascii       |
|       | /app13/irb/8bimiptc/iptc/Originating Program |             |
|       | /xmp/xmp:CreatorTool                         | unicode     |
|       | /xmp/xmp:creatortool                         | unicode     |
|       | /xmp/tiff:Software                           | unicode     |
|       | /xmp/tiff:software                           | unicode     |
|       | /app13/irb/8bimiptc/iptc/Originating Program |             |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Ruta de acceso                                         | Formato de disco |
|-------|----------------------------------------------|-------------|
|       | /app1/ifd/{ushort=305}                       | ascii       |
|       | /xmp/xmp:CreatorTool                         | unicode     |
|       | /xmp/xmp:creatortool                         | unicode     |
|       | /xmp/tiff:Software                           | unicode     |
|       | /xmp/tiff:software                           | unicode     |
|       | /app13/irb/8bimiptc/iptc/Originating Program |             |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                                         |
|-------|----------------------------------------------|
|       | /app1/ifd/{ushort=305}                       |
|       | /xmp/xmp:CreatorTool                         |
|       | /xmp/xmp:creatortool                         |
|       | /xmp/tiff:Software                           |
|       | /xmp/tiff:software                           |
|       | /app13/irb/8bimiptc/iptc/Originating Program |



 

### <a name="tiff-policy"></a>Directiva TIFF

### <a name="read-paths"></a>Rutas de acceso de lectura



| Pedido | Ruta de acceso                                       | Formato de disco |
|-------|--------------------------------------------|-------------|
|       | /ifd/{ushort=305}                          | ascii       |
|       | /ifd/iptc/Originating Program              |             |
|       | /ifd/xmp/xmp:CreatorTool                   | unicode     |
|       | /ifd/xmp/xmp:creatortool                   | unicode     |
|       | /ifd/xmp/tiff:Software                     | unicode     |
|       | /ifd/xmp/tiff:software                     | unicode     |
|       | /ifd/iptc/Originating Program              |             |
|       | /ifd/irb/8bimiptc/iptc/Originating Program |             |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Ruta de acceso                                       | Formato de disco |
|-------|--------------------------------------------|-------------|
|       | /ifd/{ushort=305}                          | ascii       |
|       | /ifd/xmp/xmp:CreatorTool                   | unicode     |
|       | /ifd/xmp/xmp:creatortool                   | unicode     |
|       | /ifd/xmp/tiff:Software                     | unicode     |
|       | /ifd/xmp/tiff:software                     | unicode     |
|       | /ifd/iptc/Originating Program              |             |
|       | /ifd/irb/8bimiptc/iptc/Originating Program |             |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                                       |
|-------|--------------------------------------------|
|       | /ifd/{ushort=305}                          |
|       | /ifd/xmp/xmp:CreatorTool                   |
|       | /ifd/xmp/xmp:creatortool                   |
|       | /ifd/xmp/tiff:Software                     |
|       | /ifd/xmp/tiff:software                     |
|       | /ifd/iptc/Originating Program              |
|       | /ifd/irb/8bimiptc/iptc/Originating Program |



 

## <a name="remarks"></a>Comentarios

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System.ApplicationName](../properties/props-system-applicationname.md)
</dt> </dl>

 

 
