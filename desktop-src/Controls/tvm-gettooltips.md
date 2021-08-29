---
title: TVM_GETTOOLTIPS mensaje (Commctrl.h)
description: Recupera el identificador del control de información sobre herramientas secundario utilizado por un control de vista de árbol. Puede enviar este mensaje explícitamente o mediante la macro TreeView \_ GetToolTips.
ms.assetid: 65e8189e-ae3e-4268-b1ed-bb0d88f2cbe3
keywords:
- TVM_GETTOOLTIPS controles de Windows mensaje
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
ms.openlocfilehash: 9f0166402c7605139d3e27fce17b94ad0afdffb66622f40da4adc3044b7023d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060175"
---
# <a name="tvm_gettooltips-message"></a>Mensaje \_ GETTOOLTIPS de TVM

Recupera el identificador del control de información sobre herramientas secundario utilizado por un control de vista de árbol. Puede enviar este mensaje explícitamente o mediante la macro [**TreeView \_ GetToolTips.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_gettooltips)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el identificador al control de información sobre herramientas secundario o **NULL** si el control no usa información sobre herramientas.

## <a name="remarks"></a>Comentarios

Cuando se crean, los controles de vista de árbol crean automáticamente un control de información sobre herramientas secundario. Para que un control de vista de árbol no use información sobre herramientas, cree el control con el estilo [**\_ TVS NOTOOLTIPS.**](tree-view-control-window-styles.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TVM \_ SETTOOLTIPS**](tvm-settooltips.md)
</dt> </dl>

 

 





