---
title: Mensaje de STM_SETIMAGE (Winuser. h)
description: Una aplicación envía un \_ mensaje STM SETIMAGE para asociar una nueva imagen con un control estático.
ms.assetid: d3e7c5d4-f621-40f6-9558-7fb699e8b489
keywords:
- STM_SETIMAGE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- STM_SETIMAGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27c4f9c216d2e987727a1e2fa9bc6de12a823d52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996061"
---
# <a name="stm_setimage-message"></a>Mensaje de STM \_ SETIMAGE

Una aplicación envía un mensaje **STM \_ SETIMAGE** para asociar una nueva imagen con un control estático.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica el tipo de imagen que se va a asociar al control estático. Este parámetro puede ser uno de los siguientes valores:



| Value                                                                                                                                                                     | Significado                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span id="IMAGE_BITMAP"></span><span id="image_bitmap"></span><dl> <dt>**mapa de bits de imagen \_**</dt> </dl>                | MyBitmap.<br/>            |
| <span id="IMAGE_CURSOR"></span><span id="image_cursor"></span><dl> <dt>**CURSOR de imagen \_**</dt> </dl>                | Cursor.<br/>            |
| <span id="IMAGE_ENHMETAFILE"></span><span id="image_enhmetafile"></span><dl> <dt>**IMAGEN \_ ENHMETAFILE**</dt> </dl> | Metarchivo mejorado.<br/> |
| <span id="IMAGE_ICON"></span><span id="image_icon"></span><dl> <dt>**icono de imagen \_**</dt> </dl>                      | Icono.<br/>              |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador de la imagen que se va a asociar al control estático.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es un identificador de la imagen asociada previamente al control estático, si existe; de lo contrario, es **null**.

## <a name="remarks"></a>Observaciones

Para asociar una imagen a un control estático, el control debe tener el estilo adecuado. En la tabla siguiente se muestra el estilo necesario para cada tipo de imagen.



| Tipo de imagen         | Estilo de control estático |
|--------------------|----------------------|
| mapa de bits de imagen \_      | \_mapa de bits SS           |
| CURSOR de imagen \_      | icono de SS \_             |
| IMAGEN \_ ENHMETAFILE | SS \_ ENHMETAFILE      |
| icono de imagen \_        | icono de SS \_             |



 

> [!IMPORTANT]
>
> En la versión 6 de los controles de Microsoft Win32, un mapa de bits que se pasa a un control estático mediante el mensaje **STM \_ SetImage** era el mismo mapa de bits devuelto por un mensaje **STM \_ SetImage** subsiguiente. El cliente es responsable de eliminar cualquier mapa de bits enviado a un control estático.
>
> Con Windows XP, si el mapa de bits pasado en el mensaje **STM \_ SETIMAGE** contiene píxeles con alfa distinto de cero, el control estático toma una copia del mapa de bits. Este mapa de bits copiado lo devuelve el siguiente mensaje de **STM \_ SETIMAGE** . El código de cliente puede realizar un seguimiento independiente de los mapas de bits que se pasan al control estático, pero si no comprueba y libera los mapas de bits devueltos de los mensajes de **STM \_ SETIMAGE** , se pierden los mapas de bits.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**STM \_ GetImage**](stm-getimage.md)
</dt> </dl>

 

 





