---
title: Código de notificación de DTN_DATETIMECHANGE (commctrl. h)
description: Se envía mediante un control de selector de fecha y hora (DTP) cada vez que se produce un cambio. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 65cdd8fb-1f07-4447-b503-d40fdfa37202
keywords:
- DTN_DATETIMECHANGE controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- DTN_DATETIMECHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a40072a54732a0a3575e3153ddb901ca1df291b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905427"
---
# <a name="dtn_datetimechange-notification-code"></a>Código de notificación de DATETIMECHANGE de DTN \_

Se envía mediante un control de selector de fecha y hora (DTP) cada vez que se produce un cambio. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
DTN_DATETIMECHANGE

    lpChange = (LPNMDATETIMECHANGE) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMDATETIMECHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimechange) que contiene información sobre el cambio que tuvo lugar en el control.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El propietario del control debe devolver cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





