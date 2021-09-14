---
title: TVM_SETHOT mensaje (Commctrl.h)
description: Establece el elemento de acceso de acceso de un control de vista de árbol. Puede enviar este mensaje explícitamente o mediante la macro TreeView \_ SetHot.
ms.assetid: 5e7368f5-40ce-4e7b-bbe3-5fe0b17181a8
keywords:
- TVM_SETHOT controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165646"
---
# <a name="tvm_sethot-message"></a>Mensaje \_ SETHOT de TVM

\[Diseñado para uso interno; no se recomienda para su uso en aplicaciones. Es posible que este mensaje no se pueda usar en versiones futuras de Windows.\]

Establece el elemento de acceso de acceso de un control de vista de árbol. Puede enviar este mensaje explícitamente o mediante la macro [**TreeView \_ SetHot.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sethot)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Controle el nuevo elemento de acceso de acceso. Si este valor es **NULL,** el control de vista de árbol se establecerá para que no tenga ningún elemento de acceso.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** de lo contrario.

## <a name="security-considerations"></a>Consideraciones de seguridad

El uso de este mensaje podría poner en peligro la seguridad del programa.

## <a name="remarks"></a>Observaciones

El *elemento de acceso* activa es el elemento sobre el que se mantiene el puntero del mouse. Este mensaje hace que un elemento parezca que es el elemento de acceso activa aunque el mouse no mantenga el puntero sobre él.

Este mensaje no tiene ningún efecto visible si no se establece el estilo [**\_ TRACKSELECT de TVS.**](tree-view-control-window-styles.md)

Si se realiza correctamente, este mensaje hace que se vuelva a dibujar el elemento de acceso.

Este mensaje se omite si *lParam* es **NULL** y el control de vista de árbol está siguiendo el mouse.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TreeView \_ SetHot**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sethot)
</dt> </dl>

 

 





