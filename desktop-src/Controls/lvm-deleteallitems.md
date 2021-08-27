---
title: LVM_DELETEALLITEMS mensaje (Commctrl.h)
description: Quita todos los elementos de un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la macro \_ ListView DeleteAllItems.
ms.assetid: 816bf565-79e9-4f5d-b5b4-5cdecce8a61c
keywords:
- LVM_DELETEALLITEMS controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_DELETEALLITEMS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c81d2911caee047b63c4a637b6996bc90096e56d337f068beb73fe0fb42b4579
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958414"
---
# <a name="lvm_deleteallitems-message"></a>Mensaje \_ DELETEALLITEMS de LVM

Quita todos los elementos de un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la macro [**\_ ListView DeleteAllItems.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_deleteallitems)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** en caso contrario.

## <a name="remarks"></a>Comentarios

Cuando un control de vista de lista recibe el mensaje **LVM \_ DELETEALLITEMS,** envía el código de [**notificación \_ LVN DELETEALLITEMS**](lvn-deleteallitems.md) a su ventana primaria.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





