---
title: LVM_UPDATE mensaje (Commctrl.h)
description: Actualiza un elemento de vista de lista. Si el control de vista de lista tiene el estilo LVS AUTOARRANGE, esta macro hace que se ordene el \_ control list-view. Puede enviar este mensaje explícitamente o mediante la macro ListView \_ Update.
ms.assetid: 81b332e9-4bea-481e-a7c5-613371103550
keywords:
- LVM_UPDATE controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_UPDATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6cf2a4316e3ae3fc4dbab5e1afe780b03829b30
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362619"
---
# <a name="lvm_update-message"></a>Mensaje LVM \_ UPDATE

Actualiza un elemento de vista de lista. Si el control de vista de lista tiene [**el estilo LVS \_ AUTOARRANGE,**](list-view-window-styles.md) esta macro hace que se ordene el control list-view. Puede enviar este mensaje explícitamente o mediante la macro [**ListView \_ Update.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_update)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice del elemento que se actualizará.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





