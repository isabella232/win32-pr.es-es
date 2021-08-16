---
description: Directiva de metadatos de fotos para la propiedad System.DateAcquired.
ms.assetid: 04a61ecc-d168-4f93-b143-3e6ba8aaf322
title: Directiva de metadatos de fotos System.DateAcquired
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c95b8f68d99476db0832a321de1f61c6f3c4dc6be6f10d679735bd51fc92ce7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119087886"
---
# <a name="systemdateacquired-photo-metadata-policy"></a>Directiva de metadatos de fotos System.DateAcquired

Directiva de metadatos de fotos para [la propiedad System.DateAcquired.](../properties/props-system-dateacquired.md)

### <a name="pkey"></a>Pkey

PKEY \_ DateAcquired

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

No

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de salida

VT \_ FILETIME

### <a name="input-propvariant-type"></a>Tipo PROPVARIANT de entrada

VT \_ FILETIME

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Los valores de esquemas diferentes se concilian.

### <a name="precedence-of-paths-jpeg"></a>Prioridad de las rutas de acceso (JPEG)

Si el archivo está en formato JPEG, el controlador busca los datos en el orden siguiente:



| Pedido | Ruta de acceso                             | Formato de disco                        | Requerido |
|-------|----------------------------------|------------------------------------|----------|
| 1     | /xmp/MicrosoftPhoto:DateAcquired | Cadena Unicode en formato de fecha XMP. | Sí      |



 

### <a name="precedence-of-paths-tiff"></a>Precedencia de rutas de acceso (TIFF)

Si el archivo está en formato TIFF, el controlador busca los datos en el orden siguiente:



| Pedido | Ruta de acceso                                 | Formato de disco                        | Requerido |
|-------|--------------------------------------|------------------------------------|----------|
| 1     | /ifd/xmp/MicrosoftPhoto:DateAcquired | Cadena Unicode en formato de fecha XMP. | Sí      |



 

## <a name="remarks"></a>Comentarios

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System.DateAcquired](../properties/props-system-dateacquired.md)
</dt> </dl>

 

 
