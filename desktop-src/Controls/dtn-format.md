---
title: DTN_FORMAT de notificación (Commctrl.h)
description: Enviado por un control selector de fecha y hora (DTP) para solicitar que el texto se muestre en un campo de devolución de llamada. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: ce0ee230-638e-425f-9f34-c379342cea93
keywords:
- DTN_FORMAT código de notificación Windows controles
topic_type:
- apiref
api_name:
- DTN_FORMAT
- DTN_FORMATA
- DTN_FORMATW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75fb4279f6ec6b95ded673083a024d32785dd5156588852663e6c307f8351dc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916275"
---
# <a name="dtn_format-notification-code"></a>Código de notificación \_ DE DTN FORMAT

Enviado por un control selector de fecha y hora (DTP) para solicitar que el texto se muestre en un campo de devolución de llamada. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
DTN_FORMAT

    lpNMFormat = (LPNMDATETIMEFORMAT) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMDATETIMEFORMAT**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformata) que contiene información sobre esta instancia del código de notificación. La estructura contiene la subcadena que define el campo de devolución de llamada y recibe la cadena con formato que mostrará el control.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El propietario del control debe devolver cero.

## <a name="remarks"></a>Comentarios

El control de este código de notificación permite al propietario del control proporcionar una cadena personalizada que el control mostrará. (Para obtener información adicional sobre los campos de devolución de llamada, vea [Campos de devolución de llamada).](date-and-time-picker-controls.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **DTN \_ FORMATW** (Unicode) y **DTN \_ FORMATA** (ANSI)<br/>                     |



 

 





