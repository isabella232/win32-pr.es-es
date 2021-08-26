---
title: ACN_STOP de notificación (Commctrl.h)
description: Notifica a la ventana primaria de un control de animación que el clip AVI asociado ha dejado de reproducirse. Este código de notificación se envía en forma de mensaje WM \_ COMMAND.
ms.assetid: 2f21a2ec-975f-4592-8b21-956bd5311ef4
keywords:
- ACN_STOP código de notificación Windows controles
topic_type:
- apiref
api_name:
- ACN_STOP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96ba1fe51f4ceaae6e145de43a0e1104903c90b2d573c43d7aa7904f1d8f7ae1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119922095"
---
# <a name="acn_stop-notification-code"></a>Código de notificación STOP de ACN \_

Notifica a la ventana primaria de un control de animación que el clip AVI asociado ha dejado de reproducirse. Este código de notificación se envía en forma de mensaje [**WM \_ COMMAND.**](/windows/desktop/menurc/wm-command)


```C++
ACN_STOP     

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

El [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene el identificador del control de animación. [**HIWORD especifica**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) el código de notificación.

</dd> <dt>

*lParam* 
</dt> <dd>

HWND **que** especifica el identificador del control de animación.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

