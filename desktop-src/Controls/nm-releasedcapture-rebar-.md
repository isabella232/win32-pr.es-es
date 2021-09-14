---
title: NM_RELEASEDCAPTURE de notificación (rebar) (Commctrl.h)
description: Notifica a la ventana primaria de un control rebar que el control está liberando la captura del mouse. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 1196260f-b9ba-4a9e-80a7-e126196c3beb
keywords:
- NM_RELEASEDCAPTURE (rebar) notification code Windows Controls
topic_type:
- apiref
api_name:
- NM_RELEASEDCAPTURE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c2f5367a0a5d5fac0948493ef70e4be1140013c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167889"
---
# <a name="nm_releasedcapture-rebar-notification-code"></a>Código \_ de notificación NM RELEASEDCAPTURE (rebar)

Notifica a la ventana primaria de un control rebar que el control está liberando la captura del mouse. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
NM_RELEASEDCAPTURE

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contiene información adicional sobre esta notificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El control omite el valor devuelto de este código de notificación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





