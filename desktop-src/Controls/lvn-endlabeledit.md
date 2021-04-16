---
title: Código de notificación de LVN_ENDLABELEDIT (commctrl. h)
description: Notifica a la ventana primaria de un control de vista de lista el final de la edición de la etiqueta de un elemento. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 03129fef-abf1-4374-b4b8-503c46ef7115
keywords:
- LVN_ENDLABELEDIT controles de código de notificación de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658422"
---
# <a name="lvn_endlabeledit-notification-code"></a>Código de notificación de ENDLABELEDIT de LVN \_

Notifica a la ventana primaria de un control de vista de lista el final de la edición de la etiqueta de un elemento. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
LVN_ENDLABELEDIT

    pdi = (LPNMLVDISPINFO) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) . El miembro del **elemento** de esta estructura es una estructura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) cuyo miembro **iItem** identifica el elemento que se está editando. El miembro **miembros pszText** del **elemento** contiene un valor válido cuando \_ se envía el código de notificación LVN ENDLABELEDIT, independientemente de si la \_ marca de texto LVIF está establecida en el miembro **Mask** de la estructura **LVITEM** . Si el usuario cancela la edición, el miembro **miembros pszText** de la estructura **LVITEM** es **null**. de lo contrario, **miembros pszText** es la dirección del texto editado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el miembro **miembros pszText** de la estructura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) no es **null**, devuelva **true** para establecer la etiqueta del elemento en el texto editado. Devuelve **false** para rechazar el texto editado y volver a la etiqueta original.

Si el miembro **miembros pszText** de la estructura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) es **null**, se omite el valor devuelto.

## <a name="remarks"></a>Observaciones

El valor devuelto del procedimiento de cuadro de diálogo es si se controló el mensaje. El segundo valor devuelto se debe establecer llamando a [**SetwindowLongPtr**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra) con **DWLP_MSGRESULT**.

Cuando el usuario comienza a editar una etiqueta de elemento, la ventana primaria del control de vista de lista recibe un código de notificación [LVN \_ BEGINLABELEDIT](lvn-beginlabeledit.md) . Cuando el usuario cancela o completa la edición, la ventana primaria recibe un \_ código de notificación LVN ENDLABELEDIT.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **LVN \_ ENDLABELEDITW** (Unicode) y **LVN \_ ENDLABELEDITA** (ANSI)<br/>         |



 

 





