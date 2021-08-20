---
description: Especifica si el archivo MFT de remux de vídeo H.264 debe marcar I pictures como punto limpio para mejorar la capacidad de búsqueda. Esto tiene la posibilidad de daños en las búsquedas en archivos MP4 finales no conformes.
ms.assetid: BB521E13-40A4-4643-B071-76B8CBC62074
title: MFT_REMUX_MARK_I_PICTURE_AS_CLEAN_POINT atributo (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bf4156cfc25620e40e0c39df20922b75787db0b30c026635f36322fa2e8b5d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117688786"
---
# <a name="mft_remux_mark_i_picture_as_clean_point-attribute"></a>Atributo MFT \_ REMUX \_ MARK I PICTURE AS CLEAN \_ \_ \_ \_ \_ POINT

Especifica si el archivo MFT de remux de vídeo H.264 debe marcar I pictures como punto limpio para mejorar la capacidad de búsqueda. Esto tiene la posibilidad de daños en las búsquedas en archivos MP4 finales no conformes.

## <a name="data-type"></a>Tipo de datos

**Bool almacenado** como **UINT32**

## <a name="remarks"></a>Comentarios

La imagen de punto limpio debe ser imágenes de IDR comprimidas por definición.

Esto no se recomienda para grabar o volver a usar archivos MP4, a menos que este ejercicio sea generar algunos archivos pseudo MP4 intermedios para la edición de vídeo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Server 2012 Aplicaciones de \[ escritorio R2 \| aplicaciones para UWP\]<br/>                             |
| Header<br/>                   | <dl> <dt>Mftransform.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Mftransform.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




