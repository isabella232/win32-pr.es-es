---
title: NM_CLICK de notificación (vista de lista) (Commctrl.h)
description: Lo envía un control de vista de lista cuando el usuario hace clic en un elemento con el botón izquierdo del mouse. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 7921bc27-54ca-4bb2-ac88-8267776661ab
keywords:
- NM_CLICK (vista de lista) de código de notificación Windows controles
topic_type:
- apiref
api_name:
- NM_CLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e9189861db0ec956b549145584202e3b88978478a9dd8de4386785d46e0d160
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061765"
---
# <a name="nm_click-list-view-notification-code"></a>Código \_ de notificación NM CLICK (vista de lista)

Lo envía un control de vista de lista cuando el usuario hace clic en un elemento con el botón izquierdo del mouse. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
NM_CLICK

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

El **miembro iItem** de *lParam* solo es válido si se ha hecho clic en el icono o la etiqueta de primera columna. Para determinar qué elemento se selecciona cuando se realiza un clic en otra parte de una fila, envíe un mensaje [**\_ LVM SUBITEMHITTEST.**](lvm-subitemhittest.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





