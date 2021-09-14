---
description: Directiva de metadatos de fotos para la propiedad System.Photo.TranscodedForSync.
ms.assetid: 1869d845-6264-425a-ab3e-e0a9f942961a
title: Directiva de metadatos de fotos System.Photo.TranscodedForSync
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5884ad469fcf7b5dffc8c4ad14f0ee5ff90cd07
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127251787"
---
# <a name="systemphototranscodedforsync-photo-metadata-policy"></a>Directiva de metadatos de fotos System.Photo.TranscodedForSync

Directiva de metadatos de fotos para [la propiedad System.Photo.TranscodedForSync.](../properties/props-system-photo-transcodedforsync.md)

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ TranscodedForSync

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

No

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de salida

VT \_ BOOL

### <a name="input-type"></a>Tipo de entrada

booleano.

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Los valores de esquemas diferentes se concilian.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Rutas de acceso de lectura



| Pedido | Path                                  | Formato de disco  |
|-------|---------------------------------------|--------------|
| 1     | /app1/ifd/{ushort=18248}              | bool \_ ushort |
| 2     | /xmp/MicrosoftPhoto:TranscodedForSync |              |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Path                                  | Formato de disco  |
|-------|---------------------------------------|--------------|
| 1     | /app1/ifd/{ushort=18248}              | bool \_ ushort |
| 2     | /xmp/MicrosoftPhoto:TranscodedForSync |              |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Path                                  |
|-------|---------------------------------------|
| 1     | /app1/ifd/{ushort=18248}              |
| 2     | /xmp/microsoftphoto:transcodedforsync |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Rutas de acceso de lectura



| Pedido | Path                                      | Formato de disco  |
|-------|-------------------------------------------|--------------|
| 1     | /ifd/{ushort=18248}                       | bool \_ ushort |
| 2     | /ifd/xmp/MicrosoftPhoto:TranscodedForSync |              |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Path                                      | Formato de disco  |
|-------|-------------------------------------------|--------------|
| 1     | /ifd/{ushort=18248}                       | bool \_ ushort |
| 2     | /ifd/xmp/MicrosoftPhoto:TranscodedForSync |              |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Path                                      |
|-------|-------------------------------------------|
| 1     | /ifd/{ushort=18248}                       |
| 2     | /ifd/xmp/microsoftphoto:transcodedforsync |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System.Photo.TranscodedForSync](../properties/props-system-photo-transcodedforsync.md)
</dt> </dl>

 

 
