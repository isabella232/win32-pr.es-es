---
title: Mensaje de TVM_EDITLABEL (commctrl. h)
description: Comienza la edición en contexto del texto del elemento especificado y reemplaza el texto del elemento por un control de edición de una sola línea que contiene el texto.
ms.assetid: ae844cbf-fa43-4f91-90cc-688f44bf77a5
keywords:
- TVM_EDITLABEL controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TVM_EDITLABEL
- TVM_EDITLABELA
- TVM_EDITLABELW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3608c3f959c45571d9bc085518b763cf505180ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996206"
---
# <a name="tvm_editlabel-message"></a>\_Mensaje de EDITLABEL TVM

Comienza la edición en contexto del texto del elemento especificado y reemplaza el texto del elemento por un control de edición de una sola línea que contiene el texto. Este mensaje selecciona implícitamente y se centra en el elemento especificado. Puede enviar este mensaje explícitamente o mediante la macro [**\_ EditLabel de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_editlabel) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Identificador del elemento que se va a editar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el identificador del control de edición que se usa para editar el texto del elemento si se realiza correctamente, o **null** en caso contrario.

## <a name="remarks"></a>Observaciones

Este mensaje envía un código de notificación de [TVN \_ BEGINLABELEDIT](tvn-beginlabeledit.md) al elemento primario del control de vista de árbol.

Cuando el usuario finaliza o cancela la edición, el control de edición se destruye y el identificador ya no es válido. Puede crear subclases del control de edición, pero no destruirlo.

El control debe tener el foco antes de enviar este mensaje al control. El foco se puede establecer mediante la función [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **TVM \_ EDITLABELW** (Unicode) y **TVM \_ EDITLABELA** (ANSI)<br/>               |



 

