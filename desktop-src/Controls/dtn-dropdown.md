---
title: DTN_DROPDOWN de notificación (Commctrl.h)
description: Enviado por un control de selector de fecha y hora (DTP) cuando el usuario activa el calendario de mes desplegable. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 6f20fa87-2223-4876-b77d-2c684685bf10
keywords:
- DTN_DROPDOWN código de notificación Windows controles
topic_type:
- apiref
api_name:
- DTN_DROPDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba6c583de68b8a92c8d93990bce84787fa061ec5422ea2c6b32a6a3942b766ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877685"
---
# <a name="dtn_dropdown-notification-code"></a>Código de notificación DE LISTA DESPLEGABLE de DTN \_

Enviado por un control de selector de fecha y hora (DTP) cuando el usuario activa el calendario de mes desplegable. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
DTN_DROPDOWN

    lpNmhdr = (LPNMHDR)lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contiene información sobre la notificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se usa el valor devuelto para esta notificación.

## <a name="remarks"></a>Comentarios

Una tarea que el controlador de notificaciones puede tener que realizar es personalizar el control de calendario mensual desplegable. Por ejemplo, si no quiere "Ir a hoy", debe establecer el estilo [**\_ NOTODAY**](month-calendar-control-styles.md)  de MCS del control. Para recuperar un identificador al control month-calendar, envíe al control DTP un mensaje [**\_ GETMONTHCAL de DTM.**](dtm-getmonthcal.md) A continuación, puede usar este identificador [**y SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) para establecer el estilo de calendario mensual deseado.

Los controles DTP no mantienen un control de calendario de mes secundario estático. El control DTP crea un nuevo control de calendario mensual antes de enviar este código de notificación. Además, el control DTP destruye el control secundario cuando no está activo (visible). Por lo tanto, la aplicación no debe basarse en un identificador de ventana estático para el calendario del mes secundario del control.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[CIERRE \_ DE DTN](dtn-closeup.md)
</dt> <dt>

[**DTM \_ GETMONTHCAL**](dtm-getmonthcal.md)
</dt> </dl>

 

