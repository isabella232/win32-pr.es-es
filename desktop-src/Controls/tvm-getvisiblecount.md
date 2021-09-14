---
title: TVM_GETVISIBLECOUNT mensaje (Commctrl.h)
description: Obtiene el número de elementos que pueden ser totalmente visibles en la ventana de cliente de un control de vista de árbol. Puede enviar este mensaje explícitamente o mediante la macro TreeView \_ GetVisibleCount.
ms.assetid: c3519543-3fb2-4ecf-ac01-905d0946cb1b
keywords:
- TVM_GETVISIBLECOUNT controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165690"
---
# <a name="tvm_getvisiblecount-message"></a>Mensaje \_ GETVISIBLECOUNT de TVM

Obtiene el número de elementos que pueden ser totalmente visibles en la ventana de cliente de un control de vista de árbol. Puede enviar este mensaje explícitamente o mediante la macro [**TreeView \_ GetVisibleCount.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getvisiblecount)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el número de elementos que pueden ser totalmente visibles en la ventana de cliente del control de vista de árbol.

## <a name="remarks"></a>Observaciones

El número de elementos que pueden ser totalmente visibles puede ser mayor que el número de elementos del control . El control calcula este valor dividiendo el alto de la ventana cliente entre el alto de un elemento.

Tenga en cuenta que el valor devuelto es el número de elementos que pueden ser *totalmente* visibles. Si puede ver todos los 20 elementos y parte de un elemento más, el valor devuelto es 20.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





