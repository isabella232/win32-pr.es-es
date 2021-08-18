---
title: ACN_START de notificación (Commctrl.h)
description: Notifica a la ventana primaria de un control de animación que el clip AVI asociado ha empezado a reproducirse. Este código de notificación se envía en forma de mensaje \_ WM COMMAND.
ms.assetid: b4d12225-36f7-4f87-b58a-dac091d14e4c
keywords:
- ACN_START de notificación Windows controles
topic_type:
- apiref
api_name:
- ACN_START
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ccfb5a1fc1f6b258cfe8363e99f38894ed7e601401d4f725431992a31f86376
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119922165"
---
# <a name="acn_start-notification-code"></a>Código de notificación \_ DE ACN START

Notifica a la ventana primaria de un control de animación que el clip AVI asociado ha empezado a reproducirse. Este código de notificación se envía en forma de mensaje [**\_ WM COMMAND.**](/windows/desktop/menurc/wm-command)


```C++
ACN_START 

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

LOWORD [**contiene el**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) identificador del control de animación. [**HIWORD especifica**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) el código de notificación.

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



 

