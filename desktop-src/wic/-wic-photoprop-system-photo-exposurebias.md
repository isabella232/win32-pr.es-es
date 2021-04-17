---
description: La Directiva de metadatos de fotos para la propiedad System. Photo. ExposureBias.
ms.assetid: 00ebe037-0116-4d75-868b-d75b3e58a84d
title: Directiva de metadatos de la foto de System. Photo. ExposureBias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 709aa21da7cec56d36b5de643681a592873717bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678100"
---
# <a name="systemphotoexposurebias-photo-metadata-policy"></a>Directiva de metadatos de la foto de System. Photo. ExposureBias

La Directiva de metadatos de fotos para la propiedad [System. Photo. ExposureBias](../properties/props-system-photo-exposurebias.md) .

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ ExposureBias

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

Sí

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de salida

VT \_ R8

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Este valor se genera a partir de System. Photo. ExposureBiasNumerator y System. Photo. ExposureBiasDenominator. No se puede escribir directamente. Se reconcilian los valores de los distintos esquemas.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /app1/IFD/Exif/{ushort = 37380} |             |
| 2     | /xmp/exif:ExposureBiasValue   |             |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /app1/IFD/Exif/{ushort = 37380} |             |
| 2     | /xmp/exif:ExposureBiasValue   |             |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                          |
|-------|-------------------------------|
| 1     | /app1/IFD/Exif/{ushort = 37380} |
| 2     | /xmp/exif:exposurebiasvalue   |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                            | Formato de disco |
|-------|---------------------------------|-------------|
| 1     | /IFD/Exif/{ushort = 37380}        |             |
| 2     | /ifd/xmp/exif:ExposureBiasValue |             |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                            | Formato de disco |
|-------|---------------------------------|-------------|
| 1     | /IFD/Exif/{ushort = 37380}        |             |
| 2     | /ifd/xmp/exif:ExposureBiasValue |             |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                            |
|-------|---------------------------------|
| 1     | /IFD/Exif/{ushort = 37380}        |
| 2     | /ifd/xmp/exif:exposurebiasvalue |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System. Photo. ExposureBias](../properties/props-system-photo-exposurebias.md)
</dt> </dl>

 

 
