---
title: RBN_AUTOBREAK mensaje (Commctrl.h)
description: Notifica al elemento primario de una barra de rebar que aparecerá una interrupción en la barra. El elemento primario determina si se debe realizar la interrupción. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: b7a63027-6cfa-4d5a-9ea6-fdd8b4fb6864
keywords:
- RBN_AUTOBREAK controles de Windows mensaje
topic_type:
- apiref
api_name:
- RBN_AUTOBREAK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d614277d89578cb66e528ba16656ed55681ebbcf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167245"
---
# <a name="rbn_autobreak-message"></a>Mensaje \_ AUTOBREAK de RBN

Notifica al elemento [primario de una barra](rebar-controls.md) de rebar que aparecerá una interrupción en la barra. El elemento primario determina si se debe realizar la interrupción. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
RBN_AUTOBREAK

    pnmRebarAutoBreak = (LPNMREBARAUTOBREAK) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMREBARAUTOBREAK**](/windows/win32/api/commctrl/ns-commctrl-nmrebarautobreak) que contiene información sobre el código de notificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se usa el valor devuelto para esta notificación.

## <a name="remarks"></a>Observaciones

El valor del **miembro fAutoBreak** de la estructura [**NMREBARAUTOBREAK**](/windows/win32/api/commctrl/ns-commctrl-nmrebarautobreak) indica si se debe producir una interrupción en la barra rebar.

Para usar este código de notificación, especifique Comctl32.dll versión 6 en el manifiesto. Para obtener más información sobre los manifiestos, vea [Habilitar estilos visuales.](cookbook-overview.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





