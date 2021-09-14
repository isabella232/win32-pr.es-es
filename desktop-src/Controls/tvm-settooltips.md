---
title: TVM_SETTOOLTIPS mensaje (Commctrl.h)
description: Establece el control de información sobre herramientas secundario de un control de vista de árbol. Puede enviar este mensaje explícitamente o mediante la macro TreeView \_ SetToolTips.
ms.assetid: beb9a739-868e-46a8-95d9-9dc032c79dd4
keywords:
- TVM_SETTOOLTIPS controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165609"
---
# <a name="tvm_settooltips-message"></a>Mensaje \_ SETTOOLTIPS de TVM

Establece el control de información sobre herramientas secundario de un control de vista de árbol. Puede enviar este mensaje explícitamente o mediante la macro [**TreeView \_ SetToolTips.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_settooltips)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de un control de información sobre herramientas.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el identificador al control de información sobre herramientas establecido anteriormente para el control de vista de árbol, o **NULL** si no se usó anteriormente la información sobre herramientas.

## <a name="remarks"></a>Observaciones

Cuando se crean, los controles de vista de árbol crean automáticamente un control de información sobre herramientas secundario. Para evitar que un control de vista de árbol use información sobre herramientas, cree el control con el estilo [**\_ TVS NOTOOLTIPS.**](tree-view-control-window-styles.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TVM \_ GETTOOLTIPS**](tvm-gettooltips.md)
</dt> </dl>

 

 





