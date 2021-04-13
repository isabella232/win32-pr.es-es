---
description: La Directiva de metadatos de la fotografía para la propiedad System. DateAcquired.
ms.assetid: 04a61ecc-d168-4f93-b143-3e6ba8aaf322
title: Directiva de metadatos de la foto System. DateAcquired
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f126ccb4424d1489f671f61f719a505559a78c8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278840"
---
# <a name="systemdateacquired-photo-metadata-policy"></a>Directiva de metadatos de la foto System. DateAcquired

La Directiva de metadatos de la fotografía para la propiedad [System. DateAcquired](../properties/props-system-dateacquired.md) .

### <a name="pkey"></a>PKEY

PKEY \_ DateAcquired

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

No

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de salida

VT \_ FILETIME

### <a name="input-propvariant-type"></a>Tipo de PROPVARIANT de entrada

VT \_ FILETIME

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Se reconcilian los valores de los distintos esquemas.

### <a name="precedence-of-paths-jpeg"></a>Prioridad de las rutas de acceso (JPEG)

Si el archivo está en formato JPEG, el controlador busca los datos en el orden siguiente:



| Pedido | Ruta                             | Formato de disco                        | Obligatorio |
|-------|----------------------------------|------------------------------------|----------|
| 1     | /xmp/MicrosoftPhoto:DateAcquired | Cadena Unicode en formato de fecha XMP. | Sí      |



 

### <a name="precedence-of-paths-tiff"></a>Prioridad de las rutas de acceso (TIFF)

Si el archivo está en formato TIFF, el controlador busca los datos en el orden siguiente:



| Pedido | Ruta                                 | Formato de disco                        | Obligatorio |
|-------|--------------------------------------|------------------------------------|----------|
| 1     | /ifd/xmp/MicrosoftPhoto:DateAcquired | Cadena Unicode en formato de fecha XMP. | Sí      |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System. DateAcquired](../properties/props-system-dateacquired.md)
</dt> </dl>

 

 
