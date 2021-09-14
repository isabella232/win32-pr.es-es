---
title: TVN_BEGINLABELEDIT de notificación (Commctrl.h)
description: Notifica a la ventana primaria de un control de vista de árbol el inicio de la edición de etiquetas para un elemento. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 67ed1f1f-7ccc-4e84-9540-4a46f6cd3a44
keywords:
- TVN_BEGINLABELEDIT código de notificación Windows controles
topic_type:
- apiref
api_name:
- TVN_BEGINLABELEDIT
- TVN_BEGINLABELEDITA
- TVN_BEGINLABELEDITW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34eccdeda553d0792a2862e3ca81a0889539d5ae
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165585"
---
# <a name="tvn_beginlabeledit-notification-code"></a>Código de notificación \_ BEGINLABELEDIT de TVN

Notifica a la ventana primaria de un control de vista de árbol el inicio de la edición de etiquetas para un elemento. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TVN_BEGINLABELEDIT 

    ptvdi = (LPNMTVDISPINFO) lParam 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMTVDISPINFO.**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) El **miembro** de elemento es una [**estructura TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) que contiene información válida sobre el elemento que se está editando en los miembros **hItem**, **state**, **lParam** y **pszText.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE para** cancelar la edición de etiquetas.

## <a name="remarks"></a>Observaciones

Cuando comienza la edición de etiquetas, se crea un control de edición, pero no se coloca ni se muestra. Antes de que se muestre, el control de vista de árbol envía a su ventana primaria un código de notificación \_ BEGINLABELEDIT de TVN.

Para personalizar la edición de etiquetas, implemente un controlador para TVN BEGINLABELEDIT y haga que envíe un mensaje \_ [**\_ GETEDITCONTROL**](tvm-geteditcontrol.md) de TVM al control de vista de árbol. Si se edita una etiqueta, el valor devuelto será un identificador del control de edición. Use este identificador para personalizar el control de edición mediante el envío de los mensajes EM \_ XXX habituales.

Cuando el usuario cancela o completa la edición, la ventana primaria recibe un código de [notificación \_ ENDLABELEDIT de TVN.](tvn-endlabeledit.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **TVN \_ BEGINLABELEDITW** (Unicode) y **TVN \_ BEGINLABELEDITA** (ANSI)<br/>     |



 

 





