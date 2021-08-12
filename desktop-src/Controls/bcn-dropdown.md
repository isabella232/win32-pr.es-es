---
title: BCN_DROPDOWN de notificación (Winuser.h)
description: Se envía cuando el usuario hace clic en una flecha desplegable de un botón. La ventana primaria del control recibe este código de notificación en forma de mensaje WM \_ NOTIFY.
ms.assetid: 61503b8d-193e-4855-b9eb-35c0dc636c02
keywords:
- BCN_DROPDOWN código de notificación Windows controles
topic_type:
- apiref
api_name:
- BCN_DROPDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fbacf22cdabbac7c5d2932c604fab634dbc185207acda8cee311d434478e5ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118674981"
---
# <a name="bcn_dropdown-notification-code"></a>Código de notificación \_ DE BCN DROPDOWN

Se envía cuando el usuario hace clic en una flecha desplegable de un botón. La ventana primaria del control recibe este código de notificación en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
BCN_DROPDOWN
        
    pnmdropdown = (NMBCDROPDOWN*) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMBCDROPDOWN.**](/windows/win32/api/commctrl/ns-commctrl-nmbcdropdown) El **miembro rcButton** se establece para describir el área desplegable.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El receptor de notificaciones convierte **LPARAM** para recuperar la estructura [**NMBCDROPDOWN.**](/windows/win32/api/commctrl/ns-commctrl-nmbcdropdown) **WPARAM** contiene el identificador del control que envía este mensaje. El control de botón debe tener un estilo de botón desplegable.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



 

 





