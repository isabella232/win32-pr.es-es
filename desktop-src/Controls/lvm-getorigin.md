---
title: LVM_GETORIGIN mensaje (Commctrl.h)
description: Recupera el origen de vista actual para un control list-view. Puede enviar este mensaje explícitamente o mediante la macro \_ ListView GetOrigin.
ms.assetid: 913c8339-fbe4-43c8-a997-5a972920dc3b
keywords:
- LVM_GETORIGIN controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_GETORIGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a274e81c276d70eb1ab6c7f214b62ae5c346a59dda026bb13c5ab6b3ce80f68d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118411362"
---
# <a name="lvm_getorigin-message"></a>Mensaje \_ GETORIGIN de LVM

Recupera el origen de vista actual para un control list-view. Puede enviar este mensaje explícitamente o mediante la macro [**\_ ListView GetOrigin.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getorigin)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura POINT**](/previous-versions//dd162805(v=vs.85)) que recibe el origen de la vista.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** si la vista actual es de lista o vista de informe.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

