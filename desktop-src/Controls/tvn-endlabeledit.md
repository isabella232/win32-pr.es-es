---
title: Código de notificación de TVN_ENDLABELEDIT (commctrl. h)
description: Notifica a la ventana primaria de un control de vista de árbol sobre el final de la edición de etiquetas para un elemento. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 82eb9fcd-de10-4efb-8501-78c5af5e089e
keywords:
- TVN_ENDLABELEDIT controles de código de notificación de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150359"
---
# <a name="tvn_endlabeledit-notification-code"></a>Código de notificación de ENDLABELEDIT de TVN \_

Notifica a la ventana primaria de un control de vista de árbol sobre el final de la edición de etiquetas para un elemento. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
TVN_ENDLABELEDIT 

    ptvdi = (LPNMTVDISPINFO) lParam 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) . El **miembro** de esta estructura es una estructura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) cuyos miembros **hItem**, **lParam** y **miembros pszText** contienen información válida sobre el elemento que se editó. Si se canceló la edición de la etiqueta, el miembro **miembros pszText** de la estructura **TVITEM** es **null**. de lo contrario, **miembros pszText** es la dirección del texto editado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el miembro **miembros pszText** no es **null**, devuelva **true** para establecer la etiqueta del elemento en el texto editado. Devuelve **false** para rechazar el texto editado y volver a la etiqueta original.

## <a name="remarks"></a>Observaciones

Si el miembro **miembros pszText** es **null**, se omite el valor devuelto.

Si especificó el \_ valor de LPSTR TEXTCALLBACK para este elemento y el miembro **miembros pszText** no es **null**, el \_ controlador TVN ENDLABELEDIT debe copiar el texto de **miembros pszText** en el almacenamiento local.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **TVN \_ ENDLABELEDITW** (Unicode) y **TVN \_ ENDLABELEDITA** (ANSI)<br/>         |



 

 





