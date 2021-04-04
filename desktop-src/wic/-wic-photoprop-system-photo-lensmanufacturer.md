---
description: La Directiva de metadatos de fotos para la propiedad System. Photo. LensManufacturer.
ms.assetid: ee25da96-982f-475e-8957-e24ef7721b78
title: Directiva de metadatos de la foto de System. Photo. LensManufacturer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6696e7113a14a9b5b26a26f38258f30a5ba82cf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278188"
---
# <a name="systemphotolensmanufacturer-photo-metadata-policy"></a>Directiva de metadatos de la foto de System. Photo. LensManufacturer

La Directiva de metadatos de fotos para la propiedad [System. Photo. LensManufacturer](../properties/props-system-photo-lensmanufacturer.md) .

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ LensManufacturer

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



| Pedido | Ruta                                 | Formato de disco | Obligatorio |
|-------|--------------------------------------|-------------|----------|
| 1     | /xmp/MicrosoftPhoto:LensManufacturer | Unicode     | Sí      |



 

### <a name="precedence-of-paths-tiff"></a>Prioridad de las rutas de acceso (TIFF)

Si el archivo está en formato TIFF, el controlador usará el orden de prioridad siguiente al leer o escribir los datos.



| Pedido | Ruta                                     | Formato de disco | Obligatorio |
|-------|------------------------------------------|-------------|----------|
| 1     | /ifd/xmp/MicrosoftPhoto:LensManufacturer | Unicode     | Sí      |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System. Photo. LensManufacturer](../properties/props-system-photo-lensmanufacturer.md)
</dt> </dl>

 

 
