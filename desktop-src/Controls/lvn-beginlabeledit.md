---
title: LVN_BEGINLABELEDIT de notificación (Commctrl.h)
description: Notifica a la ventana primaria de un control de vista de lista el inicio de la edición de etiquetas para un elemento. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: c13a9e95-22a9-476e-aeee-4928b8b096b0
keywords:
- LVN_BEGINLABELEDIT código de notificación Windows controles
topic_type:
- apiref
api_name:
- LVN_BEGINLABELEDIT
- LVN_BEGINLABELEDITA
- LVN_BEGINLABELEDITW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f77550b474534cee096b610a0805bce547d9b429
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362615"
---
# <a name="lvn_beginlabeledit-notification-code"></a>Código de notificación \_ LVN BEGINLABELEDIT

Notifica a la ventana primaria de un control de vista de lista el inicio de la edición de etiquetas para un elemento. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
LVN_BEGINLABELEDIT

    pdi = (LPNMLVDISPINFO) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMLVDISPINFO.**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) El **miembro** de elemento de esta estructura es [**una estructura LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) cuyo **miembro iItem** identifica el elemento que se está editando. Tenga en cuenta que los subelementos no se pueden editar; el **miembro iSubItem** siempre se establece en cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para permitir que el usuario edite la etiqueta, devuelva **FALSE.**

Para evitar que el usuario edite la etiqueta, devuelva **TRUE**.

## <a name="remarks"></a>Observaciones

Cuando comienza la edición de etiquetas, se crea, coloca e inicializa un control de edición. Antes de que se muestre, el control de vista de lista envía a su ventana primaria un código de notificación \_ LVN BEGINLABELEDIT.

Para personalizar la edición de etiquetas, implemente un controlador para LVN BEGINLABELEDIT y haga que envíe un mensaje \_ [**\_ GETEDITCONTROL**](lvm-geteditcontrol.md) de LVM al control de vista de lista. Si se está editando una etiqueta, el valor devuelto será un identificador para el control de edición. Use este identificador para personalizar el control de edición mediante el envío de los mensajes **EM \_ XXX habituales.**

Cuando el usuario cancela o completa la edición, la ventana primaria recibe un código de [notificación \_ LVN ENDLABELEDIT.](lvn-endlabeledit.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **LVN \_ BEGINLABELEDITW** (Unicode) y **LVN \_ BEGINLABELEDITA** (ANSI)<br/>     |



 

 





