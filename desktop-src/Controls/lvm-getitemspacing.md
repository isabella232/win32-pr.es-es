---
title: LVM_GETITEMSPACING mensaje (Commctrl.h)
description: Determina el espaciado entre los elementos de un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la macro \_ ListView GetItemSpacing.
ms.assetid: 4e43fb43-468c-4b8a-9e3b-1694e90ffef8
keywords:
- LVM_GETITEMSPACING controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_GETITEMSPACING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 687a1aa75d71b96cebe855bb97ea57f0a9c628ed49b1ef7a51a7557b23b5ce41
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088895"
---
# <a name="lvm_getitemspacing-message"></a>Mensaje \_ LVM GETITEMSPACING

Determina el espaciado entre los elementos de un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la macro [**\_ ListView GetItemSpacing.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemspacing)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Vista para la que se va a recuperar el espaciado de elementos. Este parámetro es **TRUE para** la vista de iconos pequeño o **FALSE para** la vista de iconos.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve la cantidad de espaciado entre los elementos. El espaciado horizontal se encuentra en [**loword**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) y el espaciado vertical se encuentra en [**hiword**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

