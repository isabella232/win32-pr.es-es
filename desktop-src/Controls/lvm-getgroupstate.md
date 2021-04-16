---
title: Mensaje de LVM_GETGROUPSTATE (commctrl. h)
description: Obtiene el estado de un grupo especificado. Envíe este mensaje explícitamente o mediante la \_ macro GetGroupState de ListView.
ms.assetid: f087d17f-9066-44fb-b21b-ac7ceb56eb45
keywords:
- LVM_GETGROUPSTATE controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489268"
---
# <a name="lvm_getgroupstate-message"></a>\_Mensaje GETGROUPSTATE LVM

Obtiene el estado de un grupo especificado. Envíe este mensaje explícitamente o mediante la [**macro \_ GetGroupState de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getgroupstate) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ de\]
</dt> <dd>

Especifica el grupo por **iGroupId** (vea la estructura [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) ).

</dd> <dt>

*lParam* \[ de\]
</dt> <dd>

Especifica los valores de estado que se van a recuperar. Se trata de una combinación de las marcas enumeradas para el miembro de **Estado** de [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve la combinación de valores de estado que se establecen. Por ejemplo, si *lParam* es LVGS \_ contraído y el valor devuelto es cero, el \_ Estado contraído LVGS no se establece. Si no se encuentra el grupo, se devuelve cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





