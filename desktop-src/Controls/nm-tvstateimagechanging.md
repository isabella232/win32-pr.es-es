---
title: NM_TVSTATEIMAGECHANGING de notificación (Commctrl.h)
description: Enviado por un control de vista de árbol a su ventana primaria que cambia la imagen de estado. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 8e42d8b3-5e76-4d03-94b0-3e4583669095
keywords:
- NM_TVSTATEIMAGECHANGING código de notificación Windows controles
topic_type:
- apiref
api_name:
- NM_TVSTATEIMAGECHANGING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a57da81dbcccf4dcfbb896417e15c8788bb8d3f6baba71a57a6a99f053a3ba45
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119433685"
---
# <a name="nm_tvstateimagechanging-notification-code"></a>Código \_ de notificación DE NM TVSTATEIMAGECHANGING

Enviado por un control de vista de árbol a su ventana primaria que cambia la imagen de estado. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
NM_TVSTATEIMAGECHANGING
        
    lpnmtsic = (LPNMTVSTATEIMAGECHANGING) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMTVSTATEIMAGECHANGING**](/windows/win32/api/commctrl/ns-commctrl-nmtvstateimagechanging) que contiene información adicional sobre esta notificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El control omite el valor devuelto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





