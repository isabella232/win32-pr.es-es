---
title: Mensaje de TVM_SETTOOLTIPS (commctrl. h)
description: Establece un control de información sobre herramientas secundario del control de vista de árbol. Puede enviar este mensaje explícitamente o mediante la \_ macro SetToolTips de TreeView.
ms.assetid: beb9a739-868e-46a8-95d9-9dc032c79dd4
keywords:
- TVM_SETTOOLTIPS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TVM_SETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efd9d5957a38d873993405a5283545472433e958
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150265"
---
# <a name="tvm_settooltips-message"></a>\_Mensaje de SETTOOLTIPS TVM

Establece un control de información sobre herramientas secundario del control de vista de árbol. Puede enviar este mensaje explícitamente o mediante la macro [**\_ SetToolTips de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_settooltips) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de un control de información sobre herramientas.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el identificador del control de información sobre herramientas previamente establecido para el control de vista de árbol o **null** si no se ha usado anteriormente la información sobre herramientas.

## <a name="remarks"></a>Observaciones

Cuando se crean, los controles de vista de árbol crean automáticamente un control ToolTip secundario. Para evitar que un control de vista de árbol use la información sobre herramientas, cree el control con el estilo [**TV \_ notooltips**](tree-view-control-window-styles.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TVM \_ GETTOOLTIPS**](tvm-gettooltips.md)
</dt> </dl>

 

 





