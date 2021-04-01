---
title: Mensaje de LVM_GETITEMSPACING (commctrl. h)
description: Determina el espaciado entre los elementos de un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la \_ macro GetItemSpacing de ListView.
ms.assetid: 4e43fb43-468c-4b8a-9e3b-1694e90ffef8
keywords:
- LVM_GETITEMSPACING controles de mensajes de Windows
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
ms.openlocfilehash: 5ea08a7fc1004ffb46d710da6d1c2a8b0fb18e57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996914"
---
# <a name="lvm_getitemspacing-message"></a>\_Mensaje GETITEMSPACING LVM

Determina el espaciado entre los elementos de un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la macro [**\_ GetItemSpacing de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemspacing) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Vista para la que se va a recuperar el espaciado del elemento. Este parámetro es **true** para la vista de iconos pequeños o **false** para la vista de iconos.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve la cantidad de espaciado entre los elementos. El espaciado horizontal está contenido en el [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) y el espaciado vertical está incluido en el [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

