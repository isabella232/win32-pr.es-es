---
title: NM_RDBLCLK de notificación (vista de lista) (Commctrl.h)
description: Lo envía un control de vista de lista cuando el usuario hace doble clic en un elemento con el botón derecho del mouse. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: ebbb127f-07bd-48e0-bf38-7bbda5802f70
keywords:
- NM_RDBLCLK (vista de lista) de código de notificación Windows controles
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
ms.openlocfilehash: 41832b228fe40b212c0aba809b15022c6f7b39ce
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167930"
---
# <a name="nm_rdblclk-list-view-notification-code"></a>Código \_ de notificación DE NM RDBLCLK (vista de lista)

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

## <a name="remarks"></a>Observaciones

El **miembro iItem** de *lParam* solo es válido si se ha hecho clic en el icono o la etiqueta de primera columna. Para determinar qué elemento se selecciona cuando se realiza un clic en otra parte de una fila, envíe un mensaje [**\_ LVM SUBITEMHITTEST.**](lvm-subitemhittest.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





