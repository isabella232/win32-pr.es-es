---
title: Mensaje de TVM_GETITEMSTATE (commctrl. h)
description: Recupera algunos o todos los atributos de estado de un elemento de vista de árbol. Puede enviar este mensaje explícitamente o mediante la \_ macro GetItemState de TreeView.
ms.assetid: 89aaaa82-2809-4e4e-a325-5666a57c5cbb
keywords:
- TVM_GETITEMSTATE controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079552"
---
# <a name="tvm_getitemstate-message"></a>\_Mensaje de GETITEMSTATE TVM

Recupera algunos o todos los atributos de estado de un elemento de vista de árbol. Puede enviar este mensaje explícitamente o mediante la macro [**\_ GetItemState de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitemstate) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador del elemento.

</dd> <dt>

*lParam* 
</dt> <dd>

Máscara que se usa para especificar los Estados que se van a consultar. Es equivalente al miembro **stateMask** de [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **uint** con los bits de estado adecuados establecidos en **true**. Solo se establecerán los bits especificados por *lParam* y que sean **true** . Este valor es equivalente al miembro **State** de [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





