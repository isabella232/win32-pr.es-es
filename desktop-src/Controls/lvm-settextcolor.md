---
title: LVM_SETTEXTCOLOR mensaje (Commctrl.h)
description: Establece el color de texto de un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la macro \_ SetTextColor de ListView.
ms.assetid: ff90c18b-0cd7-4331-bcd8-61044e891d1f
keywords:
- LVM_SETTEXTCOLOR controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_SETTEXTCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64b30c965bd523cd5638c894b47fc4785ffbdd09
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362655"
---
# <a name="lvm_settextcolor-message"></a>Mensaje \_ SETTEXTCOLOR de LVM

Establece el color de texto de un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la macro [**\_ SetTextColor de ListView.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settextcolor)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

COLORREF [**que**](/windows/desktop/gdi/colorref) especifica el nuevo color del texto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** de lo contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

