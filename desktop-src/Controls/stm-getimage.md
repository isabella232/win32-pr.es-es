---
title: Mensaje de STM_GETIMAGE (Winuser. h)
description: Una aplicación envía un \_ mensaje de STM GetImage para recuperar un identificador de la imagen (icono o mapa de bits) asociado a un control estático.
ms.assetid: eb5fe67a-09be-4c13-89c6-0e2f23e8c081
keywords:
- STM_GETIMAGE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- STM_GETIMAGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77fe0c3d00a2a957530160a5ce5a21b8a1cf84e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078925"
---
# <a name="stm_getimage-message"></a>Mensaje de STM \_ GetImage

Una aplicación envía un mensaje de **STM \_ GetImage** para recuperar un identificador de la imagen (icono o mapa de bits) asociado a un control estático.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica el tipo de imagen que se va a recuperar. Este parámetro puede ser uno de los siguientes valores:



| Value                                                                                                                                                                     | Significado                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span id="IMAGE_BITMAP"></span><span id="image_bitmap"></span><dl> <dt>**mapa de bits de imagen \_**</dt> </dl>                | MyBitmap.<br/>            |
| <span id="IMAGE_CURSOR"></span><span id="image_cursor"></span><dl> <dt>**CURSOR de imagen \_**</dt> </dl>                | Cursor.<br/>            |
| <span id="IMAGE_ENHMETAFILE"></span><span id="image_enhmetafile"></span><dl> <dt>**IMAGEN \_ ENHMETAFILE**</dt> </dl> | Metarchivo mejorado.<br/> |
| <span id="IMAGE_ICON"></span><span id="image_icon"></span><dl> <dt>**icono de imagen \_**</dt> </dl>                      | Icono.<br/>              |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es un identificador de la imagen, si existe; de lo contrario, es **null**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**STM \_ SETIMAGE**](stm-setimage.md)
</dt> </dl>

 

 





