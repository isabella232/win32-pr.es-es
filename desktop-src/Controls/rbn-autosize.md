---
title: RBN_AUTOSIZE de notificación (Commctrl.h)
description: Enviado por un control rebar creado con el estilo AUTOSIZE de RBS cuando la barra se cambia automáticamente \_ de tamaño. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: d174fe99-13cc-404c-9dc5-d5a93e9807a2
keywords:
- RBN_AUTOSIZE código de notificación Windows controles
topic_type:
- apiref
api_name:
- RBN_AUTOSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32c0ef601562c6887e05c78c06a66cf61e330843769eb3bb66105eb941e09339
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985375"
---
# <a name="rbn_autosize-notification-code"></a>Código de notificación AUTOSIZE de RBN \_

Enviado por un control rebar creado con el [**estilo \_ AUTOSIZE de RBS**](rebar-control-styles.md) cuando la barra se cambia automáticamente de tamaño. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
RBN_AUTOSIZE

    lpnmas = (LPNMRBAUTOSIZE) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMRBAUTOSIZE**](/windows/win32/api/commctrl/ns-commctrl-nmrbautosize) que contiene información sobre la operación de cambio de tamaño.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se usa el valor devuelto para esta notificación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





