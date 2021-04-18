---
description: Especifica si el Remux de vídeo H. 264 debe marcar las imágenes como punto limpio para mejorar la capacidad de búsqueda. Esto tiene la posibilidad de que se produzcan daños en las búsquedas en archivos MP4 finales no conformes.
ms.assetid: BB521E13-40A4-4643-B071-76B8CBC62074
title: MFT_REMUX_MARK_I_PICTURE_AS_CLEAN_POINT atributo (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26c9fe8398507f6d7af5d0e4bf45a36a4454f220
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706126"
---
# <a name="mft_remux_mark_i_picture_as_clean_point-attribute"></a>\_REMUX \_ de MFT marca \_ I \_ imagen \_ como \_ atributo de \_ punto limpio

Especifica si el Remux de vídeo H. 264 debe marcar las imágenes como punto limpio para mejorar la capacidad de búsqueda. Esto tiene la posibilidad de que se produzcan daños en las búsquedas en archivos MP4 finales no conformes.

## <a name="data-type"></a>Tipo de datos

**Bool** almacenado como **UINT32**

## <a name="remarks"></a>Observaciones

La imagen del punto de limpieza debe comprimir las imágenes de IDR por definición.

Esto no se recomienda para la grabación o la remuxing de archivos MP4, a menos que un ejercicio de este tipo sea generar algunos archivos seudopersonalizados intermedios para la edición de vídeo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Aplicaciones \[ para UWP de Windows 8.1 Desktop apps \|\]<br/>                                        |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 R2 \|\]<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Mftransform. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Mftransform. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




