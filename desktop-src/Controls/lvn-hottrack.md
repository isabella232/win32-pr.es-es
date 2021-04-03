---
title: Código de notificación de LVN_HOTTRACK (commctrl. h)
description: Lo envía un control de vista de lista cuando el usuario mueve el mouse sobre un elemento. Este código de notificación solo lo envían los controles de vista de lista que tienen \_ el \_ estilo de vista de lista extendido LVS ex TRACKSELECT. Se envía en forma de un mensaje de notificación de WM \_ .
ms.assetid: 6bbfe6b8-9b67-49e4-9481-65abe98608bb
keywords:
- LVN_HOTTRACK controles de código de notificación de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905695"
---
# <a name="lvn_hottrack-notification-code"></a>Código de notificación de HOTTRACK de LVN \_

Lo envía un control de vista de lista cuando el usuario mueve el mouse sobre un elemento. Este código de notificación solo lo envían los controles de vista de lista que tienen el estilo de vista de lista extendido [**LVS \_ ex \_ TRACKSELECT**](extended-list-view-styles.md) . Se envía en forma de un mensaje de [**\_ notificación de WM**](wm-notify.md) .


```C++
LVN_HOTTRACK

    lpnmlv = (LPNMLISTVIEW) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) que contiene información sobre este código de notificación. Los miembros **iItem**, **iSubItem** y **ptAction** de esta estructura contienen información sobre el elemento. La aplicación receptora puede modificar el miembro **iItem** para especificar el elemento que se seleccionará. Si **iItem** se establece en-1, no se seleccionará ningún elemento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero para permitir que la vista de lista realice su procesamiento de selección de pista normal. Si la aplicación devuelve un valor distinto de cero, el elemento no se seleccionará.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





