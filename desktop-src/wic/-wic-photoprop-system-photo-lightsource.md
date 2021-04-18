---
description: La Directiva de metadatos de la fotografía para la propiedad System. Photo. LightSource.
ms.assetid: 051a49ad-bb4c-459f-ae52-dc359a03a14a
title: Directiva de metadatos de fotografía de System. Photo. LightSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec9b3d31f01cdd2bea8d3fabbbc730a41f1fb0da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546606"
---
# <a name="systemphotolightsource-photo-metadata-policy"></a>Directiva de metadatos de fotografía de System. Photo. LightSource

La Directiva de metadatos de la fotografía para la propiedad [System. Photo. lightsource](../properties/props-system-photo-lightsource.md) .

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ lightsource

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

No

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de salida

VT \_ UI4

### <a name="input-type"></a>Tipo de entrada

UShort

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Se reconcilian los valores de los distintos esquemas.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /app1/IFD/Exif/{ushort = 37384} | ushort      |
| 2     | /XMP/Exif: LightSource         | unicode     |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /app1/IFD/Exif/{ushort = 37384} | ushort      |
| 2     | /XMP/Exif: LightSource         | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                          |
|-------|-------------------------------|
| 1     | /app1/IFD/Exif/{ushort = 37384} |
| 2     | /XMP/Exif: lightsource         |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /IFD/Exif/{ushort = 37384}  | ushort      |
| 2     | /IFD/XMP/Exif: LightSource | unicode     |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /IFD/Exif/{ushort = 37384}  | ushort      |
| 2     | /IFD/XMP/Exif: LightSource | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                      |
|-------|---------------------------|
| 1     | /IFD/Exif/{ushort = 37384}  |
| 2     | /IFD/XMP/Exif: lightsource |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System. Photo. LightSource](../properties/props-system-photo-lightsource.md)
</dt> </dl>

 

 
