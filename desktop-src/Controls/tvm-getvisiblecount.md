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
ms.openlocfilehash: 07604eed3d3ece140d33bb9c612a2f898f6de02785f2c9916332de60358693fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119698665"
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

## <a name="remarks"></a>Comentarios

El número de elementos que pueden ser totalmente visibles puede ser mayor que el número de elementos del control . El control calcula este valor dividiendo el alto de la ventana cliente entre el alto de un elemento.

Tenga en cuenta que el valor devuelto es el número de elementos que pueden ser *totalmente* visibles. Si puede ver todos los 20 elementos y parte de uno más, el valor devuelto es 20.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





