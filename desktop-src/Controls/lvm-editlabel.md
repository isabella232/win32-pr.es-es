---
title: LVM_EDITLABEL mensaje (Commctrl.h)
description: Comienza la edición en contexto del texto del elemento de vista de lista especificado. El mensaje selecciona y centra implícitamente el elemento especificado. Puede enviar este mensaje explícitamente o mediante la macro ListView \_ EditLabel.
ms.assetid: b63f13f1-6e66-4770-af84-30bcdb241727
keywords:
- LVM_EDITLABEL controles de Windows mensaje
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
ms.openlocfilehash: a9be1896c39e06c25bf06e033d74a17107b3e194a43b1c574e1dcb7f9a456413
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118411849"
---
# <a name="lvm_editlabel-message"></a>Mensaje LVM \_ EDITLABEL

Comienza la edición en contexto del texto del elemento de vista de lista especificado. El mensaje selecciona y centra implícitamente el elemento especificado. Puede enviar este mensaje explícitamente o mediante la macro [**ListView \_ EditLabel.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_editlabel)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice del elemento list-view. Para cancelar la edición, establezca el índice en -1.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el identificador al control de edición que se usa para editar el texto del elemento si se realiza correctamente o **NULL** en caso contrario.

## <a name="remarks"></a>Comentarios

Cuando el usuario completa o cancela la edición, el control de edición se destruye y el identificador ya no es válido. Puede crear subclases del control de edición, pero no debe destruirlo.

El control debe tener el foco antes de enviar este mensaje al control . El foco se puede establecer mediante la [**función SetFocus.**](/windows/desktop/api/winuser/nf-winuser-setfocus)

Si *wParam es* -1, se envía [un código de notificación \_ ENDLABELEDIT de LVN.](lvn-endlabeledit.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **LVM \_ EDITLABELW** (Unicode) y **LVM \_ EDITLABELA** (ANSI)<br/>               |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**WM \_ CANCELMODE**](/windows/desktop/winmsg/wm-cancelmode)
</dt> </dl>

 

