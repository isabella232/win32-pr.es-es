---
title: LVN_ODSTATECHANGED de notificación (Commctrl.h)
description: Enviado por un control de vista de lista cuando el estado de un elemento o intervalo de elementos ha cambiado. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: a3aafda5-a3ec-4f84-8153-8d34097e04f1
keywords:
- LVN_ODSTATECHANGED de notificación Windows controles
topic_type:
- apiref
api_name:
- LVN_ODSTATECHANGED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdf8712078e3398f775115233c0fd54622943cc2cb7febe0c24d800776418de5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915115"
---
# <a name="lvn_odstatechanged-notification-code"></a>Código de notificación \_ LVN ODSTATECHANGED

Enviado por un control de vista de lista cuando el estado de un elemento o intervalo de elementos ha cambiado. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
LVN_ODSTATECHANGED

    lpStateChange = (LPNMLVODSTATECHANGE) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMLVODSTATECHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmlvodstatechange) que contiene información sobre el elemento o los elementos que han cambiado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La aplicación que recibe este código de notificación debe devolver cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





