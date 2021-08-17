---
title: LVM_ISITEMVISIBLE mensaje (Commctrl.h)
description: Indica si un elemento del control list-view está visible. Envíe este mensaje explícitamente o mediante la macro \_ ListView IsItemVisible.
ms.assetid: 355be527-e2b9-46be-96a0-951d72216d92
keywords:
- LVM_ISITEMVISIBLE controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_ISITEMVISIBLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 424d321b79b4a4f497942c36ca78c751cc5404cdfaf965b451eea94a8b3c8e1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958184"
---
# <a name="lvm_isitemvisible-message"></a>Mensaje \_ DE LVM ISITEMVISIBLE

Indica si un elemento del control list-view está visible. Envíe este mensaje explícitamente o mediante la macro [**\_ ListView IsItemVisible.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_isitemvisible)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ En\]
</dt> <dd>

Índice del elemento en el control list-view.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** está visible o **FALSE** en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





