---
title: EN_UPDATE de notificación (Winuser.h)
description: Se envía cuando un control de edición está a punto de volver a dibujarse.
ms.assetid: 59138736-6cc9-4a3f-95f3-ada9cbf253cb
keywords:
- EN_UPDATE código de notificación Windows controles
topic_type:
- apiref
api_name:
- EN_UPDATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c126122336fd878dda633620c395cb86c112de1f5dc89e8e25d2c4e08bd93ebd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119436435"
---
# <a name="en_update-notification-code"></a>Código de notificación de EN \_ UPDATE

Se envía cuando un control de edición está a punto de volver a dibujarse. Este código de notificación se envía después de que el control haya dado formato al texto, pero antes de mostrar el texto. Esto permite cambiar el tamaño de la ventana de control de edición, si es necesario. La ventana primaria del control de edición recibe este código de notificación a través de un [**mensaje \_ WM COMMAND.**](/windows/desktop/menurc/wm-command)


```C++
EN_UPDATE

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

LOWORD [**contiene**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) el identificador del control de edición. [**HIWORD especifica**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) el código de notificación.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador del control de edición.

</dd> </dl>

## <a name="remarks"></a>Observaciones

**Rich Edit 1.0:** Para recibir los \_ códigos de notificación de EN UPDATE, especifique [**ENM \_ UPDATE**](rich-edit-control-event-mask-flags.md) en la máscara enviada con el [**mensaje EM \_ SETEVENTMASK.**](em-seteventmask.md)

**Rich Edit 2.0 y versiones posteriores:** Se omite la marca UPDATE de [**ENM. \_**](rich-edit-control-event-mask-flags.md) Siempre se \_ recibe el código de notificación DE UPDATE. Sin embargo, cuando Microsoft Rich Edit 3.0 emula Microsoft Rich Edit 1.0, para recibir códigos de notificación de EN UPDATE, debe especificar ENM UPDATE en la máscara enviada con el mensaje \_ [**EM \_ SETEVENTMASK.**](em-seteventmask.md) **\_**

Para obtener información sobre la compatibilidad de las versiones de edición enriquecciones con las distintas versiones del sistema, vea [About Rich Edit Controls](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[CAMBIO \_ EN](en-change.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**COMANDO \_ WM**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

