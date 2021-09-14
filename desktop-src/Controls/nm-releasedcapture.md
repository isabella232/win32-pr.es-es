---
title: NM_RELEASEDCAPTURE de notificación (Commctrl.h)
description: Notifica a la ventana primaria de un control que el control está liberando la captura del mouse. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 222a3be1-20f1-43c6-b982-852512209a45
keywords:
- NM_RELEASEDCAPTURE código de notificación Windows controles
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
ms.openlocfilehash: 2d1510fd3bbdd6877dba279cbfb9c69c14146a2c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167862"
---
# <a name="nm_releasedcapture-notification-code"></a>Código de \_ notificación NM RELEASEDCAPTURE

Notifica a la ventana primaria de un control que el control está liberando la captura del mouse. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


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

A menos que se especifique lo contrario, el control omite el valor devuelto de este código de notificación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





