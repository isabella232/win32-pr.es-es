---
title: Mensaje de TVM_GETEDITCONTROL (commctrl. h)
description: Recupera el identificador del control de edición que se usa para editar el texto de un elemento de la vista de árbol. Puede enviar este mensaje explícitamente o mediante la \_ macro GetEditControl de TreeView.
ms.assetid: c89e57e8-e113-47a1-85e6-bb68990f9c1a
keywords:
- TVM_GETEDITCONTROL controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151046"
---
# <a name="tvm_geteditcontrol-message"></a>\_Mensaje de GETEDITCONTROL TVM

Recupera el identificador del control de edición que se usa para editar el texto de un elemento de la vista de árbol. Puede enviar este mensaje explícitamente o mediante la macro [**\_ GetEditControl de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_geteditcontrol) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el identificador del control de edición si se realiza correctamente, o **null** en caso contrario.

## <a name="remarks"></a>Observaciones

Cuando comienza la edición de etiquetas, se crea un control de edición, pero no se coloca ni se muestra. Antes de que se muestre, el control de vista de árbol envía a su ventana primaria un código de notificación [TVN \_ BEGINLABELEDIT](tvn-beginlabeledit.md) .

Para personalizar la edición de etiquetas, implemente un controlador para [TVN \_ BEGINLABELEDIT](tvn-beginlabeledit.md) y envíe un mensaje **TVM \_ GETEDITCONTROL** al control de vista de árbol. Si se está editando una etiqueta, el valor devuelto será un identificador del control de edición. Use este identificador para personalizar el control de edición mediante el envío de los mensajes de **em \_ XXX** habituales.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





