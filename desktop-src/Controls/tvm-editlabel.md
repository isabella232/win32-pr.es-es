---
title: TVM_EDITLABEL mensaje (Commctrl.h)
description: Comienza la edición en contexto del texto del elemento especificado, reemplazando el texto del elemento por un control de edición de una sola línea que contiene el texto.
ms.assetid: ae844cbf-fa43-4f91-90cc-688f44bf77a5
keywords:
- TVM_EDITLABEL controles de Windows mensaje
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
ms.openlocfilehash: 87ba9f9d0af4d6afb3c454f5e5477ccd67728bdec7f378b0f0a04adc901ba322
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118408592"
---
# <a name="tvm_editlabel-message"></a>Mensaje \_ EDITLABEL de TVM

Comienza la edición en contexto del texto del elemento especificado, reemplazando el texto del elemento por un control de edición de una sola línea que contiene el texto. Este mensaje selecciona y centra implícitamente el elemento especificado. Puede enviar este mensaje explícitamente o mediante la macro [**TreeView \_ EditLabel.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_editlabel)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Controle el elemento que se editará.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el identificador al control de edición utilizado para editar el texto del elemento si se realiza correctamente o **NULL en caso** contrario.

## <a name="remarks"></a>Comentarios

Este mensaje envía un [código de notificación \_ BEGINLABELEDIT](tvn-beginlabeledit.md) de TVN al elemento primario del control de vista de árbol.

Cuando el usuario completa o cancela la edición, el control de edición se destruye y el identificador ya no es válido. Puede crear subclases del control de edición, pero no destruirlo.

El control debe tener el foco antes de enviar este mensaje al control. El foco se puede establecer mediante la [**función SetFocus.**](/windows/desktop/api/winuser/nf-winuser-setfocus)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **TVM \_ EDITLABELW** (Unicode) y **TVM \_ EDITLABELA** (ANSI)<br/>               |



 

