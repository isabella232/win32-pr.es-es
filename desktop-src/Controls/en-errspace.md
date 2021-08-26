---
title: EN_ERRSPACE de notificación (Winuser.h)
description: Se envía cuando un control de edición no puede asignar suficiente memoria para satisfacer una solicitud específica. La ventana primaria del control de edición recibe este código de notificación a través de un mensaje \_ WM COMMAND.
ms.assetid: 23a6eb10-a9d7-4fd5-9176-407c35e6f492
keywords:
- EN_ERRSPACE código de notificación Windows controles
topic_type:
- apiref
api_name:
- EN_ERRSPACE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 548270e6382befa8a202a94c625f8cea214025d41661305f290250d66a771cbe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047775"
---
# <a name="en_errspace-notification-code"></a>Código \_ de notificación EN ERRSPACE

Se envía cuando un control de edición no puede asignar suficiente memoria para satisfacer una solicitud específica. La ventana primaria del control de edición recibe este código de notificación a través de un [**mensaje \_ WM COMMAND.**](/windows/desktop/menurc/wm-command)


```C++
EN_ERRSPACE

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Loword [**contiene**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) el identificador del control de edición. [**HIWORD especifica**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) el código de notificación.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador del control de edición.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La ventana primaria siempre recibirá un mensaje [**WM \_ COMMAND**](/windows/desktop/menurc/wm-command) para este evento; no requiere una máscara de notificación enviada con el mensaje [**EM \_ SETEVENTMASK.**](em-seteventmask.md)

**Edición enriquecte:** Compatible con Microsoft Rich Edit 1.0 y versiones posteriores. Para obtener información sobre la compatibilidad de las versiones de edición enriquecciones con las distintas versiones del sistema, vea [Acerca de los controles rich edit](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**COMANDO \_ WM**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

