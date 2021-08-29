---
title: LVM_GETVIEWRECT mensaje (Commctrl.h)
description: Recupera el rectángulo delimitador de todos los elementos del control de vista de lista. La vista de lista debe estar en la vista de icono o icono pequeño. Puede enviar este mensaje explícitamente o mediante la macro \_ ListView GetViewRect.
ms.assetid: 69b96f86-8b7e-42c1-ad73-f9b2732ab9f9
keywords:
- LVM_GETVIEWRECT controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_GETVIEWRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4de840c68af1abb9fd5a79e93318d984b64b295f5431317330bf03f0e34e44ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062365"
---
# <a name="lvm_getviewrect-message"></a>Mensaje \_ GETVIEWRECT de LVM

Recupera el rectángulo delimitador de todos los elementos del control de vista de lista. La vista de lista debe estar en la vista de icono o icono pequeño. Puede enviar este mensaje explícitamente o mediante la macro [**\_ ListView GetViewRect.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getviewrect)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura RECT**](/previous-versions//dd162897(v=vs.85)) que recibe el rectángulo delimitador. Todas las coordenadas son relativas al área visible del control list-view.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

