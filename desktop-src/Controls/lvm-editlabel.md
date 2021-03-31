---
title: Mensaje de LVM_EDITLABEL (commctrl. h)
description: Comienza la edición en contexto del texto del elemento de vista de lista especificado. El mensaje selecciona y centra implícitamente el elemento especificado. Puede enviar este mensaje explícitamente o mediante la \_ macro EditLabel de ListView.
ms.assetid: b63f13f1-6e66-4770-af84-30bcdb241727
keywords:
- LVM_EDITLABEL controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_EDITLABEL
- LVM_EDITLABELA
- LVM_EDITLABELW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25cb4e119731c41130e1c19fdea2f74882796435
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801124"
---
# <a name="lvm_editlabel-message"></a>\_Mensaje EDITLABEL LVM

Comienza la edición en contexto del texto del elemento de vista de lista especificado. El mensaje selecciona y centra implícitamente el elemento especificado. Puede enviar este mensaje explícitamente o mediante la macro [**\_ EditLabel de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_editlabel) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice del elemento de vista de lista. Para cancelar la edición, establezca el índice en-1.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el identificador del control de edición que se usa para editar el texto del elemento si se realiza correctamente, o **null** en caso contrario.

## <a name="remarks"></a>Observaciones

Cuando el usuario finaliza o cancela la edición, el control de edición se destruye y el identificador ya no es válido. Puede crear una subclase del control de edición, pero no debe destruirlo.

El control debe tener el foco antes de enviar este mensaje al control. El foco se puede establecer mediante la función [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) .

Si *wParam* es-1, se envía un código de notificación [ \_ ENDLABELEDIT de LVN](lvn-endlabeledit.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **LVM \_ EDITLABELW** (Unicode) y **\_ EDITLABELA de LVM** (ANSI)<br/>               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CANCELMODE de WM \_**](/windows/desktop/winmsg/wm-cancelmode)
</dt> </dl>

 

