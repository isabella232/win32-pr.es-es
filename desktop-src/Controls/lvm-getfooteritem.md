---
title: LVM_GETFOOTERITEM mensaje (Commctrl.h)
description: Obtiene información sobre un elemento de pie de página en un control de vista de lista. Envíe este mensaje explícitamente o mediante la \_ macro ListView GetFooterItem.
ms.assetid: 92f55719-c265-433f-84fc-a673680c7ad9
keywords:
- LVM_GETFOOTERITEM controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061851"
---
# <a name="lvm_getfooteritem-message"></a>Mensaje \_ GETFOOTERITEM de LVM

Obtiene información sobre un elemento de pie de página en un control de vista de lista. Envíe este mensaje explícitamente o mediante la macro [**\_ ListView GetFooterItem.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooteritem)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ En\]
</dt> <dd>

Índice del elemento.

</dd> <dt>

*lParam* \[ in, out\]
</dt> <dd>

Puntero a una [**estructura LVFOOTERITEM**](/windows/win32/api/commctrl/ns-commctrl-lvfooteritem) para recibir un valor para los miembros **state** o **pszText** según el valor del miembro **mask.** El proceso de llamada es responsable de asignar esta estructura y establecer sus miembros para indicar al receptor qué información devolver. Para obtener más información, **vea LVFOOTERITEM**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** de lo contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





