---
title: LVM_UPDATE mensaje (Commctrl.h)
description: Actualiza un elemento de vista de lista. Si el control list-view tiene el estilo LVS AUTOARRANGE, esta macro hace que se ordene el \_ control list-view. Puede enviar este mensaje explícitamente o mediante la macro ListView \_ Update.
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
ms.openlocfilehash: ff9067d6eb80c5db7880ee9331a04e9259e9c841ccfe7dd80158a2afbcd06c99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915235"
---
# <a name="lvm_update-message"></a>Mensaje DE \_ ACTUALIZACIÓN DE LVM

Actualiza un elemento de vista de lista. Si el control list-view tiene el [**estilo LVS \_ AUTOARRANGE,**](list-view-window-styles.md) esta macro hace que se ordene el control list-view. Puede enviar este mensaje explícitamente o mediante la macro [**ListView \_ Update.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_update)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice del elemento que se actualizará.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** de lo contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





