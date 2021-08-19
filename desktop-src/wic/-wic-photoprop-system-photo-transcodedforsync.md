---
description: Directiva de metadatos de fotos para la propiedad System.Photo.TranscodedForSync.
ms.assetid: 1869d845-6264-425a-ab3e-e0a9f942961a
title: Directiva de metadatos de fotos System.Photo.TranscodedForSync
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34e78086284e1ca13b01c5e7cd188b761afe7eeba8acb5f2bca103234f80955b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964764"
---
# <a name="systemphototranscodedforsync-photo-metadata-policy"></a>Directiva de metadatos de fotos System.Photo.TranscodedForSync

Directiva de metadatos de fotos para [la propiedad System.Photo.TranscodedForSync.](../properties/props-system-photo-transcodedforsync.md)

### <a name="pkey"></a>Pkey

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

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta de acceso                                  | Formato de disco  |
|-------|---------------------------------------|--------------|
| 1     | /app1/ifd/{ushort=18248}              | bool \_ ushort |
| 2     | /xmp/MicrosoftPhoto:TranscodedForSync |              |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Ruta de acceso                                  | Formato de disco  |
|-------|---------------------------------------|--------------|
| 1     | /app1/ifd/{ushort=18248}              | bool \_ ushort |
| 2     | /xmp/MicrosoftPhoto:TranscodedForSync |              |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                                  |
|-------|---------------------------------------|
| 1     | /app1/ifd/{ushort=18248}              |
| 2     | /xmp/microsoftphoto:transcodedforsync |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta de acceso                                      | Formato de disco  |
|-------|-------------------------------------------|--------------|
| 1     | /ifd/{ushort=18248}                       | bool \_ ushort |
| 2     | /ifd/xmp/MicrosoftPhoto:TranscodedForSync |              |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Ruta de acceso                                      | Formato de disco  |
|-------|-------------------------------------------|--------------|
| 1     | /ifd/{ushort=18248}                       | bool \_ ushort |
| 2     | /ifd/xmp/MicrosoftPhoto:TranscodedForSync |              |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                                      |
|-------|-------------------------------------------|
| 1     | /ifd/{ushort=18248}                       |
| 2     | /ifd/xmp/microsoftphoto:transcodedforsync |



 

## <a name="remarks"></a>Comentarios

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System.Photo.TranscodedForSync](../properties/props-system-photo-transcodedforsync.md)
</dt> </dl>

 

 
