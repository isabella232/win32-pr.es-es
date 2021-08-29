---
title: NM_DBLCLK (vista de lista) código de notificación (Commctrl.h)
description: Enviado por un control de vista de lista cuando el usuario hace doble clic en un elemento con el botón izquierdo del mouse. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 28455109-177e-4932-88c5-500a3a91c13a
keywords:
- NM_DBLCLK (vista de lista) de código de notificación Windows controles
topic_type:
- apiref
api_name:
- NM_DBLCLK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3590b417954f67c454b6cece979bdd6eac4706fa5dfc97b7dda30be6dde183c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919705"
---
# <a name="nm_dblclk-list-view-notification-code"></a>Código de notificación de NM \_ DBLCLK (vista de lista)

Enviado por un control de vista de lista cuando el usuario hace doble clic en un elemento con el botón izquierdo del mouse. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
NM_DBLCLK
        
    lpnmitem = (LPNMITEMACTIVATE) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

[Versión 4.71.](common-control-versions.md) Puntero a una [**estructura NMITEMACTIVATE**](/windows/win32/api/commctrl/ns-commctrl-nmitemactivate) que contiene información adicional sobre esta notificación. Los **miembros iItem**, **iSubItem** y **ptAction** de esta estructura contienen información sobre el elemento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se usa el valor devuelto para esta notificación.

## <a name="remarks"></a>Comentarios

El **miembro iItem** de *lParam* solo es válido si se ha hecho clic en el icono o la etiqueta de primera columna. Para determinar qué elemento se selecciona cuando se hace clic en otra parte de una fila, envíe un mensaje [**LVM \_ SUBITEMHITTEST.**](lvm-subitemhittest.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





