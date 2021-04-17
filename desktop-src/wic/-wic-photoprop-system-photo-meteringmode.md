---
description: La Directiva de metadatos de fotos para la propiedad System. Photo. MeteringMode.
ms.assetid: cb0bf0d5-eccf-4345-a242-76769c34e02d
title: Directiva de metadatos de la foto de System. Photo. MeteringMode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12a4443521c84113e4e2a6f4c2b9b2b3f822ae90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678226"
---
# <a name="systemphotometeringmode-photo-metadata-policy"></a>Directiva de metadatos de la foto de System. Photo. MeteringMode

La Directiva de metadatos de fotos para la propiedad [System. Photo. MeteringMode](../properties/props-system-photo-meteringmode.md) .

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ MeteringMode

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

No

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de salida

VT \_ UI2

### <a name="input-type"></a>Tipo de entrada

UShort

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Se reconcilian los valores de los distintos esquemas.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /app1/IFD/Exif/{ushort = 37383} | ushort      |
| 2     | /xmp/exif:MeteringMode        | unicode     |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /app1/IFD/Exif/{ushort = 37383} | ushort      |
| 2     | /xmp/exif:MeteringMode        | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                          |
|-------|-------------------------------|
| 1     | /app1/IFD/Exif/{ushort = 37383} |
| 2     | /xmp/exif:meteringmode        |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                       | Formato de disco |
|-------|----------------------------|-------------|
| 1     | /IFD/Exif/{ushort = 37383}   | ushort      |
| 2     | /ifd/xmp/exif:MeteringMode | unicode     |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                       | Formato de disco |
|-------|----------------------------|-------------|
| 1     | /IFD/Exif/{ushort = 37383}   | ushort      |
| 2     | /ifd/xmp/exif:MeteringMode | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                       |
|-------|----------------------------|
| 1     | /IFD/Exif/{ushort = 37383}   |
| 2     | /ifd/xmp/exif:meteringmode |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System. Photo. MeteringMode](../properties/props-system-photo-meteringmode.md)
</dt> </dl>

 

 
