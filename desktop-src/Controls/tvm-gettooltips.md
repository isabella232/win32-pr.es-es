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
ms.openlocfilehash: 305aaa05df5b72ffde709e4cf3b3e06d47c43448
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165702"
---
# <a name="tvm_gettooltips-message"></a>Mensaje \_ DE TVM GETTOOLTIPS

Recupera el identificador del control de información sobre herramientas secundario utilizado por un control de vista de árbol. Puede enviar este mensaje explícitamente o mediante la macro [**TreeView \_ GetToolTips.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_gettooltips)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el identificador al control de información sobre herramientas secundario o **NULL** si el control no usa información sobre herramientas.

## <a name="remarks"></a>Observaciones

Cuando se crean, los controles de vista de árbol crean automáticamente un control de información sobre herramientas secundario. Para hacer que un control de vista de árbol no use información sobre herramientas, cree el control con el estilo [**\_ TVS NOTOOLTIPS.**](tree-view-control-window-styles.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TVM \_ SETTOOLTIPS**](tvm-settooltips.md)
</dt> </dl>

 

 





