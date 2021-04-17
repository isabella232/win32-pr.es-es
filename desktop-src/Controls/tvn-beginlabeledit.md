---
title: Código de notificación de TVN_BEGINLABELEDIT (commctrl. h)
description: Notifica a la ventana primaria de un control de vista de árbol sobre el inicio de la edición de la etiqueta de un elemento. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 67ed1f1f-7ccc-4e84-9540-4a46f6cd3a44
keywords:
- TVN_BEGINLABELEDIT controles de código de notificación de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658209"
---
# <a name="tvn_beginlabeledit-notification-code"></a>Código de notificación de BEGINLABELEDIT de TVN \_

Notifica a la ventana primaria de un control de vista de árbol sobre el inicio de la edición de la etiqueta de un elemento. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
TVN_BEGINLABELEDIT 

    ptvdi = (LPNMTVDISPINFO) lParam 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) . El miembro del **elemento** es una estructura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) que contiene información válida sobre el elemento que se está editando en los miembros **hItem**, **State**, **lParam** y **miembros pszText** .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** para cancelar la edición de la etiqueta.

## <a name="remarks"></a>Observaciones

Cuando comienza la edición de etiquetas, se crea un control de edición pero no se coloca ni se muestra. Antes de que se muestre, el control de vista de árbol envía a su ventana primaria un \_ código de notificación TVN BEGINLABELEDIT.

Para personalizar la edición de etiquetas, implemente un controlador para TVN \_ BEGINLABELEDIT y envíe un mensaje [**TVM \_ GETEDITCONTROL**](tvm-geteditcontrol.md) al control de vista de árbol. Si se está editando una etiqueta, el valor devuelto será un identificador del control de edición. Use este identificador para personalizar el control de edición mediante el envío de los mensajes de EM \_ XXX habituales.

Cuando el usuario cancela o completa la edición, la ventana primaria recibe un código de notificación [TVN \_ ENDLABELEDIT](tvn-endlabeledit.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **TVN \_ BEGINLABELEDITW** (Unicode) y **TVN \_ BEGINLABELEDITA** (ANSI)<br/>     |



 

 





