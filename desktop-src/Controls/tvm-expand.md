---
title: TVM_EXPAND mensaje (Commctrl.h)
description: El mensaje EXPAND de TVM expande o contrae la lista de elementos secundarios asociados al \_ elemento primario especificado, si los hay. Puede enviar este mensaje explícitamente o mediante la macro TreeView \_ Expand.
ms.assetid: d6c2e5b2-ce36-4c2b-b527-91c6de56e305
keywords:
- TVM_EXPAND controles de Windows mensaje
topic_type:
- apiref
api_name:
- TVM_EXPAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14d5cd7577c6f4581865569c3aefca93f13aa305
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165770"
---
# <a name="tvm_expand-message"></a>Mensaje \_ DE EXPANSIÓN DE TVM

El **mensaje EXPAND \_ de TVM** expande o contrae la lista de elementos secundarios asociados al elemento primario especificado, si los hay. Puede enviar este mensaje explícitamente o mediante la macro [**TreeView \_ Expand.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_expand)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Marca de acción. Este parámetro puede ser uno o varios de los valores siguientes:



| Value                                                                                                                                                                     | Significado                                                                                                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TVE_COLLAPSE"></span><span id="tve_collapse"></span><dl> <dt>**TVE \_ COLLAPSE**</dt> </dl>                | Contrae la lista. <br/>                                                                                                                                                                                                                                                       |
| <span id="TVE_COLLAPSERESET"></span><span id="tve_collapsereset"></span><dl> <dt>**TVE \_ COLLAPSERESET**</dt> </dl> | Contrae la lista y quita los elementos secundarios. Se restablece la marca de estado [**\_ TVIS EXPANDEDONCE.**](tree-view-control-item-states.md) Esta marca debe usarse con la marca \_ COLLAPSE de TVE.<br/>                                                                 |
| <span id="TVE_EXPAND"></span><span id="tve_expand"></span><dl> <dt>**TVE \_ EXPAND**</dt> </dl>                      | Expande la lista.<br/>                                                                                                                                                                                                                                                          |
| <span id="TVE_EXPANDPARTIAL"></span><span id="tve_expandpartial"></span><dl> <dt>**TVE \_ EXPANDPARTIAL**</dt> </dl> | [Versión 4.70.](common-control-versions.md) Expande parcialmente la lista. En este estado, los elementos secundarios están visibles y se muestra el signo más (+) del elemento primario, que indica que se puede expandir. Esta marca debe usarse en combinación con la marca \_ EXPAND de TVE.<br/> |
| <span id="TVE_TOGGLE"></span><span id="tve_toggle"></span><dl> <dt>**ALTERNANCIA DE TVE \_**</dt> </dl>                      | Contrae la lista si se expande o la expande si está contraida.<br/>                                                                                                                                                                                                     |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador del elemento primario que se expandirá o contraerá.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si la operación se ha realizado correctamente o cero en caso contrario.

## <a name="remarks"></a>Observaciones

La expansión de un nodo que ya está expandido se considera una operación correcta y [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) devuelve un valor distinto de cero. Al contraer un nodo, se devuelve cero si el nodo ya está contraído; de lo contrario, devuelve un valor distinto de cero. El intento de expandir o contraer un nodo que no tiene ningún nodo secundario se considera un error y **SendMessage** devuelve cero.

Cuando un elemento se expande por primera vez mediante un mensaje EXPAND de **TVM, \_** la acción genera los códigos de notificación [TVN \_ ITEMEXPANDING](tvn-itemexpanding.md) y [TVN \_ ITEMEXPANDED](tvn-itemexpanded.md) y se establece la marca de estado [**TVIS \_ EXPANDEDONCE**](tree-view-control-item-states.md) del elemento. Mientras esta marca de estado permanezca establecida, los mensajes EXPAND de **\_ TVM** subsiguientes no generarán notificaciones \_ ITEMEXPANDING de TVN o \_ ITEMEXPANDED de TVN. Para restablecer la marca de estado **TVIS \_ EXPANDEDONCE,** debe enviar un mensaje **\_ TVM EXPAND** con las marcas TVE COLLAPSE y \_ TVE \_ COLLAPSERESET establecidas. Si se intenta establecer explícitamente **TVIS \_ EXPANDEDONCE,** se provocará un comportamiento impredecible.

La operación de expansión puede producir un error si el propietario del control treeview deniega la operación en respuesta a una [notificación \_ ITEMEXPANDING de TVN.](tvn-itemexpanding.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

