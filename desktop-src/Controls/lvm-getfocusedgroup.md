---
title: LVM_GETFOCUSEDGROUP mensaje (Commctrl.h)
description: Obtiene el grupo que tiene el foco. Envíe este mensaje explícitamente o mediante la \_ macro ListView GetFocusedGroup.
ms.assetid: c1902f35-84b7-4f46-89a6-e48148f06172
keywords:
- LVM_GETFOCUSEDGROUP controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_GETFOCUSEDGROUP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e0d12eb637ec1a421a5eaff58636df7bef8f449
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061852"
---
# <a name="lvm_getfocusedgroup-message"></a>Mensaje \_ GETFOCUSEDGROUP de LVM

Obtiene el grupo que tiene el foco. Envíe este mensaje explícitamente o mediante la macro [**\_ ListView GetFocusedGroup.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfocusedgroup)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el índice del grupo con el estado LVGS FOCUSED, o -1 si no hay ningún grupo con el estado \_ LVGS \_ FOCUSED.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





