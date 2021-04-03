---
title: Código de notificación de DTN_DROPDOWN (commctrl. h)
description: Se envía mediante un control de selector de fecha y hora (DTP) cuando el usuario activa el calendario del mes desplegable. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 6f20fa87-2223-4876-b77d-2c684685bf10
keywords:
- DTN_DROPDOWN controles de código de notificación de Windows
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
ms.openlocfilehash: 101a25a8e2da09b9f4065a54fcff9896690adbb8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905426"
---
# <a name="dtn_dropdown-notification-code"></a>\_Código de notificación de desplegable DTN

Se envía mediante un control de selector de fecha y hora (DTP) cuando el usuario activa el calendario del mes desplegable. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
DTN_DROPDOWN

    lpNmhdr = (LPNMHDR)lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contiene información sobre la notificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se utiliza el valor devuelto para esta notificación.

## <a name="remarks"></a>Observaciones

Una tarea que el controlador de notificación puede tener que realizar es personalizar el control de calendario mensual de la lista desplegable. Por ejemplo, si no desea "ir a hoy", debe establecer el estilo [**MCS \_ noactual**](month-calendar-control-styles.md)  del control. Para recuperar un identificador del control de calendario mensual, envíe el control de DTP a un mensaje [**DTM \_ GETMONTHCAL**](dtm-getmonthcal.md) . Después, puede usar este identificador y [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) para establecer el estilo de calendario mensual deseado.

Los controles de DTP no mantienen un control de calendario mensual secundario estático. El control de DTP crea un nuevo control de calendario mensual antes de enviar este código de notificación. Además, el control de DTP destruye el control secundario cuando no está activo (visible). Por lo tanto, la aplicación no debe basarse en un identificador de ventana estático para el calendario mensual del control.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[DTN \_ primer plano](dtn-closeup.md)
</dt> <dt>

[**DTM \_ GETMONTHCAL**](dtm-getmonthcal.md)
</dt> </dl>

 

