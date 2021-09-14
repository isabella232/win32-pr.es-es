---
title: HDN_ENDTRACK de notificación (Commctrl.h)
description: Notifica a la ventana primaria de un control de encabezado que el usuario ha terminado de arrastrar un divisor. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: d9b25871-7bd6-439c-91b8-e8249d9be67d
keywords:
- HDN_ENDTRACK código de notificación Windows controles
topic_type:
- apiref
api_name:
- HDN_ENDTRACK
- HDN_ENDTRACKA
- HDN_ENDTRACKW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42ab7625690a2de0414f1da391f26f919c1c2617
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061951"
---
# <a name="hdn_endtrack-notification-code"></a>Código de notificación ENDTRACK de HDN \_

Notifica a la ventana primaria de un control de encabezado que el usuario ha terminado de arrastrar un divisor. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
HDN_ENDTRACK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) que contiene información sobre el control de encabezado y el elemento cuyo divisor se arrastró.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **HDN \_ ENDTRACKW** (Unicode) y **HDN \_ ENDTRACKA** (ANSI)<br/>                 |



 

 





