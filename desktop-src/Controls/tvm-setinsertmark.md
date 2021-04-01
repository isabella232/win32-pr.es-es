---
title: Mensaje de TVM_SETINSERTMARK (commctrl. h)
description: Establece la marca de inserción en un control de vista de árbol. Puede enviar este mensaje explícitamente o mediante la \_ macro SetInsertMark de TreeView.
ms.assetid: 35441807-406a-408c-ad89-6dd40c907e3c
keywords:
- TVM_SETINSERTMARK controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TVM_SETINSERTMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff5a9cc9b05e9cd7dc3281d778734bee1048ffd2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905348"
---
# <a name="tvm_setinsertmark-message"></a>\_Mensaje de SETINSERTMARK TVM

Establece la marca de inserción en un control de vista de árbol. Puede enviar este mensaje explícitamente o mediante la macro [**\_ SetInsertMark de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setinsertmark) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor **booleano** que especifica si la marca de inserción se coloca antes o después del elemento especificado. Si este argumento es distinto de cero, la marca de inserción se colocará después del elemento. Si este argumento es cero, la marca de inserción se colocará delante del elemento.

</dd> <dt>

*lParam* 
</dt> <dd>

**HTREEITEM** que especifica en qué elemento se colocará la marca de inserción. Si este argumento es **null**, se quita la marca de inserción.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si es correcto o cero de lo contrario.

## <a name="remarks"></a>Observaciones

En algunas circunstancias, la marca de inserción puede aparecer en dos lugares después de expandir un nodo. Si usa marcas de inserción, se recomienda forzar una actualización del control después de expandir un nodo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





