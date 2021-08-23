---
title: LVM_GETGROUPSTATE mensaje (Commctrl.h)
description: Obtiene el estado de un grupo especificado. Envíe este mensaje explícitamente o mediante la \_ macro ListView GetGroupState.
ms.assetid: f087d17f-9066-44fb-b21b-ac7ceb56eb45
keywords:
- LVM_GETGROUPSTATE controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_GETGROUPSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66272dd259e80f239804ffadbd706370f948a2505173cc03aaa40057b273a629
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958434"
---
# <a name="lvm_getgroupstate-message"></a>Mensaje GETGROUPSTATE de LVM \_

Obtiene el estado de un grupo especificado. Envíe este mensaje explícitamente o mediante la macro [**\_ ListView GetGroupState.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getgroupstate)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ En\]
</dt> <dd>

Especifica el grupo por **iGroupId** (vea [**ESTRUCTURA LVGROUP).**](/windows/win32/api/commctrl/ns-commctrl-lvgroup)

</dd> <dt>

*lParam* \[ En\]
</dt> <dd>

Especifica los valores de estado que se recuperarán. Se trata de una combinación de las marcas enumeradas para el miembro **de** estado de [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve la combinación de valores de estado que se establecen. Por ejemplo, si *lParam* es LVGS COLLAPSED y el valor devuelto es cero, no se establece el estado \_ \_ COLLAPSED de LVGS. Se devuelve cero si no se encuentra el grupo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





