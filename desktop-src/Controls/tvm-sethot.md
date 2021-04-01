---
title: Mensaje de TVM_SETHOT (commctrl. h)
description: Establece el elemento activo para un control de vista de árbol. Puede enviar este mensaje explícitamente o mediante la macro TreeView \_ SetHot.
ms.assetid: 5e7368f5-40ce-4e7b-bbe3-5fe0b17181a8
keywords:
- TVM_SETHOT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TVM_SETHOT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: beccd5429267350682a6721cde66cca9316cf438
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996960"
---
# <a name="tvm_sethot-message"></a>\_Mensaje TVM SETHOT

\[Diseñado para uso interno; no se recomienda para su uso en aplicaciones de. Es posible que este mensaje no se admita en versiones futuras de Windows.\]

Establece el elemento activo para un control de vista de árbol. Puede enviar este mensaje explícitamente o mediante la macro [**TreeView \_ SetHot**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sethot) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador del nuevo elemento activo. Si este valor es **null**, el control de vista de árbol se establecerá en no tener ningún elemento activo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto, o **false** en caso contrario.

## <a name="security-considerations"></a>Consideraciones sobre la seguridad

El uso de este mensaje podría poner en peligro la seguridad del programa.

## <a name="remarks"></a>Observaciones

El *elemento activo* es el elemento sobre el que se mantiene el mouse. Este mensaje hace que un elemento parezca que es el elemento activo, incluso si el mouse no se mantiene sobre él.

Este mensaje no tiene ningún efecto visible si no se establece el estilo [**\_ TRACKSELECT de los televisores**](tree-view-control-window-styles.md) .

Si se realiza correctamente, este mensaje hace que el elemento activo se vuelva a dibujar.

Este mensaje se omite si *lParam* es **null** y el control de vista de árbol está realizando el seguimiento del mouse.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Vista de árbol \_ SetHot**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sethot)
</dt> </dl>

 

 





