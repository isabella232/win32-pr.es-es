---
title: MCN_VIEWCHANGE de notificación (Commctrl.h)
description: Enviado por un control de calendario mensual cuando cambia la vista actual. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: ee35ac1d-9aeb-4d75-9cef-016487f23602
keywords:
- MCN_VIEWCHANGE código de notificación Windows controles
topic_type:
- apiref
api_name:
- MCN_VIEWCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef04fc370d67f6e6c7a4ef854d542584e170ddd05bf7c12a5135c84e97f33875
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799135"
---
# <a name="mcn_viewchange-notification-code"></a>Código de notificación \_ DE MCN VIEWCHANGE

Enviado por un control de calendario mensual cuando cambia la vista actual. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
MCN_VIEWCHANGE

    lpNMViewChange = (LPNMVIEWCHANGE) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMVIEWCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmviewchange) que contiene información sobre la vista actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





