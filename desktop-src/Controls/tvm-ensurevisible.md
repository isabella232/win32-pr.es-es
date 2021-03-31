---
title: Mensaje de TVM_ENSUREVISIBLE (commctrl. h)
description: Garantiza que un elemento de vista de árbol está visible, expandiendo el elemento primario o desplazándose por el control de vista de árbol, si es necesario. Puede enviar este mensaje explícitamente o mediante la \_ macro ensureVisible de TreeView.
ms.assetid: 7053438a-f9ca-4c4c-9da6-46b99fe1e4f8
keywords:
- TVM_ENSUREVISIBLE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TVM_ENSUREVISIBLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06100ee33106736076608aa216d2aebc03b76ebe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996205"
---
# <a name="tvm_ensurevisible-message"></a>Mensaje de la \_ ENSUREVISIBLE TVM

Garantiza que un elemento de vista de árbol está visible, expandiendo el elemento primario o desplazándose por el control de vista de árbol, si es necesario. Puede enviar este mensaje explícitamente o mediante la macro [**\_ ensureVisible de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_ensurevisible) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Identificador del elemento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si el sistema desplazó los elementos del control de vista de árbol y no se expandió ningún elemento. De lo contrario, el mensaje devuelve cero.

## <a name="remarks"></a>Observaciones

Si el mensaje de la \_ ENSUREVISIBLE TVM expande el elemento primario, la ventana primaria recibe los códigos de notificación [TVN \_ ITEMEXPANDING](tvn-itemexpanding.md) y [TVN \_ ITEMEXPANDED](tvn-itemexpanded.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





