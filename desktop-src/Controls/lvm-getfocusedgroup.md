---
title: LVM_GETFOCUSEDGROUP mensaje (Commctrl.h)
description: Obtiene el grupo que tiene el foco. Envíe este mensaje explícitamente o mediante la macro \_ ListView GetFocusedGroup.
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
ms.openlocfilehash: f9b253405683c058518706e92e62f09041ae4db0e4bee426aa653103bda2188c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877435"
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

Devuelve el índice del grupo con el estado LVGS FOCUSED o -1 si no hay ningún grupo con el estado \_ LVGS \_ FOCUSED.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





