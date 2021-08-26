---
title: LVN_INSERTITEM de notificación (Commctrl.h)
description: Notifica a la ventana primaria de un control de vista de lista que se insertó un nuevo elemento. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 8d368fb2-e4fc-4dc4-a89e-872ba1278b75
keywords:
- LVN_INSERTITEM código de notificación Windows controles
topic_type:
- apiref
api_name:
- LVN_INSERTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee1c706c7329e192559cb307962e293f0bbf02109c81fcde177eb36d8d39e37e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062155"
---
# <a name="lvn_insertitem-notification-code"></a>Código de notificación \_ LVN INSERTITEM

Notifica a la ventana primaria de un control de vista de lista que se insertó un nuevo elemento. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
LVN_INSERTITEM

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMLISTVIEW.**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) El **miembro iItem** identifica el nuevo elemento y los demás miembros son cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





