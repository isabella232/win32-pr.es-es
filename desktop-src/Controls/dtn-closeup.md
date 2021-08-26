---
title: DTN_CLOSEUP de notificación (Commctrl.h)
description: Enviado por un control selector de fecha y hora (DTP) cuando el usuario cierra el calendario de mes desplegable.
ms.assetid: 94ace714-55cc-4c59-8b87-8d0348b15f34
keywords:
- DTN_CLOSEUP código de notificación Windows controles
topic_type:
- apiref
api_name:
- DTN_CLOSEUP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a97cd2d799d05afc638b60adc9203eaad80feb159f985df8b3813403bf5ca0d2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877725"
---
# <a name="dtn_closeup-notification-code"></a>Código de notificación DE CIERRE DE DTN \_

Enviado por un control selector de fecha y hora (DTP) cuando el usuario cierra el calendario de mes desplegable. El calendario mensual se cierra cuando el usuario elige una fecha del calendario mensual o hace clic en la flecha desplegable mientras el calendario está abierto. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
DTN_CLOSEUP

    lpNmhdr = (LPMNHDR)lParam;
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

Los controles DTP no mantienen un control de calendario de mes secundario estático. El control DTP destruye el control de calendario del mes secundario antes de enviar este código de notificación. Por lo tanto, la aplicación no debe basarse en un identificador de ventana estático para el calendario del mes secundario del control.

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

[LISTA DESPLEGABLE DE DTN \_](dtn-dropdown.md)
</dt> <dt>

[**DTM \_ GETMONTHCAL**](dtm-getmonthcal.md)
</dt> </dl>

 

 





