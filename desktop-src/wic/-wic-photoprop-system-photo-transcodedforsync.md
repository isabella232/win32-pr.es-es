---
description: La Directiva de metadatos de fotos para la propiedad System. Photo. TranscodedForSync.
ms.assetid: 1869d845-6264-425a-ab3e-e0a9f942961a
title: Directiva de metadatos de la foto de System. Photo. TranscodedForSync
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5884ad469fcf7b5dffc8c4ad14f0ee5ff90cd07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911945"
---
# <a name="systemphototranscodedforsync-photo-metadata-policy"></a>Directiva de metadatos de la foto de System. Photo. TranscodedForSync

La Directiva de metadatos de fotos para la propiedad [System. Photo. TranscodedForSync](../properties/props-system-photo-transcodedforsync.md) .

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ TranscodedForSync

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

No

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de salida

VT \_ bool

### <a name="input-type"></a>Tipo de entrada

booleano.

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Se reconcilian los valores de los distintos esquemas.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                                  | Formato de disco  |
|-------|---------------------------------------|--------------|
| 1     | /app1/IFD/{ushort = 18248}              | bool \_ ushort |
| 2     | /xmp/MicrosoftPhoto:TranscodedForSync |              |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                                  | Formato de disco  |
|-------|---------------------------------------|--------------|
| 1     | /app1/IFD/{ushort = 18248}              | bool \_ ushort |
| 2     | /xmp/MicrosoftPhoto:TranscodedForSync |              |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                                  |
|-------|---------------------------------------|
| 1     | /app1/IFD/{ushort = 18248}              |
| 2     | /xmp/microsoftphoto:transcodedforsync |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                                      | Formato de disco  |
|-------|-------------------------------------------|--------------|
| 1     | /IFD/{ushort = 18248}                       | bool \_ ushort |
| 2     | /ifd/xmp/MicrosoftPhoto:TranscodedForSync |              |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                                      | Formato de disco  |
|-------|-------------------------------------------|--------------|
| 1     | /IFD/{ushort = 18248}                       | bool \_ ushort |
| 2     | /ifd/xmp/MicrosoftPhoto:TranscodedForSync |              |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                                      |
|-------|-------------------------------------------|
| 1     | /IFD/{ushort = 18248}                       |
| 2     | /ifd/xmp/microsoftphoto:transcodedforsync |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System. Photo. TranscodedForSync](../properties/props-system-photo-transcodedforsync.md)
</dt> </dl>

 

 
