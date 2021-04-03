---
description: La Directiva de metadatos de fotos para la propiedad System. Photo. LensModel.
ms.assetid: 39aeff17-e8d3-4ceb-86a1-1749d2ca98d6
title: Directiva de metadatos de la foto de System. Photo. LensModel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8a5249136346407ab9fcd1e4802d6910d3e514a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083168"
---
# <a name="systemphotolensmodel-photo-metadata-policy"></a>Directiva de metadatos de la foto de System. Photo. LensModel

La Directiva de metadatos de fotos para la propiedad [System. Photo. LensModel](../properties/props-system-photo-lensmodel.md) .

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ LensModel

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

No

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de salida

VT \_ LPWStr

### <a name="input-type"></a>Tipo de entrada

String.

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Se reconcilian los valores de los distintos esquemas.

### <a name="precedence-of-paths-jpeg"></a>Prioridad de las rutas de acceso (JPEG)

Si el archivo está en formato JPEG, el controlador usará la siguiente ruta de acceso al leer o escribir los datos.



| Pedido | Ruta                          | Formato de disco | Obligatorio |
|-------|-------------------------------|-------------|----------|
| 1     | /xmp/MicrosoftPhoto:LensModel | Unicode     | Sí      |



 

### <a name="precedence-of-paths-tiff"></a>Prioridad de las rutas de acceso (TIFF)

Si el archivo está en formato TIFF, el controlador usará el orden de prioridad siguiente al leer o escribir los datos.



| Pedido | Ruta                              | Formato de disco | Obligatorio |
|-------|-----------------------------------|-------------|----------|
| 1     | /ifd/xmp/MicrosoftPhoto:LensModel | Unicode     | Sí      |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System. Photo. LensModel](../properties/props-system-photo-lensmodel.md)
</dt> </dl>

 

 
