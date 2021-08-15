---
description: Directiva de metadatos de fotos para la propiedad System.Photo.CameraManufacturer.
ms.assetid: 6710161c-4835-4385-9d4c-566acc000925
title: System.Photo.CameraManufacturer Photo Metadata Policy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37744420babedf6b398cdf3ab9007c3895c09d33b9254221b5ba4760ab917a0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119087091"
---
# <a name="systemphotocameramanufacturer-photo-metadata-policy"></a>System.Photo.CameraManufacturer Photo Metadata Policy

Directiva de metadatos de fotos [para la propiedad System.Photo.CameraManufacturer.](../properties/props-system-photo-cameramanufacturer.md)

### <a name="pkey"></a>Pkey

PKEY \_ Photo \_ CameraManufacturer

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

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta de acceso                   | Formato de disco |
|-------|------------------------|-------------|
| 1     | /app1/ifd/{ushort=271} | ascii       |
| 2     | /xmp/tiff:Make         | unicode     |
| 3     | /xmp/tiff:make         | unicode     |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Ruta de acceso                   | Formato de disco |
|-------|------------------------|-------------|
| 1     | /app1/ifd/{ushort=271} | ascii       |
| 2     | /xmp/tiff:Make         | unicode     |
| 3     | /xmp/tiff:make         | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                   |
|-------|------------------------|
| 1     | /app1/ifd/{ushort=271} |
| 2     | /xmp/tiff:Make         |
| 3     | /xmp/tiff:make         |



 

### <a name="tiff-policy"></a>Directiva TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta de acceso               | Formato de disco |
|-------|--------------------|-------------|
| 1     | /ifd/{ushort=271}  | ascii       |
| 2     | /ifd/xmp/tiff:Make | unicode     |
| 3     | /ifd/xmp/tiff:make | unicode     |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Ruta de acceso               | Formato de disco |
|-------|--------------------|-------------|
| 1     | /ifd/{ushort=271}  | ascii       |
| 2     | /ifd/xmp/tiff:Make | unicode     |
| 3     | /ifd/xmp/tiff:make | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso               |
|-------|--------------------|
| 1     | /ifd/{ushort=271}  |
| 2     | /ifd/xmp/tiff:Make |
| 3     | /ifd/xmp/tiff:make |



 

## <a name="remarks"></a>Comentarios

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System.Photo.CameraManufacturer](../properties/props-system-photo-cameramanufacturer.md)
</dt> </dl>

 

 
