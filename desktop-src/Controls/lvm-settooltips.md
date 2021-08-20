---
title: LVM_SETTOOLTIPS mensaje (Commctrl.h)
description: Establece el control de información sobre herramientas que usará el control de vista de lista para mostrar información sobre herramientas. Puede enviar este mensaje explícitamente o usar la \_ macro ListView SetToolTips.
ms.assetid: 5b4335a4-e9f0-4b13-b00b-516af3b60bf1
keywords:
- LVM_SETTOOLTIPS controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_SETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bf2256d94630b8e792fd1f148864f3588b27e73ea5781eb0bdcd24bf9571507
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118170401"
---
# <a name="lvm_settooltips-message"></a>Mensaje \_ DE LVM SETTOOLTIPS

Establece el control de información sobre herramientas que usará el control de vista de lista para mostrar información sobre herramientas. Puede enviar este mensaje explícitamente o usar la macro [**\_ ListView SetToolTips.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settooltips)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Identificador del control de información sobre herramientas que se va a establecer.</dd> <dt>

*lParam* 
</dt> <dd>

Debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el identificador al control de información sobre herramientas anterior.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**LVM \_ GETTOOLTIPS**](lvm-gettooltips.md)
</dt> </dl>

 

 





