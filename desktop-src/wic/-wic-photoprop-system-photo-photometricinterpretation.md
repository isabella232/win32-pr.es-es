---
description: La Directiva de metadatos de fotos para la propiedad System. Photo. PhotometricInterpretation.
ms.assetid: ff36b2c3-8763-4640-a049-b5880fd26929
title: Directiva de metadatos de la foto de System. Photo. PhotometricInterpretation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35b371ce9257d526f941f3fdb33949e8788a7112
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678224"
---
# <a name="systemphotophotometricinterpretation-photo-metadata-policy"></a>Directiva de metadatos de la foto de System. Photo. PhotometricInterpretation

La Directiva de metadatos de fotos para la propiedad [System. Photo. PhotometricInterpretation](../properties/props-system-photo-photometricinterpretation.md) .

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ PhotometricInterpretation

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

Sí

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de salida

VT \_ UI2

### <a name="input-type"></a>Tipo de entrada

UShort

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Se reconcilian los valores de los distintos esquemas.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                                | Formato de disco |
|-------|-------------------------------------|-------------|
| 1     | /app1/IFD/{ushort = 262}              | ushort      |
| 2     | /xmp/tiff:PhotometricInterpretation | unicode     |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                                | Formato de disco |
|-------|-------------------------------------|-------------|
| 1     | /app1/IFD/{ushort = 262}              | ushort      |
| 2     | /xmp/tiff:PhotometricInterpretation | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                                |
|-------|-------------------------------------|
| 1     | /app1/IFD/{ushort = 262}              |
| 2     | /xmp/tiff:photometricinterpretation |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                                    | Formato de disco |
|-------|-----------------------------------------|-------------|
| 1     | /IFD/{ushort = 262}                       | ushort      |
| 2     | /ifd/xmp/tiff:PhotometricInterpretation | unicode     |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                                    | Formato de disco |
|-------|-----------------------------------------|-------------|
| 1     | /IFD/{ushort = 262}                       | ushort      |
| 2     | /ifd/xmp/tiff:PhotometricInterpretation | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                                    |
|-------|-----------------------------------------|
| 1     | /IFD/{ushort = 262}                       |
| 2     | /ifd/xmp/tiff:photometricinterpretation |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System. Photo. PhotometricInterpretation](../properties/props-system-photo-photometricinterpretation.md)
</dt> </dl>

 

 
