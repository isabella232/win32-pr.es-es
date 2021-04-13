---
title: Mensaje de TVM_GETTOOLTIPS (commctrl. h)
description: Recupera el identificador del control de información sobre herramientas secundario utilizado por un control de vista de árbol. Puede enviar este mensaje explícitamente o mediante la \_ macro GetToolTips de TreeView.
ms.assetid: 65e8189e-ae3e-4268-b1ed-bb0d88f2cbe3
keywords:
- TVM_GETTOOLTIPS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TVM_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 305aaa05df5b72ffde709e4cf3b3e06d47c43448
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489790"
---
# <a name="tvm_gettooltips-message"></a>\_Mensaje de GETTOOLTIPS TVM

Recupera el identificador del control de información sobre herramientas secundario utilizado por un control de vista de árbol. Puede enviar este mensaje explícitamente o mediante la macro [**\_ GetToolTips de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_gettooltips) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el identificador del control de información sobre herramientas secundario, o **null** si el control no usa información sobre herramientas.

## <a name="remarks"></a>Observaciones

Cuando se crean, los controles de vista de árbol crean automáticamente un control ToolTip secundario. Para hacer que un control de vista de árbol no use la información sobre herramientas, cree el control con el estilo [**TV \_ notooltips**](tree-view-control-window-styles.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TVM \_ SETTOOLTIPS**](tvm-settooltips.md)
</dt> </dl>

 

 





