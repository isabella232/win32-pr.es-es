---
title: Mensaje de LVM_SETTOOLTIPS (commctrl. h)
description: Establece el control de información sobre herramientas que el control de vista de lista usará para mostrar la información sobre herramientas. Puede enviar este mensaje explícitamente o utilizar la \_ macro SetToolTips de ListView.
ms.assetid: 5b4335a4-e9f0-4b13-b00b-516af3b60bf1
keywords:
- LVM_SETTOOLTIPS controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489965"
---
# <a name="lvm_settooltips-message"></a>\_Mensaje SETTOOLTIPS LVM

Establece el control de información sobre herramientas que el control de vista de lista usará para mostrar la información sobre herramientas. Puede enviar este mensaje explícitamente o utilizar la [**macro \_ SetToolTips de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settooltips) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Identificador del control de información sobre herramientas que se va a establecer.</dd> <dt>

*lParam* 
</dt> <dd>

Debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el identificador del control de información sobre herramientas anterior.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_GETTOOLTIPS LVM**](lvm-gettooltips.md)
</dt> </dl>

 

 





