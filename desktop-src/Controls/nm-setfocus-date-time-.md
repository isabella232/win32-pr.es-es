---
title: Código de notificación de NM_SETFOCUS (fecha y hora) (commctrl. h)
description: Notifica a la ventana primaria de un control de fecha y hora que el control ha recibido el foco de entrada. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 61c62fb2-bc79-404b-9958-7208d1c781fa
keywords:
- NM_SETFOCUS (fecha y hora) controles de Windows de código de notificación
topic_type:
- apiref
api_name:
- NM_SETFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba80ea119056c131f1dd94cdf1f39a84371b7052
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489959"
---
# <a name="nm_setfocus-date-time-notification-code"></a>NM \_ código de notificación de SETFOCUS (fecha y hora)

Notifica a la ventana primaria de un control de fecha y hora que el control ha recibido el foco de entrada. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
NM_SETFOCUS 

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contiene información adicional sobre esta notificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Se omite el valor devuelto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





