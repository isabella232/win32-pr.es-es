---
title: LVM_GETEDITCONTROL mensaje (Commctrl.h)
description: Obtiene el identificador del control de edición que se usa para editar el texto de un elemento de vista de lista. Puede enviar este mensaje explícitamente o mediante la macro \_ ListView GetEditControl.
ms.assetid: 70450b24-9879-4be8-9bc9-f87008b66415
keywords:
- LVM_GETEDITCONTROL controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_GETEDITCONTROL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29f7e7ac31b3d429ab32ac6564a47f859f0e5dc2207d991cb580173838a4c366
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119968315"
---
# <a name="lvm_geteditcontrol-message"></a>Mensaje \_ GETEDITCONTROL de LVM

Obtiene el identificador del control de edición que se usa para editar el texto de un elemento de vista de lista. Puede enviar este mensaje explícitamente o mediante la macro [**\_ ListView GetEditControl.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_geteditcontrol)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el identificador al control de edición si se realiza correctamente o NULL en **caso** contrario.

## <a name="remarks"></a>Comentarios

Cuando comienza la edición de etiquetas, se crea, coloca e inicializa un control de edición. Antes de que se muestre, el control de vista de lista envía a su ventana primaria un código de [notificación \_ LVN BEGINLABELEDIT.](lvn-beginlabeledit.md)

Para personalizar la edición de etiquetas, implemente un controlador para [LVN \_ BEGINLABELEDIT](lvn-beginlabeledit.md) y haga que envíe un mensaje **\_ GETEDITCONTROL** de LVM al control de vista de lista. Si se está editando una etiqueta, el valor devuelto será un identificador para el control de edición. Use este identificador para personalizar el control de edición mediante el envío de los mensajes **EM \_ XXX habituales.**

Cuando el usuario completa o cancela la edición, el control de edición se destruye y el identificador ya no es válido. Puede crear subclases del control de edición, pero no debe destruirlo. Para cancelar la edición, envíe al control list-view un [**mensaje \_ CANCELMODE de WM.**](/windows/desktop/winmsg/wm-cancelmode)

El elemento de vista de lista que se está editando es el elemento centrado actualmente, es decir, el elemento en estado enfocado. Para buscar un elemento en función de su estado, use el [**mensaje \_ LVM GETNEXTITEM.**](lvm-getnextitem.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ListView \_ GetEditControl**](/windows/desktop/api/Commctrl/nf-commctrl-listview_geteditcontrol)
</dt> </dl>

 

