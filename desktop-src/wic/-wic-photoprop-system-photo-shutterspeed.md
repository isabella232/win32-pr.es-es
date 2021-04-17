---
description: La Directiva de metadatos de fotos para la propiedad System. Photo. ShutterSpeed.
ms.assetid: f320944c-978d-4a3c-9bf8-5c5652123e29
title: Directiva de metadatos de la foto de System. Photo. ShutterSpeed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8df8c9e7fda5643fed022f67c3b6b7846e7a72f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678221"
---
# <a name="systemphotoshutterspeed-photo-metadata-policy"></a>Directiva de metadatos de la foto de System. Photo. ShutterSpeed

La Directiva de metadatos de fotos para la propiedad [System. Photo. ShutterSpeed](../properties/props-system-photo-shutterspeed.md) .

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ ShutterSpeed

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

Sí

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de salida

VT \_ R8

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Este valor se genera a partir de System. Photo. ShutterSpeedNumerator y System. Photo. ShutterSpeedDenominator. No se puede escribir directamente. Se reconcilian los valores de los distintos esquemas.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /app1/IFD/Exif/{ushort = 37377} |             |
| 2     | /xmp/exif:ShutterSpeedValue   |             |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /app1/IFD/Exif/{ushort = 37377} |             |
| 2     | /xmp/exif:ShutterSpeedValue   |             |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                          |
|-------|-------------------------------|
| 1     | /app1/IFD/Exif/{ushort = 37377} |
| 2     | /xmp/exif:shutterspeedvalue   |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                            | Formato de disco |
|-------|---------------------------------|-------------|
| 1     | /IFD/Exif/{ushort = 37377}        |             |
| 2     | /ifd/xmp/exif:ShutterSpeedValue |             |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                            | Formato de disco |
|-------|---------------------------------|-------------|
| 1     | /IFD/Exif/{ushort = 37377}        |             |
| 2     | /ifd/xmp/exif:ShutterSpeedValue |             |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                            |
|-------|---------------------------------|
| 1     | /IFD/Exif/{ushort = 37377}        |
| 2     | /ifd/xmp/exif:shutterspeedvalue |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System. Photo. ShutterSpeed](../properties/props-system-photo-shutterspeed.md)
</dt> </dl>

 

 
