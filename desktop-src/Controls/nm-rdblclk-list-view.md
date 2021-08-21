---
title: NM_RDBLCLK de notificación (vista de lista) (Commctrl.h)
description: Lo envía un control de vista de lista cuando el usuario hace doble clic en un elemento con el botón derecho del mouse. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: ebbb127f-07bd-48e0-bf38-7bbda5802f70
keywords:
- NM_RDBLCLK (vista de lista) código de notificación Windows controles
topic_type:
- apiref
api_name:
- NM_RDBLCLK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c0197659f89392d352e2500d37cbda9dadee5487c5ee180123f502d127925a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957994"
---
# <a name="nm_rdblclk-list-view-notification-code"></a>Código de notificación DE NM \_ RDBLCLK (vista de lista)

Lo envía un control de vista de lista cuando el usuario hace doble clic en un elemento con el botón derecho del mouse. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
NM_RDBLCLK

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



 

 





