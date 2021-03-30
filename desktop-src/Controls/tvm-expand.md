---
title: Mensaje de TVM_EXPAND (commctrl. h)
description: El \_ mensaje TVM expand expande o contrae la lista de elementos secundarios asociada al elemento primario especificado, si existe. Puede enviar este mensaje explícitamente o mediante la \_ macro Expand de TreeView.
ms.assetid: d6c2e5b2-ce36-4c2b-b527-91c6de56e305
keywords:
- TVM_EXPAND controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492377"
---
# <a name="tvm_expand-message"></a>\_Mensaje de expansión TVM

El mensaje **TVM \_ Expand** expande o contrae la lista de elementos secundarios asociada al elemento primario especificado, si existe. Puede enviar este mensaje explícitamente o mediante la macro [**\_ Expand de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_expand) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Marca de acción. Este parámetro puede ser uno o varios de los siguientes valores:



| Value                                                                                                                                                                     | Significado                                                                                                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TVE_COLLAPSE"></span><span id="tve_collapse"></span><dl> <dt>**TVE \_ contraer**</dt> </dl>                | Contrae la lista. <br/>                                                                                                                                                                                                                                                       |
| <span id="TVE_COLLAPSERESET"></span><span id="tve_collapsereset"></span><dl> <dt>**TVE \_ COLLAPSERESET**</dt> </dl> | Contrae la lista y quita los elementos secundarios. Se restablece la marca de estado [**TVIS \_ EXPANDEDONCE**](tree-view-control-item-states.md) . Esta marca debe usarse con la \_ marca de contraer TVE.<br/>                                                                 |
| <span id="TVE_EXPAND"></span><span id="tve_expand"></span><dl> <dt>**TVE \_ expandir**</dt> </dl>                      | Expande la lista.<br/>                                                                                                                                                                                                                                                          |
| <span id="TVE_EXPANDPARTIAL"></span><span id="tve_expandpartial"></span><dl> <dt>**TVE \_ EXPANDPARTIAL**</dt> </dl> | [Versión 4,70](common-control-versions.md). Expande parcialmente la lista. En este estado, los elementos secundarios son visibles y se muestra el signo más (+) del elemento primario, que indica que se puede expandir. Esta marca se debe usar en combinación con la \_ marca de expansión TVE.<br/> |
| <span id="TVE_TOGGLE"></span><span id="tve_toggle"></span><dl> <dt>**TVE \_ alternar**</dt> </dl>                      | Contrae la lista si está expandida o la expande si está contraída.<br/>                                                                                                                                                                                                     |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador del elemento primario que se va a expandir o contraer.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si la operación se realizó correctamente o cero en caso contrario.

## <a name="remarks"></a>Observaciones

La expansión de un nodo que ya se ha expandido se considera una operación correcta y [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) devuelve un valor distinto de cero. Al contraer un nodo, se devuelve cero si el nodo ya está contraído; en caso contrario, devuelve un valor distinto de cero. El intento de expandir o contraer un nodo que no tiene elementos secundarios se considera un error y **SendMessage** devuelve cero.

Cuando se expande un elemento por primera vez mediante un mensaje de **\_ expansión TVM** , la acción genera los códigos de notificación [TVN \_ ITEMEXPANDING](tvn-itemexpanding.md) y [TVN \_ ITEMEXPANDED](tvn-itemexpanded.md) y se establece la marca de estado [**TVIS \_**](tree-view-control-item-states.md) EXPANDEDONCE del elemento. Siempre y cuando esta marca de estado permanezca establecida, los mensajes de **\_ expansión TVM** posteriores no generarán \_ notificaciones de TVN ITEMEXPANDING o TVN \_ ITEMEXPANDED. Para restablecer la marca de estado **TVIS \_ EXPANDEDONCE** , debe enviar un mensaje **TVM \_ Expand** con las \_ marcas TVE Collapse y TVE \_ COLLAPSERESET establecidas. Al intentar establecer explícitamente **TVIS \_ EXPANDEDONCE** , se producirá un comportamiento imprevisible.

Se puede producir un error en la operación de expansión si el propietario del control TreeView deniega la operación en respuesta a una notificación [ \_ ITEMEXPANDING de TVN](tvn-itemexpanding.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

