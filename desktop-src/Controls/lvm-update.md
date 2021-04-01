---
title: Mensaje de LVM_UPDATE (commctrl. h)
description: Actualiza un elemento de vista de lista. Si el control de vista de lista tiene el \_ estilo LVS AutoArrange, esta macro hace que el control de vista de lista esté organizado. Puede enviar este mensaje explícitamente o mediante la macro de \_ actualización de ListView.
ms.assetid: 81b332e9-4bea-481e-a7c5-613371103550
keywords:
- LVM_UPDATE controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905030"
---
# <a name="lvm_update-message"></a>Mensaje de actualización de LVM \_

Actualiza un elemento de vista de lista. Si el control de vista de lista tiene el estilo [**LVS \_ AutoArrange**](list-view-window-styles.md) , esta macro hace que el control de vista de lista esté organizado. Puede enviar este mensaje explícitamente o mediante la macro [**de \_ actualización de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_update) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice del elemento que se va a actualizar.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto, o **false** en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





