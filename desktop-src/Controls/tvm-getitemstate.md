---
title: TVM_GETITEMSTATE mensaje (Commctrl.h)
description: Recupera algunos o todos los atributos de estado de un elemento de vista de árbol. Puede enviar este mensaje explícitamente o mediante la macro TreeView \_ GetItemState.
ms.assetid: 89aaaa82-2809-4e4e-a325-5666a57c5cbb
keywords:
- TVM_GETITEMSTATE controles de Windows mensaje
topic_type:
- apiref
api_name:
- TVM_GETITEMSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b851ff3845743c802a2a914a0f40d5d9eb65c6a8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165722"
---
# <a name="tvm_getitemstate-message"></a>Mensaje \_ GETITEMSTATE de TVM

Recupera algunos o todos los atributos de estado de un elemento de vista de árbol. Puede enviar este mensaje explícitamente o mediante la macro [**TreeView \_ GetItemState.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitemstate)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador del elemento.

</dd> <dt>

*lParam* 
</dt> <dd>

Máscara que se usa para especificar los estados que se deben consultar. Es equivalente al miembro **stateMask** de [**TVITEMEX.**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor UINT** con los bits de estado adecuados establecidos en **TRUE.** Solo se establecerán los bits especificados por *lParam* y que sean **TRUE.** Este valor es equivalente al miembro **de** estado de [**TVITEMEX.**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





