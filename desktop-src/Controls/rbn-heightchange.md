---
title: RBN_HEIGHTCHANGE de notificación (Commctrl.h)
description: Enviado por un control rebar cuando ha cambiado su alto. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: cf90e38c-ac3e-4bef-b047-0956ae5041d1
keywords:
- RBN_HEIGHTCHANGE código de notificación Windows controles
topic_type:
- apiref
api_name:
- RBN_HEIGHTCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfe0601e8cb22ec9b86768741c5b455aa7f21eef
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167206"
---
# <a name="rbn_heightchange-notification-code"></a>Código de notificación HEIGHTCHANGE de RBN \_

Enviado por un control rebar cuando ha cambiado su alto. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
RBN_HEIGHTCHANGE

    lpnmhdr = (LPNMHDR) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contiene información adicional sobre esta notificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se usa el valor devuelto para esta notificación.

## <a name="remarks"></a>Observaciones

Los controles rebar que usan el [**estilo \_ CCS VERT**](common-control-styles.md) envían este código de notificación cuando cambia su ancho.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





