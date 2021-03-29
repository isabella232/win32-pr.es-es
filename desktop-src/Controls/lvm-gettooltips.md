---
title: Mensaje de LVM_GETTOOLTIPS (commctrl. h)
description: Recupera el control de información sobre herramientas que el control de vista de lista utiliza para mostrar la información sobre herramientas. Puede enviar este mensaje explícitamente o utilizar la \_ macro GetToolTips de ListView.
ms.assetid: a3522c64-9498-40b8-9062-c112b7c8cacc
keywords:
- LVM_GETTOOLTIPS controles de mensajes de Windows
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
ms.openlocfilehash: 6f409c85ed6157e8cfc837e5efa3a68488aec504
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492401"
---
# <a name="lvm_gettooltips-message"></a>\_Mensaje GETTOOLTIPS LVM

Recupera el control de información sobre herramientas que el control de vista de lista utiliza para mostrar la información sobre herramientas. Puede enviar este mensaje explícitamente o utilizar la [**macro \_ GetToolTips de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gettooltips) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el identificador del control ToolTip.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_SETTOOLTIPS LVM**](lvm-settooltips.md)
</dt> </dl>

 

 





