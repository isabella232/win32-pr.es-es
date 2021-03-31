---
description: La Directiva de metadatos de fotos para la propiedad System. Photo. CameraModel.
ms.assetid: ff85e6ee-dc75-45bc-a406-2290b012c22d
title: Directiva de metadatos de la foto de System. Photo. CameraModel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2cf9cbb2906f15d02e8d72219862c607d0f515a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912622"
---
# <a name="systemphotocameramodel-photo-metadata-policy"></a>Directiva de metadatos de la foto de System. Photo. CameraModel

La Directiva de metadatos de fotos para la propiedad [System. Photo. CameraModel](../properties/props-system-photo-cameramodel.md) .

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ CameraModel

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

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                   | Formato de disco |
|-------|------------------------|-------------|
| 1     | /app1/IFD/{ushort = 272} | ascii       |
| 2     | /XMP/TIFF: modelo        | unicode     |
| 3     | /XMP/TIFF: modelo        | unicode     |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                   | Formato de disco |
|-------|------------------------|-------------|
| 1     | /app1/IFD/{ushort = 272} | ascii       |
| 2     | /XMP/TIFF: modelo        | unicode     |
| 3     | /XMP/TIFF: modelo        | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                   |
|-------|------------------------|
| 1     | /app1/IFD/{ushort = 272} |
| 2     | /XMP/TIFF: modelo        |
| 3     | /XMP/TIFF: modelo        |



 

### <a name="tiff-policy"></a>Directiva TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                | Formato de disco |
|-------|---------------------|-------------|
| 1     | /IFD/{ushort = 272}   | ascii       |
| 2     | /IFD/XMP/TIFF: modelo | unicode     |
| 3     | /IFD/XMP/TIFF: modelo | unicode     |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                | Formato de disco |
|-------|---------------------|-------------|
| 1     | /IFD/{ushort = 272}   | ascii       |
| 2     | /IFD/XMP/TIFF: modelo | unicode     |
| 3     | /IFD/XMP/TIFF: modelo | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                |
|-------|---------------------|
| 1     | /IFD/{ushort = 272}   |
| 2     | /IFD/XMP/TIFF: modelo |
| 3     | /IFD/XMP/TIFF: modelo |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System. Photo. CameraModel](../properties/props-system-photo-cameramodel.md)
</dt> </dl>

 

 
