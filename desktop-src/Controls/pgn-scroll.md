---
title: PGN_SCROLL de notificación (Commctrl.h)
description: Notifica a la ventana primaria de un control de paginación que la ventana independiente está a punto de desplazarse. Esta notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 3d40e75e-c445-4885-b807-8cfcb92cb2d9
keywords:
- PGN_SCROLL código de notificación Windows controles
topic_type:
- apiref
api_name:
- PGN_SCROLL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 864903c73eeb611d1c748ec6a4d936192a1a27f22d3f37115af8879916286a8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117830149"
---
# <a name="pgn_scroll-notification-code"></a>Código de notificación SCROLL de PGN \_

Notifica a la ventana primaria de un control de paginación que la ventana independiente está a punto de desplazarse. Esta notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
PGN_SCROLL

    lpnms = (LPNMPGSCROLL) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMPGSCROLL**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgscroll) que contiene y recibe información sobre el código de notificación. El **miembro iDir** de esta estructura indica la dirección del desplazamiento. Los **miembros iXpos** **e iYpos** contienen la posición horizontal y vertical de la ventana independiente antes del desplazamiento. El **miembro iScroll** contiene la cantidad diferencial de desplazamiento predeterminada. Puede modificar este miembro a una cantidad de desplazamiento diferente si lo desea.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Se omite el valor devuelto.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





