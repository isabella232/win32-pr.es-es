---
title: LVM_SETTEXTBKCOLOR mensaje (Commctrl.h)
description: Establece el color de fondo del texto en un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la macro \_ SetTextBkColor de ListView.
ms.assetid: e51d6914-0e98-47f8-b2d8-4c2404b98242
keywords:
- LVM_SETTEXTBKCOLOR controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_SETTEXTBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d9acdc193609f39fb81aa88263724a507695f15dcb8ba0c789df5c2a4f4d128
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119656235"
---
# <a name="lvm_settextbkcolor-message"></a>Mensaje \_ LVM SETTEXTBKCOLOR

Establece el color de fondo del texto en un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la macro [**\_ SetTextBkColor de ListView.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settextbkcolor)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Nuevo color de fondo de texto. Puede ser CLR \_ NONE sin color de fondo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** de lo contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





