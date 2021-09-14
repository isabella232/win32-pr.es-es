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
ms.openlocfilehash: aebf628eb9387acd4fd10f100f2f80570d1b021b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167813"
---
# <a name="nm_tvstateimagechanging-notification-code"></a>Código \_ de notificación NM TVSTATEIMAGECHANGING

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
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





