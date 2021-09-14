---
description: Directiva de metadatos de fotos para la propiedad System.Photo.PeopleNames.
ms.assetid: 567d5542-fc7b-4d19-bc3c-b9d6e26e3387
title: Directiva de metadatos de fotos System.Photo.PeopleNames
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5540356001cdd33bb7c0d3340534f9c69e230a5d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127267343"
---
# <a name="systemphotopeoplenames-photo-metadata-policy"></a>Directiva de metadatos de fotos System.Photo.PeopleNames

Directiva de metadatos de fotos para [la propiedad System.Photo.PeopleNames.](../properties/props-system-photo-peoplenames.md)

### <a name="pkey"></a>PKEY

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

Los valores de esquemas diferentes se concilian.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Path                                                           | Formato de disco |
|-------|----------------------------------------------------------------|-------------|
| 1     | /xmp/ &lt; xmpstruct &gt; MP:RegionInfo/ &lt; xmpbag &gt; MPRI:Regions | ushort      |



 

### <a name="write-paths"></a>Rutas de acceso de escritura

Esta propiedad no se puede escribir mediante la directiva de metadatos.

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Path                                |
|-------|-------------------------------------|
| 1     | /xmp/ &lt; xmpstruct &gt; MP:RegionInfo |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Path                                                               | Formato de disco |
|-------|--------------------------------------------------------------------|-------------|
| 1     | /ifd/xmp/ &lt; xmpstruct &gt; MP:RegionInfo/ &lt; xmpbag &gt; MPRI:Regions | ushort      |



 

### <a name="write-paths"></a>Rutas de acceso de escritura

Esta propiedad no se puede escribir mediante la directiva de metadatos.

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Path                                    |
|-------|-----------------------------------------|
| 1     | /ifd/xmp/ &lt; xmpstruct &gt; MP:RegionInfo |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System.Photo.ProgramMode](../properties/props-system-photo-programmode.md)
</dt> </dl>

 

 
