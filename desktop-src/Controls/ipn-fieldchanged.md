---
title: IPN_FIELDCHANGED de notificación (Commctrl.h)
description: Se envía cuando el usuario cambia un campo del control o se mueve de un campo a otro. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: f9ca6435-1715-458e-8d0e-475920ed75bd
keywords:
- IPN_FIELDCHANGED código de notificación Windows controles
topic_type:
- apiref
api_name:
- IPN_FIELDCHANGED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 467cf7f14f3ff8d62f85d973e9a9d11c4dc6d20488ad5b7e30b4c0787b4b1a6c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085555"
---
# <a name="ipn_fieldchanged-notification-code"></a>Código de notificación FIELDCHANGED de IPN \_

Se envía cuando el usuario cambia un campo del control o se mueve de un campo a otro. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
IPN_FIELDCHANGED

    lpnmipa = (LPNMIPADDRESS) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMIPADDRESS**](/windows/win32/api/commctrl/ns-commctrl-nmipaddress) que contiene información sobre la dirección cambiada. El **miembro iValue** de esta estructura contendrá el valor especificado, incluso si está fuera del intervalo del campo. Puede modificar este miembro a cualquier valor que esté dentro del intervalo del campo en respuesta a este código de notificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Se omite el valor devuelto.

## <a name="remarks"></a>Comentarios

Este código de notificación no se envía en respuesta a un [**mensaje \_ SETADDRESS de IPM.**](ipm-setaddress.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





