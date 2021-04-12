---
title: Código de notificación de EN_MAXTEXT (Winuser. h)
description: Se envía cuando la inserción de texto actual ha superado el número de caracteres especificado para el control de edición.
ms.assetid: b03835d6-d06f-415a-97f2-d2b62b17e175
keywords:
- EN_MAXTEXT controles de código de notificación de Windows
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
ms.openlocfilehash: 454b48fb232f2225696efacc44d54660d3a83185
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535044"
---
# <a name="en_maxtext-notification-code"></a>\_Código de notificación en MAXTEXT

Se envía cuando la inserción de texto actual ha superado el número de caracteres especificado para el control de edición. La inserción de texto se ha truncado.

Este código de notificación también se envía cuando un control de edición no tiene el estilo [**es \_ AUTOHSCROLL**](edit-control-styles.md) y el número de caracteres que se va a insertar superará el ancho del control de edición.

Este código de notificación también se envía cuando un control de edición no tiene el estilo [**es \_ AUTOVSCROLL**](edit-control-styles.md) y el número total de líneas resultante de una inserción de texto superaría el alto del control de edición.

La ventana primaria del control de edición recibe este código de notificación a través de un mensaje de [**\_ comando de WM**](/windows/desktop/menurc/wm-command) .


```C++
EN_MAXTEXT

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

La ventana primaria siempre recibe un mensaje de [**\_ comando de WM**](/windows/desktop/menurc/wm-command) para este evento, pero no requiere que se envíe una máscara de notificación con [**em \_**](em-seteventmask.md).

**Edición enriquecida:** Compatible con Microsoft Rich Edit 1,0 y versiones posteriores. Para obtener información sobre la compatibilidad de las versiones de edición enriquecidas con las distintas versiones del sistema, vea acerca de los [controles Rich Edit](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**comando de WM \_**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

