---
title: Código de notificación de EN_UPDATE (Winuser. h)
description: Se envía cuando un control de edición está a punto de volver a dibujarse.
ms.assetid: 59138736-6cc9-4a3f-95f3-ada9cbf253cb
keywords:
- EN_UPDATE controles de código de notificación de Windows
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
ms.openlocfilehash: df0b045efcfb5d50cb2a85c9ae230e215263aa2e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150909"
---
# <a name="en_update-notification-code"></a>EN el \_ código de notificación de actualización

Se envía cuando un control de edición está a punto de volver a dibujarse. Este código de notificación se envía una vez que el control ha dado formato al texto, pero antes de que muestre el texto. Esto hace posible cambiar el tamaño de la ventana de control de edición, si es necesario. La ventana primaria del control de edición recibe este código de notificación a través de un mensaje de [**\_ comando de WM**](/windows/desktop/menurc/wm-command) .


```C++
EN_UPDATE

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene el identificador del control de edición. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica el código de notificación.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador del control de edición.

</dd> </dl>

## <a name="remarks"></a>Observaciones

**Rich Edit 1,0:** Para recibir los \_ códigos de notificación en la actualización, especifique [**ENM \_ Update**](rich-edit-control-event-mask-flags.md) en la máscara enviada con el mensaje [**em \_ SETEVENTMASK**](em-seteventmask.md) .

**Edición enriquecida 2,0 y versiones posteriores:** La marca de [**\_ actualización ENM**](rich-edit-control-event-mask-flags.md) se omite. \_Siempre se recibe el código de notificación en actualización. Sin embargo, cuando Microsoft Rich Edit 3,0 emula Microsoft Rich Edit 1,0, para recibir \_ los códigos de notificación de actualización debe especificar **ENM \_ Update** en la máscara enviada con el mensaje [**em \_ SETEVENTMASK**](em-seteventmask.md) .

Para obtener información sobre la compatibilidad de las versiones de edición enriquecidas con las distintas versiones del sistema, vea acerca de los [controles Rich Edit](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[EN \_ cambio](en-change.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**comando de WM \_**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

