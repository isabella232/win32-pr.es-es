---
title: STM_SETIMAGE mensaje (Winuser.h)
description: Una aplicación envía un mensaje SETIMAGE de STM \_ para asociar una nueva imagen a un control estático.
ms.assetid: d3e7c5d4-f621-40f6-9558-7fb699e8b489
keywords:
- STM_SETIMAGE controles de Windows mensaje
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
ms.openlocfilehash: d48cc8aeb5e28ac67a6bbe25636be1a2f6f9b89f225568be02e517e1ad04dc55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078459"
---
# <a name="stm_setimage-message"></a>Mensaje \_ setimage de STM

Una aplicación envía un **mensaje \_ SETIMAGE de STM** para asociar una nueva imagen a un control estático.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica el tipo de imagen que se asociará al control estático. Este parámetro puede ser uno de los siguientes valores:



| Valor                                                                                                                                                                     | Significado                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span id="IMAGE_BITMAP"></span><span id="image_bitmap"></span><dl> <dt>**IMAGEN DE \_ MAPA DE BITS**</dt> </dl>                | Bits.<br/>            |
| <span id="IMAGE_CURSOR"></span><span id="image_cursor"></span><dl> <dt>**IMAGE \_ CURSOR**</dt> </dl>                | Cursor.<br/>            |
| <span id="IMAGE_ENHMETAFILE"></span><span id="image_enhmetafile"></span><dl> <dt>**IMAGE \_ ENHMETAFILE**</dt> </dl> | Metarchivo mejorado.<br/> |
| <span id="IMAGE_ICON"></span><span id="image_icon"></span><dl> <dt>**ICONO DE \_ IMAGEN**</dt> </dl>                      | Icono.<br/>              |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador de la imagen que se asociará al control estático.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es un identificador de la imagen asociada previamente al control estático, si existe; de lo contrario, es **NULL.**

## <a name="remarks"></a>Comentarios

Para asociar una imagen a un control estático, el control debe tener el estilo adecuado. En la tabla siguiente se muestra el estilo necesario para cada tipo de imagen.



| Tipo de imagen         | Estilo de control estático |
|--------------------|----------------------|
| IMAGEN DE \_ MAPA DE BITS      | MAPA DE BITS DE SS \_           |
| IMAGE \_ CURSOR      | ICONO \_ DE SS             |
| IMAGE \_ ENHMETAFILE | SS \_ ENHMETAFILE      |
| ICONO DE \_ IMAGEN        | ICONO \_ DE SS             |



 

> [!IMPORTANT]
>
> En la versión 6 de los controles Win32 de Microsoft, un mapa de bits pasado a un control estático mediante el mensaje **\_ SETIMAGE de STM** era el mismo mapa de bits devuelto por un mensaje **\_ SETIMAGE de STM** posterior. El cliente es responsable de eliminar cualquier mapa de bits enviado a un control estático.
>
> Con Windows XP, si el mapa de bits pasado en el mensaje **\_ SETIMAGE de STM** contiene píxeles con alfa distinto de cero, el control estático toma una copia del mapa de bits. El siguiente mensaje **\_ SETIMAGE** de STM devuelve este mapa de bits copiado. El código de cliente puede realizar un seguimiento independiente de los mapas de bits pasados al control estático, pero si no comprueba y libera los mapas de bits devueltos por los mensajes **\_ SETIMAGE de STM,** los mapas de bits se pierden.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**STM \_ GETIMAGE**](stm-getimage.md)
</dt> </dl>

 

 





