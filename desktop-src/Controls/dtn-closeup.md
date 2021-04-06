---
title: Código de notificación de DTN_CLOSEUP (commctrl. h)
description: Se envía mediante un control de selector de fecha y hora (DTP) cuando el usuario cierra el calendario del mes desplegable.
ms.assetid: 94ace714-55cc-4c59-8b87-8d0348b15f34
keywords:
- DTN_CLOSEUP controles de código de notificación de Windows
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
ms.openlocfilehash: 9cfcfb23215aeffe15bec576075fd4d930790e47
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803272"
---
# <a name="dtn_closeup-notification-code"></a>Código de notificación de primer plano de DTN \_

Se envía mediante un control de selector de fecha y hora (DTP) cuando el usuario cierra el calendario del mes desplegable. El calendario mensual se cierra cuando el usuario elige una fecha en el calendario mensual o hace clic en la flecha desplegable mientras el calendario está abierto. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
DTN_CLOSEUP

    lpNmhdr = (LPMNHDR)lParam;
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

Los controles de DTP no mantienen un control de calendario mensual secundario estático. El control de DTP destruye el control de calendario mensual secundario antes de enviar este código de notificación. Por lo tanto, la aplicación no debe basarse en un identificador de ventana estático para el calendario mensual del control.

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

[\_lista desplegable DTN](dtn-dropdown.md)
</dt> <dt>

[**DTM \_ GETMONTHCAL**](dtm-getmonthcal.md)
</dt> </dl>

 

 





