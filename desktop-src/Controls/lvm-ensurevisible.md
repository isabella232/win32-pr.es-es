---
title: Mensaje de LVM_ENSUREVISIBLE (commctrl. h)
description: Garantiza que un elemento de vista de lista es totalmente o parcialmente visible, desplazando el control de vista de lista si es necesario. Puede enviar este mensaje explícitamente o mediante la \_ macro ensureVisible de ListView.
ms.assetid: 3564b6e6-b8b6-401b-85bc-8bd6261fc054
keywords:
- LVM_ENSUREVISIBLE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_ENSUREVISIBLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d0ff4009399988f20f3e162114f91e4cff02820
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103995941"
---
# <a name="lvm_ensurevisible-message"></a>\_Mensaje ENSUREVISIBLE de LVM

Garantiza que un elemento de vista de lista es totalmente o parcialmente visible, desplazando el control de vista de lista si es necesario. Puede enviar este mensaje explícitamente o mediante la macro [**\_ ensureVisible de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_ensurevisible) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice del elemento de vista de lista.

</dd> <dt>

*lParam* 
</dt> <dd>

Valor que especifica si el elemento debe estar totalmente visible. Si este parámetro es **true**, no se produce ningún desplazamiento si el elemento está al menos parcialmente visible.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto, o **false** en caso contrario.

## <a name="remarks"></a>Observaciones

Se produce un error en el mensaje si el estilo de ventana incluye [**LVS \_ noscroll**](list-view-window-styles.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





