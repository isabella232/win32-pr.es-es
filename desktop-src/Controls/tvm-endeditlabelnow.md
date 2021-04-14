---
title: Mensaje de TVM_ENDEDITLABELNOW (commctrl. h)
description: Finaliza la edición de la etiqueta de un elemento de vista de árbol. Puede enviar este mensaje explícitamente o mediante la \_ macro EndEditLabelNow de TreeView.
ms.assetid: 68de2020-9311-4958-859a-de55f5e41fcf
keywords:
- TVM_ENDEDITLABELNOW controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TVM_ENDEDITLABELNOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f059be20560adeb8cbcb0c63a2555283f6b7051
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533975"
---
# <a name="tvm_endeditlabelnow-message"></a>\_Mensaje de ENDEDITLABELNOW TVM

Finaliza la edición de la etiqueta de un elemento de vista de árbol. Puede enviar este mensaje explícitamente o mediante la macro [**\_ EndEditLabelNow de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_endeditlabelnow) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Variable que indica si la edición se cancela sin guardarse en la etiqueta. Si este parámetro es **true**, el sistema cancela la edición sin guardar los cambios. De lo contrario, el sistema guarda los cambios en la etiqueta.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto, o **false** en caso contrario.

## <a name="remarks"></a>Observaciones

Este mensaje hace que el código de notificación [ \_ ENDLABELEDIT de TVN](tvn-endlabeledit.md) se envíe a la ventana primaria del control de vista de árbol.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





