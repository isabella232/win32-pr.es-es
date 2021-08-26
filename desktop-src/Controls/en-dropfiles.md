---
title: EN_DROPFILES de notificación (Richedit.h)
description: Notifica a una ventana primaria de control de edición enriqueciendo que el usuario está intentando colocar archivos en el control. Un control de edición enriquecido envía este código de notificación en forma de mensaje \_ WM NOTIFY cuando recibe el mensaje \_ DROPFILES de WM.
ms.assetid: fcae0ff8-ce37-4c71-b14c-cbd6429b4ab3
keywords:
- EN_DROPFILES código de notificación Windows controles
topic_type:
- apiref
api_name:
- EN_DROPFILES
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8813d3d62883ab607bb898f4aa34a664cbab47b2c8214fbd83fc8cc7913e26ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047785"
---
# <a name="en_dropfiles-notification-code"></a>Código de notificación EN \_ DROPFILES

Notifica a una ventana primaria de control de edición enriqueciendo que el usuario está intentando colocar archivos en el control. Un control de edición enriquecido envía este código de notificación en forma de mensaje [**\_ WM NOTIFY**](wm-notify.md) cuando recibe el mensaje [**\_ DROPFILES de WM.**](/windows/desktop/shell/wm-dropfiles)


```C++
EN_DROPFILES

      penDropFiles = (ENDROPFILES *) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Estructura [**ENDROPFILES**](/windows/desktop/api/Richedit/ns-richedit-endropfiles) que recibe información de archivos eliminados.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero para permitir la operación de colocación.

Devuelve cero para omitir la operación de colocación.

## <a name="remarks"></a>Comentarios

Para que un control de edición enriquecida reciba mensajes [**\_ DROPFILES**](/windows/desktop/shell/wm-dropfiles) de WM, la ventana primaria debe registrar el control como destino de colocación mediante la [**función DragAcceptFiles.**](/windows/desktop/api/shellapi/nf-shellapi-dragacceptfiles) El control no se registra a sí mismo.

Para recibir códigos de notificación EN \_ DROPFILES, especifique [**ENM \_ DROPFILES**](rich-edit-control-event-mask-flags.md) en la máscara enviada con el [**mensaje EM \_ SETEVENTMASK.**](em-seteventmask.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**ENDROPFILES**](/windows/desktop/api/Richedit/ns-richedit-endropfiles)
</dt> </dl>

 

