---
description: La Directiva de metadatos de fotos para la propiedad System. Photo. FlashModel.
ms.assetid: ef322823-1b87-40ea-a5e3-e7551f14e44d
title: Directiva de metadatos de la foto de System. Photo. FlashModel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01ade3769cb0d852239af84b769b85d5b3849589
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716395"
---
# <a name="systemphotoflashmodel-photo-metadata-policy"></a>Directiva de metadatos de la foto de System. Photo. FlashModel

La Directiva de metadatos de fotos para la propiedad [System. Photo. FlashModel](../properties/props-system-photo-flashmodel.md) .

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ FlashModel

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



| Pedido | Ruta                           | Formato de disco | Formato de datos | Obligatorio |
|-------|--------------------------------|-------------|-------------|----------|
| 1     | /xmp/MicrosoftPhoto:FlashModel | Unicode     |             | Sí      |



 

### <a name="precedence-of-paths-tiff"></a>Prioridad de las rutas de acceso (TIFF)

Si el archivo está en formato TIFF, el controlador usará el orden de prioridad siguiente al leer o escribir los datos.



| Pedido | Ruta                               | Formato de disco | Formato de datos | Obligatorio |
|-------|------------------------------------|-------------|-------------|----------|
| 1     | /ifd/xmp/MicrosoftPhoto:FlashModel | Unicode     |             | Sí      |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System. Photo. FlashModel](../properties/props-system-photo-flashmodel.md)
</dt> </dl>

 

 
