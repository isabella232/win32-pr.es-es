---
description: Directiva de metadatos de fotos para la propiedad System.Photo.LensModel.
ms.assetid: 39aeff17-e8d3-4ceb-86a1-1749d2ca98d6
title: Directiva de metadatos de fotos System.Photo.LensModel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a07fff44e14a04dab220f8dbce243a638710f30db253c43c1ff79a240bb32f3e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119441875"
---
# <a name="systemphotolensmodel-photo-metadata-policy"></a>Directiva de metadatos de fotos System.Photo.LensModel

Directiva de metadatos de fotos para [la propiedad System.Photo.LensModel.](../properties/props-system-photo-lensmodel.md)

### <a name="pkey"></a>Pkey

PKEY \_ Photo \_ LensModel

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

No

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de salida

VT \_ LPWSTR

### <a name="input-type"></a>Tipo de entrada

String.

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Los valores de esquemas diferentes se concilian.

### <a name="precedence-of-paths-jpeg"></a>Prioridad de las rutas de acceso (JPEG)

Si el archivo está en formato JPEG, el controlador usará la ruta de acceso siguiente al leer o escribir los datos.



| Pedido | Ruta de acceso                          | Formato de disco | Requerido |
|-------|-------------------------------|-------------|----------|
| 1     | /xmp/MicrosoftPhoto:LensModel | Unicode     | Sí      |



 

### <a name="precedence-of-paths-tiff"></a>Precedencia de rutas de acceso (TIFF)

Si el archivo está en formato TIFF, el controlador usará el siguiente orden de prioridad al leer o escribir los datos.



| Pedido | Ruta de acceso                              | Formato de disco | Requerido |
|-------|-----------------------------------|-------------|----------|
| 1     | /ifd/xmp/MicrosoftPhoto:LensModel | Unicode     | Sí      |



 

## <a name="remarks"></a>Comentarios

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System.Photo.LensModel](../properties/props-system-photo-lensmodel.md)
</dt> </dl>

 

 
