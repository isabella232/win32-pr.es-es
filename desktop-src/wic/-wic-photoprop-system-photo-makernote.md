---
description: La Directiva de metadatos de fotos para la propiedad System. Photo. MakerNote.
ms.assetid: e1018bc6-3fd2-4212-afee-6811bfe99f14
title: Directiva de metadatos de la foto de System. Photo. MakerNote
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0df1a16205d6a9d1229d3627e6b9cc8c746d8a69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105677967"
---
# <a name="systemphotomakernote-photo-metadata-policy"></a>Directiva de metadatos de la foto de System. Photo. MakerNote

La Directiva de metadatos de fotos para la propiedad [System. Photo. MakerNote](../properties/props-system-photo-makernote.md) .

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ MakerNote

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

No

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de salida

\_VTUI1 de vector de VT \|

### <a name="input-type"></a>Tipo de entrada

Buffer

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Se reconcilian los valores de los distintos esquemas.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /app1/IFD/Exif/{ushort = 37500} |             |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /app1/IFD/Exif/{ushort = 37500} |             |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                          |
|-------|-------------------------------|
| 1     | /app1/IFD/Exif/{ushort = 37500} |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                     | Formato de disco |
|-------|--------------------------|-------------|
| 1     | /IFD/Exif/{ushort = 37500} |             |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                     | Formato de disco |
|-------|--------------------------|-------------|
| 1     | /IFD/Exif/{ushort = 37500} |             |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                     |
|-------|--------------------------|
| 1     | /IFD/Exif/{ushort = 37500} |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System. Photo. MakerNote](../properties/props-system-photo-makernote.md)
</dt> </dl>

 

 
