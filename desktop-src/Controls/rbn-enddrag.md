---
title: RBN_ENDDRAG de notificación (Commctrl.h)
description: Enviado por un control rebar cuando el usuario deja de arrastrar una banda. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 24b06144-6a4c-46a4-bef1-d6592f72a2c0
keywords:
- RBN_ENDDRAG código de notificación Windows controles
topic_type:
- apiref
api_name:
- RBN_ENDDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2eb6c538679d793ed2407775b4238cea475ba4ef
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167217"
---
# <a name="rbn_enddrag-notification-code"></a>Código de notificación \_ ENDDRAG de RBN

Enviado por un control rebar cuando el usuario deja de arrastrar una banda. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
RBN_ENDDRAG

    lpnmrb = (LPNMREBAR) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMREBAR**](/windows/win32/api/commctrl/ns-commctrl-nmrebar) que contiene información sobre el código de notificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se usa el valor devuelto para este código de notificación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





