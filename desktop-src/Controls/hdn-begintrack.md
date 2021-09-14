---
title: HDN_BEGINTRACK de notificación (Commctrl.h)
description: Notifica a la ventana primaria de un control de encabezado que el usuario ha empezado a arrastrar un divisor en el control (es decir, el usuario ha presionado el botón primario del mouse mientras el cursor del mouse está en un divisor en el control de encabezado).
ms.assetid: 363b14bc-2b7e-4c37-9caf-7671fcc3cfa5
keywords:
- HDN_BEGINTRACK código de notificación Windows controles
topic_type:
- apiref
api_name:
- HDN_BEGINTRACK
- HDN_BEGINTRACKA
- HDN_BEGINTRACKW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6da4ae2c360b13077a612b92ab19a739a58a07e3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061956"
---
# <a name="hdn_begintrack-notification-code"></a>Código de notificación BEGINTRACK de HDN \_

Notifica a la ventana primaria de un control de encabezado que el usuario ha empezado a arrastrar un divisor en el control (es decir, el usuario ha presionado el botón primario del mouse mientras el cursor del mouse está en un divisor en el control de encabezado). Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
HDN_BEGINTRACK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) que contiene información sobre el control de encabezado y el elemento cuyo divisor se va a arrastrar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **FALSE** para permitir el seguimiento del divisor o **TRUE** para evitar el seguimiento.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **HDN \_ BEGINTRACKW** (Unicode) y **HDN \_ BEGINTRACKA** (ANSI)<br/>             |



 

 





