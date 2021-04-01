---
title: Código de notificación de LVN_BEGINLABELEDIT (commctrl. h)
description: Notifica a la ventana primaria de un control de vista de lista el inicio de la edición de la etiqueta de un elemento. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: c13a9e95-22a9-476e-aeee-4928b8b096b0
keywords:
- LVN_BEGINLABELEDIT controles de código de notificación de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103995974"
---
# <a name="lvn_beginlabeledit-notification-code"></a>Código de notificación de BEGINLABELEDIT de LVN \_

Notifica a la ventana primaria de un control de vista de lista el inicio de la edición de la etiqueta de un elemento. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
LVN_BEGINLABELEDIT

    pdi = (LPNMLVDISPINFO) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) . El miembro del **elemento** de esta estructura es una estructura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) cuyo miembro **iItem** identifica el elemento que se está editando. Tenga en cuenta que no se pueden editar los subelementos; el miembro **iSubItem** siempre se establece en cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para permitir al usuario editar la etiqueta, devuelva **false**.

Para evitar que el usuario edite la etiqueta, devuelva **true**.

## <a name="remarks"></a>Observaciones

Cuando comienza la edición de etiquetas, se crea, coloca y Inicializa un control de edición. Antes de que se muestre, el control de vista de lista envía a su ventana primaria un \_ código de notificación LVN BEGINLABELEDIT.

Para personalizar la edición de etiquetas, implemente un controlador para LVN \_ BEGINLABELEDIT y envíe un mensaje [**LVM \_ GETEDITCONTROL**](lvm-geteditcontrol.md) al control de vista de lista. Si se está editando una etiqueta, el valor devuelto será un identificador del control de edición. Use este identificador para personalizar el control de edición mediante el envío de los mensajes de **em \_ XXX** habituales.

Cuando el usuario cancela o completa la edición, la ventana primaria recibe un código de notificación [LVN \_ ENDLABELEDIT](lvn-endlabeledit.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **LVN \_ BEGINLABELEDITW** (Unicode) y **LVN \_ BEGINLABELEDITA** (ANSI)<br/>     |



 

 





