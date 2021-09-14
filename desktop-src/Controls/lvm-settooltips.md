---
title: LVM_SETTOOLTIPS mensaje (Commctrl.h)
description: Establece el control de información sobre herramientas que usará el control de vista de lista para mostrar información sobre herramientas. Puede enviar este mensaje explícitamente o usar la macro ListView \_ SetToolTips.
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
ms.openlocfilehash: 4ff749c24a35cf73de2d75b8a3b516197b57aac4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362651"
---
# <a name="lvm_settooltips-message"></a>Mensaje \_ SETTOOLTIPS de LVM

Establece el control de información sobre herramientas que usará el control de vista de lista para mostrar información sobre herramientas. Puede enviar este mensaje explícitamente o usar la macro [**ListView \_ SetToolTips.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settooltips)

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



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**LVM \_ GETTOOLTIPS**](lvm-gettooltips.md)
</dt> </dl>

 

 





