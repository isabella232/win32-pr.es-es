---
title: TVM_ENDEDITLABELNOW mensaje (Commctrl.h)
description: Finaliza la edición de la etiqueta de un elemento de vista de árbol. Puede enviar este mensaje explícitamente o mediante la macro TreeView \_ EndEditLabelNow.
ms.assetid: 68de2020-9311-4958-859a-de55f5e41fcf
keywords:
- TVM_ENDEDITLABELNOW controles de Windows mensaje
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
ms.openlocfilehash: 18355edc8efb18ea56a39e60c68361a7ef8d72e39af644707d6d102738fd60c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119387265"
---
# <a name="tvm_endeditlabelnow-message"></a>Mensaje \_ DE TVM ENDEDITLABELNOW

Finaliza la edición de la etiqueta de un elemento de vista de árbol. Puede enviar este mensaje explícitamente o mediante la macro [**TreeView \_ EndEditLabelNow.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_endeditlabelnow)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Variable que indica si la edición se cancela sin guardarse en la etiqueta. Si este parámetro es **TRUE,** el sistema cancela la edición sin guardar los cambios. De lo contrario, el sistema guarda los cambios en la etiqueta.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** de lo contrario.

## <a name="remarks"></a>Comentarios

Este mensaje hace que el [código de notificación \_ ENDLABELEDIT](tvn-endlabeledit.md) de TVN se envíe a la ventana primaria del control de vista de árbol.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





