---
title: LVN_HOTTRACK de notificación (Commctrl.h)
description: Enviado por un control de vista de lista cuando el usuario mueve el mouse sobre un elemento. Este código de notificación solo se envía mediante controles de vista de lista que tienen el estilo de vista de lista extendida LVS \_ EX \_ TRACKSELECT. Se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 6bbfe6b8-9b67-49e4-9481-65abe98608bb
keywords:
- LVN_HOTTRACK código de notificación Windows controles
topic_type:
- apiref
api_name:
- LVN_HOTTRACK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ab311b17f287b695a6b21d333f7183fdda272029e2c57dfe468527d765d1602
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117830436"
---
# <a name="lvn_hottrack-notification-code"></a>Código de notificación \_ DE LVN HOTTRACK

Enviado por un control de vista de lista cuando el usuario mueve el mouse sobre un elemento. Este código de notificación solo se envía mediante controles de vista de lista que tienen el estilo de vista de lista extendida [**LVS \_ EX \_ TRACKSELECT.**](extended-list-view-styles.md) Se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
LVN_HOTTRACK

    lpnmlv = (LPNMLISTVIEW) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) que contiene información sobre este código de notificación. Los **miembros iItem**, **iSubItem** y **ptAction** de esta estructura contienen información sobre el elemento. La aplicación receptora puede modificar el **miembro iItem** para especificar el elemento que se seleccionará. Si **iItem** está establecido en -1, no se seleccionará ningún elemento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero para permitir que la vista de lista realice su procesamiento normal de selección de seguimiento. Si la aplicación devuelve un valor distinto de cero, no se seleccionará el elemento.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





