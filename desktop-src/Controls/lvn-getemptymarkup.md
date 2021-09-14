---
title: LVN_GETEMPTYMARKUP de notificación (Commctrl.h)
description: Enviado por el control de vista de lista a su ventana primaria cuando el control no tiene elementos. El código de notificación \_ LVN GETEMPTYMARKUP es una solicitud para que la ventana primaria proporcione texto de marcado. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 5ea74120-f347-493a-af14-6bda5b8f6082
keywords:
- LVN_GETEMPTYMARKUP código de notificación Windows controles
topic_type:
- apiref
api_name:
- LVN_GETEMPTYMARKUP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dea693475ca42f962be07936f980cd3f5d52479c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072314"
---
# <a name="lvn_getemptymarkup-notification-code"></a>Código de \_ notificación LVN GETEMPTYMARKUP

Enviado por el control de vista de lista a su ventana primaria cuando el control no tiene elementos. El código de notificación \_ LVN GETEMPTYMARKUP es una solicitud para que la ventana primaria proporcione texto de marcado. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
LVN_GETEMPTYMARKUP
        
    pnmMarkup = (NMLVEMPTYMARKUP*) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMLVEMPTYMARKUP.**](/windows/win32/api/commctrl/ns-commctrl-nmlvemptymarkup) Establezca los miembros de esta estructura para proporcionar texto de marcado para el control de vista de lista.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE** para establecer el texto de marcado en el control list-view o **FALSE** en caso contrario.

## <a name="remarks"></a>Observaciones

El receptor de notificaciones convierte *lParam* para recuperar la estructura [**NMLVEMPTYMARKUP.**](/windows/win32/api/commctrl/ns-commctrl-nmlvemptymarkup) El *parámetro wParam* contiene el identificador del control que envía este mensaje.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





