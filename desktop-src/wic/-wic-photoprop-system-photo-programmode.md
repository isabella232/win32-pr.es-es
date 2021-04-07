---
description: La Directiva de metadatos de fotos para la propiedad System. Photo. ProgramMode.
ms.assetid: f1954dc7-d4df-4675-ab3b-a65f2354e57a
title: Directiva de metadatos de la foto de System. Photo. ProgramMode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6f5dffa822454509134c485e4792f4be4270912
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002578"
---
# <a name="systemphotoprogrammode-photo-metadata-policy"></a>Directiva de metadatos de la foto de System. Photo. ProgramMode

La Directiva de metadatos de fotos para la propiedad [System. Photo. ProgramMode](../properties/props-system-photo-programmode.md) .

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ ProgramMode

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
| 1     | /app1/IFD/Exif/{ushort = 34850} | ushort      |
| 2     | /xmp/exif:ExposureProgram     | unicode     |
| 3     | /xmp/exif:ProgramMode         | unicode     |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /app1/IFD/Exif/{ushort = 34850} | ushort      |
| 2     | /xmp/exif:ExposureProgram     | unicode     |
| 3     | /xmp/exif:ProgramMode         | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                          |
|-------|-------------------------------|
| 1     | /app1/IFD/Exif/{ushort = 34850} |
| 2     | /xmp/exif:exposureprogram     |
| 3     | /xmp/exif:programmode         |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /IFD/Exif/{ushort = 34850}      | ushort      |
| 2     | /ifd/xmp/exif:ExposureProgram | unicode     |
| 3     | /ifd/xmp/exif:ProgramMode     | unicode     |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /IFD/Exif/{ushort = 34850}      | ushort      |
| 2     | /ifd/xmp/exif:ExposureProgram | unicode     |
| 3     | /ifd/xmp/exif:ProgramMode     | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                          |
|-------|-------------------------------|
| 1     | /IFD/Exif/{ushort = 34850}      |
| 2     | /ifd/xmp/exif:exposureprogram |
| 3     | /ifd/xmp/exif:programmode     |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System. Photo. ProgramMode](../properties/props-system-photo-programmode.md)
</dt> </dl>

 

 
