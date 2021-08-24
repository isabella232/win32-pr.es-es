---
description: Directiva de metadatos de fotos para la propiedad System.Photo.LensManufacturer.
ms.assetid: ee25da96-982f-475e-8957-e24ef7721b78
title: Directiva de metadatos de fotos de System.Photo.LensManufacturer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f6beebc06ce690b05da62c023480bec25b675a7a9ec6093cec1752ac3a0e343
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119881994"
---
# <a name="systemphotolensmanufacturer-photo-metadata-policy"></a>Directiva de metadatos de fotos de System.Photo.LensManufacturer

Directiva de metadatos de fotos [para la propiedad System.Photo.LensManufacturer.](../properties/props-system-photo-lensmanufacturer.md)

### <a name="pkey"></a>Pkey

PKEY \_ Photo \_ LensManufacturer

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

No

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de salida

VT \_ LPWSTR

### <a name="input-type"></a>Tipo de entrada

String.

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Se concilian los valores de esquemas diferentes.

### <a name="precedence-of-paths-jpeg"></a>Prioridad de las rutas de acceso (JPEG)

Si el archivo está en formato JPEG, el controlador usará la ruta de acceso siguiente al leer o escribir los datos.



| Pedido | Ruta de acceso                                 | Formato de disco | Requerido |
|-------|--------------------------------------|-------------|----------|
| 1     | /xmp/MicrosoftPhoto:LensManufacturer | Unicode     | Sí      |



 

### <a name="precedence-of-paths-tiff"></a>Precedencia de rutas de acceso (TIFF)

Si el archivo está en formato TIFF, el controlador usará el siguiente orden de prioridad al leer o escribir los datos.



| Pedido | Ruta de acceso                                     | Formato de disco | Requerido |
|-------|------------------------------------------|-------------|----------|
| 1     | /ifd/xmp/MicrosoftPhoto:LensManufacturer | Unicode     | Sí      |



 

## <a name="remarks"></a>Comentarios

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System.Photo.LensManufacturer](../properties/props-system-photo-lensmanufacturer.md)
</dt> </dl>

 

 
