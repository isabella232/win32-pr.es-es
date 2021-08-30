---
title: EN_MAXTEXT de notificación (Winuser.h)
description: Se envía cuando la inserción de texto actual ha superado el número especificado de caracteres para el control de edición.
ms.assetid: b03835d6-d06f-415a-97f2-d2b62b17e175
keywords:
- EN_MAXTEXT código de notificación Windows controles
topic_type:
- apiref
api_name:
- EN_MAXTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8af5935c55460373a0f81007caf037a021fb627d71afd0736af97cd040b23d51
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047625"
---
# <a name="en_maxtext-notification-code"></a>Código de notificación EN \_ MAXTEXT

Se envía cuando la inserción de texto actual ha superado el número especificado de caracteres para el control de edición. La inserción de texto se ha truncado.

Este código de notificación también se envía cuando un control de edición no tiene el estilo [**\_ ES AUTOHSCROLL**](edit-control-styles.md) y el número de caracteres que se va a insertar superaría el ancho del control de edición.

Este código de notificación también se envía cuando un control de edición no tiene el estilo [**ES \_ AUTOVSCROLL**](edit-control-styles.md) y el número total de líneas resultantes de una inserción de texto superaría el alto del control de edición.

La ventana primaria del control de edición recibe este código de notificación a través de un [**mensaje \_ WM COMMAND.**](/windows/desktop/menurc/wm-command)


```C++
EN_MAXTEXT

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

## <a name="remarks"></a>Comentarios

La ventana primaria siempre recibe un [**mensaje \_ WM COMMAND**](/windows/desktop/menurc/wm-command) para este evento, no requiere una máscara de notificación enviada con EM [**\_ SETEVENTMASK**](em-seteventmask.md).

**Edición enriquecte:** Compatible con Microsoft Rich Edit 1.0 y versiones posteriores. Para obtener información sobre la compatibilidad de las versiones de edición enriquecciones con las distintas versiones del sistema, vea [About Rich Edit Controls](about-rich-edit-controls.md).

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

 

