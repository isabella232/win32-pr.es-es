---
title: TVM_SETINSERTMARK mensaje (Commctrl.h)
description: Establece la marca de inserción en un control de vista de árbol. Puede enviar este mensaje explícitamente o mediante la macro \_ SetInsertMark de TreeView.
ms.assetid: 35441807-406a-408c-ad89-6dd40c907e3c
keywords:
- TVM_SETINSERTMARK controles de Windows mensaje
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
ms.openlocfilehash: 0c3004395dcc7ea0b83af2fc2b7dae370c303228f79599215d5b6d264379b793
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119875635"
---
# <a name="tvm_setinsertmark-message"></a>Mensaje \_ DE TVM SETINSERTMARK

Establece la marca de inserción en un control de vista de árbol. Puede enviar este mensaje explícitamente o mediante la macro [**\_ SetInsertMark de TreeView.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setinsertmark)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

**Valor BOOL** que especifica si la marca de inserción se coloca antes o después del elemento especificado. Si este argumento es distinto de cero, la marca de inserción se colocará después del elemento. Si este argumento es cero, la marca de inserción se colocará delante del elemento.

</dd> <dt>

*lParam* 
</dt> <dd>

**HTREEITEM que** especifica en qué elemento se colocará la marca de inserción. Si este argumento es **NULL,** se quita la marca de inserción.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si se realiza correctamente o cero en caso contrario.

## <a name="remarks"></a>Comentarios

En algunas circunstancias, la marca de inserción puede aparecer en dos lugares después de expandir un nodo. Si usa marcas de inserción, se recomienda forzar una actualización del control después de expandir un nodo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





