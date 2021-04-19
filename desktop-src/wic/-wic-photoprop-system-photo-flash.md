---
description: La Directiva de metadatos de fotos para la propiedad System. Photo. Flash.
ms.assetid: 24b400a4-f4c7-4b59-a9e3-8a20144cd52e
title: Directiva de metadatos de foto de System. Photo. Flash
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0302e0f310d2f9a6a4390b0d4856578cc2f43e93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678097"
---
# <a name="systemphotoflash-photo-metadata-policy"></a>Directiva de metadatos de foto de System. Photo. Flash

La Directiva de metadatos de fotos para la propiedad [System. Photo. Flash](../properties/props-system-photo-exposuretime.md) .

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ Flash

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

No

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de salida

VT \_ UI1 (si el esquema de origen era XMP) o VT \_ UI2 (si el esquema de origen es EXIF)

\\lang1036

### <a name="input-type"></a>Tipo de entrada

VT \_ UI1, VTUI2, VT \_ UI4

\\lang1033

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Se reconcilian los valores de los distintos esquemas.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                             | Formato de disco |
|-------|----------------------------------|-------------|
| 1     | /app1/IFD/Exif/{ushort = 37385}    | ushort      |
| 2     | /XMP/ <xmpstruct> Exif: Flash |             |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                             | Formato de disco |
|-------|----------------------------------|-------------|
| 1     | /app1/IFD/Exif/{ushort = 37385}    | ushort      |
| 2     | /XMP/ <xmpstruct> Exif: Flash |             |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                             |
|-------|----------------------------------|
| 1     | /app1/IFD/Exif/{ushort = 37385}    |
| 2     | /XMP/ <xmpstruct> Exif: Flash |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                                 | Formato de disco |
|-------|--------------------------------------|-------------|
| 1     | /IFD/Exif/{ushort = 37385}             | ushort      |
| 2     | /IFD/XMP/ <xmpstruct> Exif: Flash |             |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                                 | Formato de disco |
|-------|--------------------------------------|-------------|
| 1     | /IFD/Exif/{ushort = 37385}             | ushort      |
| 2     | /IFD/XMP/ <xmpstruct> Exif: Flash |             |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                                 |
|-------|--------------------------------------|
| 1     | /IFD/Exif/{ushort = 37385}             |
| 2     | /IFD/XMP/ <xmpstruct> Exif: Flash |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System. Photo. Flash](../properties/props-system-photo-exposuretime.md)
</dt> </dl>

 

 
