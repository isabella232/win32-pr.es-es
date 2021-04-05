---
title: Mensaje de LVM_GETFOOTERITEM (commctrl. h)
description: Obtiene información sobre un elemento de pie de página en un control de vista de lista. Envíe este mensaje explícitamente o mediante la \_ macro GetFooterItem de ListView.
ms.assetid: 92f55719-c265-433f-84fc-a673680c7ad9
keywords:
- LVM_GETFOOTERITEM controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_GETFOOTERITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e642c9d853ae11edcd9199e48de61592de4883c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078864"
---
# <a name="lvm_getfooteritem-message"></a>\_Mensaje GETFOOTERITEM LVM

Obtiene información sobre un elemento de pie de página en un control de vista de lista. Envíe este mensaje explícitamente o mediante la [**macro \_ GetFooterItem de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooteritem) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ de\]
</dt> <dd>

Índice del elemento.

</dd> <dt>

*lParam* \[ in, out\]
</dt> <dd>

Un puntero a una estructura [**LVFOOTERITEM**](/windows/win32/api/commctrl/ns-commctrl-lvfooteritem) para recibir un valor para los miembros **State** y/o **miembros pszText** según el valor del miembro **Mask** . El proceso de llamada es responsable de asignar esta estructura y establecer sus miembros para indicar al receptor qué información se debe devolver. Para obtener más información, vea **LVFOOTERITEM**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto, o **false** en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





