---
title: TVM_GETEDITCONTROL mensaje (Commctrl.h)
description: Recupera el identificador del control de edición que se usa para editar el texto de un elemento de vista de árbol. Puede enviar este mensaje explícitamente o mediante la macro \_ TreeView GetEditControl.
ms.assetid: c89e57e8-e113-47a1-85e6-bb68990f9c1a
keywords:
- TVM_GETEDITCONTROL controles de Windows mensaje
topic_type:
- apiref
api_name:
- TVM_GETEDITCONTROL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79b4ce0beb125218e65c2c342caf59b57473088e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165762"
---
# <a name="tvm_geteditcontrol-message"></a>Mensaje \_ GETEDITCONTROL de TVM

Recupera el identificador del control de edición que se usa para editar el texto de un elemento de vista de árbol. Puede enviar este mensaje explícitamente o mediante la macro [**\_ TreeView GetEditControl.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_geteditcontrol)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el identificador al control de edición si se realiza correctamente o **NULL** en caso contrario.

## <a name="remarks"></a>Observaciones

Cuando comienza la edición de etiquetas, se crea un control de edición, pero no se coloca ni se muestra. Antes de que se muestre, el control de vista de árbol envía a su ventana primaria un [código de notificación \_ BEGINLABELEDIT de TVN.](tvn-beginlabeledit.md)

Para personalizar la edición de etiquetas, implemente un controlador para [TVN \_ BEGINLABELEDIT](tvn-beginlabeledit.md) y haga que envíe un mensaje **\_ GETEDITCONTROL** de TVM al control de vista de árbol. Si se edita una etiqueta, el valor devuelto será un identificador del control de edición. Use este identificador para personalizar el control de edición mediante el envío de los mensajes **EM \_ XXX** habituales.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





