---
title: LVN_HOTTRACK de notificación (Commctrl.h)
description: Enviado por un control de vista de lista cuando el usuario mueve el mouse sobre un elemento. Este código de notificación solo se envía mediante controles de vista de lista que tienen el estilo de vista de lista extendido LVS \_ EX \_ TRACKSELECT. Se envía en forma de mensaje WM \_ NOTIFY.
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
ms.openlocfilehash: c677b69fa21cdbe3680442304f6745cfb3a907de
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072313"
---
# <a name="lvn_hottrack-notification-code"></a>Código de notificación \_ DE LVN HOTTRACK

Enviado por un control de vista de lista cuando el usuario mueve el mouse sobre un elemento. Este código de notificación solo se envía mediante controles de vista de lista que tienen el estilo de vista de lista extendido [**LVS \_ EX \_ TRACKSELECT.**](extended-list-view-styles.md) Se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
LVN_HOTTRACK

    lpnmlv = (LPNMLISTVIEW) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) que contiene información sobre este código de notificación. Los **miembros iItem**, **iSubItem** y **ptAction** de esta estructura contienen información sobre el elemento. La aplicación receptora puede modificar el **miembro iItem** para especificar el elemento que se seleccionará. Si **iItem** se establece en -1, no se seleccionará ningún elemento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero para permitir que la vista de lista realice su procesamiento de selección de seguimiento normal. Si la aplicación devuelve un valor distinto de cero, el elemento no se seleccionará.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





