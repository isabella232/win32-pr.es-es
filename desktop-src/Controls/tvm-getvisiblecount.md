---
title: Mensaje de TVM_GETVISIBLECOUNT (commctrl. h)
description: Obtiene el número de elementos que pueden estar totalmente visibles en la ventana de cliente de un control de vista de árbol. Puede enviar este mensaje explícitamente o mediante la \_ macro GetVisibleCount de TreeView.
ms.assetid: c3519543-3fb2-4ecf-ac01-905d0946cb1b
keywords:
- TVM_GETVISIBLECOUNT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TVM_GETVISIBLECOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1927d21741b109c5f00aa964b058dc0c34732529
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996103"
---
# <a name="tvm_getvisiblecount-message"></a>\_Mensaje de GETVISIBLECOUNT TVM

Obtiene el número de elementos que pueden estar totalmente visibles en la ventana de cliente de un control de vista de árbol. Puede enviar este mensaje explícitamente o mediante la macro [**\_ GetVisibleCount de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getvisiblecount) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el número de elementos que pueden estar totalmente visibles en la ventana del cliente del control de vista de árbol.

## <a name="remarks"></a>Observaciones

El número de elementos que pueden estar totalmente visibles puede ser mayor que el número de elementos del control. El control calcula este valor dividiendo el alto de la ventana del cliente por el alto de un elemento.

Tenga en cuenta que el valor devuelto es el número de elementos que pueden estar *totalmente* visibles. Si puede ver todos los 20 elementos y parte de un elemento más, el valor devuelto es 20.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





