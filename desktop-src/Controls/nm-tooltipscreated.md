---
title: NM_TOOLTIPSCREATED de notificación (Commctrl.h)
description: Notifica a la ventana primaria de un control que el control ha creado un control de información sobre herramientas. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 8108f084-212d-4a16-b604-1ec134b1bb43
keywords:
- NM_TOOLTIPSCREATED de notificación Windows controles
topic_type:
- apiref
api_name:
- NM_TOOLTIPSCREATED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e2e99850b17b0f2b06948a09b70a89e67e65a50
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167817"
---
# <a name="nm_tooltipscreated-notification-code"></a>NM \_ TOOLTIPSCreateD notification code

Notifica a la ventana primaria de un control que el control ha creado un control de información sobre herramientas. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
NM_TOOLTIPSCREATED

    lpnmttc = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMTOOLTIPSCREATED**](/windows/win32/api/commctrl/ns-commctrl-nmtooltipscreated) que contiene información adicional sobre esta notificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

A menos que se especifique lo contrario, el control omite el valor devuelto de este código de notificación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





