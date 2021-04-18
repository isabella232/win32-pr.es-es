---
description: La Directiva de metadatos de fotos para la propiedad System. Photo. CameraManufacturer.
ms.assetid: 6710161c-4835-4385-9d4c-566acc000925
title: Directiva de metadatos de la foto de System. Photo. CameraManufacturer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd1d2765b6c787b7d7ad421300f1c3492669830b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706999"
---
# <a name="systemphotocameramanufacturer-photo-metadata-policy"></a>Directiva de metadatos de la foto de System. Photo. CameraManufacturer

La Directiva de metadatos de fotos para la propiedad [System. Photo. CameraManufacturer](../properties/props-system-photo-cameramanufacturer.md) .

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ CameraManufacturer

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
| 1     | /app1/IFD/{ushort = 271} | ascii       |
| 2     | /XMP/TIFF: make         | unicode     |
| 3     | /XMP/TIFF: make         | unicode     |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                   | Formato de disco |
|-------|------------------------|-------------|
| 1     | /app1/IFD/{ushort = 271} | ascii       |
| 2     | /XMP/TIFF: make         | unicode     |
| 3     | /XMP/TIFF: make         | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                   |
|-------|------------------------|
| 1     | /app1/IFD/{ushort = 271} |
| 2     | /XMP/TIFF: make         |
| 3     | /XMP/TIFF: make         |



 

### <a name="tiff-policy"></a>Directiva TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta               | Formato de disco |
|-------|--------------------|-------------|
| 1     | /IFD/{ushort = 271}  | ascii       |
| 2     | /IFD/XMP/TIFF: make | unicode     |
| 3     | /IFD/XMP/TIFF: make | unicode     |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta               | Formato de disco |
|-------|--------------------|-------------|
| 1     | /IFD/{ushort = 271}  | ascii       |
| 2     | /IFD/XMP/TIFF: make | unicode     |
| 3     | /IFD/XMP/TIFF: make | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta               |
|-------|--------------------|
| 1     | /IFD/{ushort = 271}  |
| 2     | /IFD/XMP/TIFF: make |
| 3     | /IFD/XMP/TIFF: make |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System. Photo. CameraManufacturer](../properties/props-system-photo-cameramanufacturer.md)
</dt> </dl>

 

 
