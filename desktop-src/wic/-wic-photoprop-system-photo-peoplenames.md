---
description: Directiva de metadatos de fotos para la propiedad System.Photo.PeopleNames.
ms.assetid: 567d5542-fc7b-4d19-bc3c-b9d6e26e3387
title: Directiva de metadatos de fotos System.Photo.PeopleNames
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4118cc8242d6dfe8a91d0bcd2b6039095fdf180037f51205d3541b9aefa2cc0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119087057"
---
# <a name="systemphotopeoplenames-photo-metadata-policy"></a>Directiva de metadatos de fotos System.Photo.PeopleNames

Directiva de metadatos de fotos para [la propiedad System.Photo.PeopleNames.](../properties/props-system-photo-peoplenames.md)

### <a name="pkey"></a>Pkey

PKEY \_ Photo \_ PeopleNames

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

No

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de salida

VT \_ VECTOR \| VT \_ LPWSTR

### <a name="input-type"></a>Tipo de entrada

StringMulti

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Se concilian los valores de esquemas diferentes.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Rutas de acceso de lectura



| Pedido | Ruta de acceso                                                           | Formato de disco |
|-------|----------------------------------------------------------------|-------------|
| 1     | /xmp/ <xmpstruct> MP:RegionInfo/ <xmpbag> MPRI:Regions | ushort      |



 

### <a name="write-paths"></a>Rutas de acceso de escritura

Esta propiedad no se puede escribir mediante la directiva de metadatos.

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                                |
|-------|-------------------------------------|
| 1     | /xmp/ <xmpstruct> MP:RegionInfo |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Rutas de acceso de lectura



| Pedido | Ruta de acceso                                                               | Formato de disco |
|-------|--------------------------------------------------------------------|-------------|
| 1     | /ifd/xmp/ <xmpstruct> MP:RegionInfo/ <xmpbag> MPRI:Regions | ushort      |



 

### <a name="write-paths"></a>Rutas de acceso de escritura

Esta propiedad no se puede escribir mediante la directiva de metadatos.

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                                    |
|-------|-----------------------------------------|
| 1     | /ifd/xmp/ <xmpstruct> MP:RegionInfo |



 

## <a name="remarks"></a>Comentarios

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System.Photo.ProgramMode](../properties/props-system-photo-programmode.md)
</dt> </dl>

 

 
