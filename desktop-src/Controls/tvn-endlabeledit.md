---
title: TVN_ENDLABELEDIT de notificación (Commctrl.h)
description: Notifica a la ventana primaria de un control de vista de árbol el final de la edición de etiquetas de un elemento. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 82eb9fcd-de10-4efb-8501-78c5af5e089e
keywords:
- TVN_ENDLABELEDIT código de notificación Windows controles
topic_type:
- apiref
api_name:
- TVN_ENDLABELEDIT
- TVN_ENDLABELEDITA
- TVN_ENDLABELEDITW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c30d494ad90b3d55f85b1ad154aed0f814a1eec
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165570"
---
# <a name="tvn_endlabeledit-notification-code"></a>Código de notificación \_ ENDLABELEDIT de TVN

Notifica a la ventana primaria de un control de vista de árbol el final de la edición de etiquetas de un elemento. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TVN_ENDLABELEDIT 

    ptvdi = (LPNMTVDISPINFO) lParam 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMTVDISPINFO.**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) El **miembro item** de esta estructura es una estructura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) cuyos miembros **hItem,** **lParam** y **pszText** contienen información válida sobre el elemento que se editó. Si se canceló la edición de etiquetas, el **miembro pszText** de la **estructura TVITEM** es **NULL**; De lo contrario, **pszText** es la dirección del texto editado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el **miembro pszText** no es **NULL,** devuelve **TRUE** para establecer la etiqueta del elemento en el texto editado. Devuelve **FALSE** para rechazar el texto editado y revertir a la etiqueta original.

## <a name="remarks"></a>Observaciones

Si el **miembro pszText** es **NULL,** se omite el valor devuelto.

Si especificó el valor LPSTR TEXTCALLBACK para este elemento y el miembro pszText no es NULL, el controlador ENDLABELEDIT de TVN debe copiar el texto de \_   \_ **pszText** en el almacenamiento local.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **TVN \_ ENDLABELEDITW** (Unicode) y **TVN \_ ENDLABELEDITA** (ANSI)<br/>         |



 

 





