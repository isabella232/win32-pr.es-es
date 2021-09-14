---
title: LVN_ENDLABELEDIT de notificación (Commctrl.h)
description: Notifica a la ventana primaria de un control de vista de lista el final de la edición de etiquetas de un elemento. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 03129fef-abf1-4374-b4b8-503c46ef7115
keywords:
- LVN_ENDLABELEDIT de notificación Windows controles
topic_type:
- apiref
api_name:
- LVN_ENDLABELEDIT
- LVN_ENDLABELEDITA
- LVN_ENDLABELEDITW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a33ab69a04202aeb3817d3eeadf01fb6f1fcaac
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362607"
---
# <a name="lvn_endlabeledit-notification-code"></a>Código de notificación \_ LVN ENDLABELEDIT

Notifica a la ventana primaria de un control de vista de lista el final de la edición de etiquetas de un elemento. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
LVN_ENDLABELEDIT

    pdi = (LPNMLVDISPINFO) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMLVDISPINFO.**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) El **miembro** de elemento de esta estructura es una [**estructura LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) cuyo **miembro iItem** identifica el elemento que se está editando. El **miembro pszText** del elemento contiene un valor válido cuando se envía el código de notificación  \_ LVN ENDLABELEDIT, independientemente de si la marca LVIF TEXT está establecida en el miembro mask de la estructura \_ **LVITEM.**  Si el usuario cancela la edición, el **miembro pszText** de la **estructura LVITEM** es **NULL**; de lo contrario, **pszText** es la dirección del texto editado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el **miembro pszText** de la estructura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) no es **NULL,** devuelve **TRUE** para establecer la etiqueta del elemento en el texto editado. Devuelve **FALSE** para rechazar el texto editado y revertir a la etiqueta original.

Si el **miembro pszText** de la [**estructura LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) **es NULL,** se omite el valor devuelto.

## <a name="remarks"></a>Observaciones

El valor devuelto del procedimiento de diálogo es si se controló el mensaje. El segundo valor devuelto debe establecerse llamando a [**SetwindowLongPtr**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra) **con DWLP_MSGRESULT**.

Cuando el usuario comienza a editar una etiqueta de elemento, la ventana primaria del control list-view recibe un código [de notificación \_ LVN BEGINLABELEDIT.](lvn-beginlabeledit.md) Cuando el usuario cancela o completa la edición, la ventana primaria recibe un código de notificación \_ LVN ENDLABELEDIT.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **LVN \_ ENDLABELEDITW** (Unicode) y **LVN \_ ENDLABELEDITA** (ANSI)<br/>         |



 

 





