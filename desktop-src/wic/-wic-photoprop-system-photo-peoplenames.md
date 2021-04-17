---
description: La Directiva de metadatos de fotos para la propiedad System. Photo. PeopleNames.
ms.assetid: 567d5542-fc7b-4d19-bc3c-b9d6e26e3387
title: Directiva de metadatos de la foto de System. Photo. PeopleNames
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c3de9f5adda67fcd0e555194500f109df078bdf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678225"
---
# <a name="systemphotopeoplenames-photo-metadata-policy"></a>Directiva de metadatos de la foto de System. Photo. PeopleNames

La Directiva de metadatos de fotos para la propiedad [System. Photo. PeopleNames](../properties/props-system-photo-peoplenames.md) .

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ PeopleNames

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

No

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de salida

VT \_ Vector \| VT \_ LPWStr

### <a name="input-type"></a>Tipo de entrada

StringMulti

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Se reconcilian los valores de los distintos esquemas.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                                                           | Formato de disco |
|-------|----------------------------------------------------------------|-------------|
| 1     | módulo de administración de/XMP/ <xmpstruct> : RegionInfo/ <xmpbag> mpri: regiones | ushort      |



 

### <a name="write-paths"></a>Escribir rutas de acceso

Esta propiedad no se puede escribir con la Directiva de metadatos.

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                                |
|-------|-------------------------------------|
| 1     | módulo de administración de/XMP/ <xmpstruct> : RegionInfo |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                                                               | Formato de disco |
|-------|--------------------------------------------------------------------|-------------|
| 1     | módulo de administración de/IFD/XMP/ <xmpstruct> : RegionInfo/ <xmpbag> mpri: regiones | ushort      |



 

### <a name="write-paths"></a>Escribir rutas de acceso

Esta propiedad no se puede escribir con la Directiva de metadatos.

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                                    |
|-------|-----------------------------------------|
| 1     | módulo de administración de/IFD/XMP/ <xmpstruct> : RegionInfo |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System. Photo. ProgramMode](../properties/props-system-photo-programmode.md)
</dt> </dl>

 

 
