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
ms.openlocfilehash: 17b5bb25fd517816afd04bb700211222e6985f5d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061837"
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
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





