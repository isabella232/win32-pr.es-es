---
title: LVM_GETTOOLTIPS mensaje (Commctrl.h)
description: Recupera el control de información sobre herramientas que usa el control de vista de lista para mostrar información sobre herramientas. Puede enviar este mensaje explícitamente o usar la \_ macro ListView GetToolTips.
ms.assetid: a3522c64-9498-40b8-9062-c112b7c8cacc
keywords:
- LVM_GETTOOLTIPS controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6ca4340a8c57c6551d3c46f9324e4b66250f383c9412a3772df3114f105c5f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019293"
---
# <a name="lvm_gettooltips-message"></a>Mensaje \_ GETTOOLTIPS de LVM

Recupera el control de información sobre herramientas que usa el control de vista de lista para mostrar información sobre herramientas. Puede enviar este mensaje explícitamente o usar la macro [**\_ ListView GetToolTips.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gettooltips)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el identificador del control de información sobre herramientas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**LVM \_ SETTOOLTIPS**](lvm-settooltips.md)
</dt> </dl>

 

 





