---
title: LVN_COLUMNDROPDOWN de notificación (Commctrl.h)
description: Lo envía un control list-view cuando se presiona el botón desplegable de la vista de lista. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 752d745e-4482-425c-af3c-f9707cbb03d7
keywords:
- LVN_COLUMNDROPDOWN código de notificación Windows controles
topic_type:
- apiref
api_name:
- LVN_COLUMNDROPDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 792d29268548d95a7f3e70b05d9d2de368a03cd6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362611"
---
# <a name="lvn_columndropdown-notification-code"></a>Código de notificación \_ LVN COLUMNDROPDOWN

Lo envía un control list-view cuando se presiona el botón desplegable de la vista de lista. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
LVN_COLUMNDROPDOWN
        
    pnmv = (LPNMLISTVIEW) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* \[ En\]
</dt> <dd>

Puntero a una [**estructura NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) que describe el código de notificación. El autor de la llamada es responsable de asignar esta estructura, incluida la estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) contenida. Establezca los miembros de la **estructura NMHDR.** El **miembro** de código debe establecerse en LVN \_ COLUMNDROPDOWN.

Establezca el **miembro iItem** de la [**estructura NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) en -1. Establezca el **miembro iSubItem** en el índice del subelemento. Establezca los **miembros uNewState**, **uOldState** y **lParam** en cero. No se usan los miembros restantes de la estructura **NMLISTVIEW.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El receptor de notificaciones convierte *lParam* para recuperar la [**estructura NMLISTVIEW.**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) El *parámetro wParam* contiene el identificador del control que envía el código de notificación.

Si un control de encabezado es un elemento secundario de la vista de lista, el control de encabezado debe enviar este código de notidication al control list-view cuando el control de encabezado recibe el código de notificación DE LISTA DESPLEGABLE de [HDN. \_ ](hdn-dropdown.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





