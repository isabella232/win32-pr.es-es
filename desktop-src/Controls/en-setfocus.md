---
title: EN_SETFOCUS de notificación (Winuser.h)
description: Se envía cuando un control de edición recibe el foco del teclado. La ventana primaria del control de edición recibe este código de notificación a través de un mensaje \_ WM COMMAND.
ms.assetid: 482d2afa-4e21-4f3f-bdf4-6966b34cc3c4
keywords:
- EN_SETFOCUS código de notificación Windows controles
topic_type:
- apiref
api_name:
- EN_SETFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5cb96482f0e42669658dde3a39637e3c2311619
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062018"
---
# <a name="en_setfocus-notification-code"></a>Código de notificación DE EN \_ SETFOCUS

Se envía cuando un control de edición recibe el foco del teclado. La ventana primaria del control de edición recibe este código de notificación a través de un [**mensaje \_ WM COMMAND.**](/windows/desktop/menurc/wm-command)


```C++
EN_SETFOCUS

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

La ventana primaria siempre recibe un [**mensaje \_ WM COMMAND**](/windows/desktop/menurc/wm-command) para este evento, no requiere una máscara de notificación enviada con EM [**\_ SETEVENTMASK**](em-seteventmask.md).

**Edición enriquecte:** Compatible con Microsoft Rich Edit 1.0 y versiones posteriores. Para obtener información sobre la compatibilidad de las versiones de edición enriquecciones con las distintas versiones del sistema, vea [About Rich Edit Controls](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Referencia**
</dt> <dt>

[EN \_ KILLFOCUS](en-killfocus.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**COMANDO \_ WM**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

