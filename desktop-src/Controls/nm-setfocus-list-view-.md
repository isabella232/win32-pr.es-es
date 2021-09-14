---
title: NM_SETFOCUS de notificación (vista de lista) (Commctrl.h)
description: Notifica a la ventana primaria de un control de vista de lista que el control ha recibido el foco de entrada. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 43d3b09a-f095-4f30-87a8-2f2e782d6720
keywords:
- NM_SETFOCUS (vista de lista) código de notificación Windows controles
topic_type:
- apiref
api_name:
- NM_SETFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99cc84e76c0203a6e2930d3d9f50bc61a1e31395
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167838"
---
# <a name="nm_setfocus-list-view-notification-code"></a>Código de notificación DE NM \_ SETFOCUS (vista de lista)

Notifica a la ventana primaria de un control de vista de lista que el control ha recibido el foco de entrada. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
NM_SETFOCUS 

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contiene información adicional sobre esta notificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se usa el valor devuelto para esta notificación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





