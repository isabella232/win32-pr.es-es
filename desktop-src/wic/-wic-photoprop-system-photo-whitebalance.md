---
description: La Directiva de metadatos de fotos para la propiedad System. Photo. WhiteBalance.
ms.assetid: 7b3a31e6-a929-41e4-b7f0-c5b3beac2519
title: Directiva de metadatos de la foto de System. Photo. WhiteBalance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc333cedcd4665ace37033452ec3c7f0336f13e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706835"
---
# <a name="systemphotowhitebalance-photo-metadata-policy"></a>Directiva de metadatos de la foto de System. Photo. WhiteBalance

La Directiva de metadatos de fotos para la propiedad [System. Photo. Whitebalance](../properties/props-system-photo-whitebalance.md) .

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ Whitebalance

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

No

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de salida

VT \_ UI4

### <a name="input-type"></a>Tipo de entrada

UShort

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Se reconcilian los valores de los distintos esquemas.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /app1/IFD/Exif/{ushort = 41987} | ushort      |
| 2     | /xmp/exif:WhiteBalance        | unicode     |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /app1/IFD/Exif/{ushort = 41987} | ushort      |
| 2     | /xmp/exif:WhiteBalance        | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                          |
|-------|-------------------------------|
| 1     | /app1/IFD/Exif/{ushort = 41987} |
| 2     | /xmp/exif:whitebalance        |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                       | Formato de disco |
|-------|----------------------------|-------------|
| 1     | /IFD/Exif/{ushort = 41987}   | ushort      |
| 2     | /ifd/xmp/exif:WhiteBalance | unicode     |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                       | Formato de disco |
|-------|----------------------------|-------------|
| 1     | /IFD/Exif/{ushort = 41987}   | ushort      |
| 2     | /ifd/xmp/exif:WhiteBalance | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                       |
|-------|----------------------------|
| 1     | /IFD/Exif/{ushort = 41987}   |
| 2     | /ifd/xmp/exif:whitebalance |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System. Photo. WhiteBalance](../properties/props-system-photo-whitebalance.md)
</dt> </dl>

 

 
