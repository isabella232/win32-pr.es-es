---
title: TVM_ENSUREVISIBLE mensaje (Commctrl.h)
description: Garantiza que un elemento de vista de árbol está visible, expandiendo el elemento primario o desplazando el control de vista de árbol, si es necesario. Puede enviar este mensaje explícitamente o mediante la macro TreeView \_ EnsureVisible.
ms.assetid: 7053438a-f9ca-4c4c-9da6-46b99fe1e4f8
keywords:
- TVM_ENSUREVISIBLE controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165782"
---
# <a name="tvm_ensurevisible-message"></a>Mensaje \_ ENSUREVISIBLE de TVM

Garantiza que un elemento de vista de árbol está visible, expandiendo el elemento primario o desplazando el control de vista de árbol, si es necesario. Puede enviar este mensaje explícitamente o mediante la macro [**TreeView \_ EnsureVisible.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_ensurevisible)

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

Si el mensaje ENSUREVISIBLE de TVM expande el elemento primario, la ventana primaria recibe los códigos de notificación \_ [TVN \_ ITEMEXPANDING](tvn-itemexpanding.md) y [TVN \_ ITEMEXPANDED.](tvn-itemexpanded.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





