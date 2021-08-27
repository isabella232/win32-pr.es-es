---
title: TVM_GETCOUNT mensaje (Commctrl.h)
description: Recupera un recuento de los elementos de un control de vista de árbol. Puede enviar este mensaje explícitamente o mediante la macro TreeView \_ GetCount.
ms.assetid: cb8477be-51c9-4e96-8fa6-f978e0c1595f
keywords:
- TVM_GETCOUNT controles de Windows mensaje
topic_type:
- apiref
api_name:
- TVM_GETCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fce2d3ed6580acc875007ff3962bbeb21e9c0d3c3cb38128a2339da79597f3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060355"
---
# <a name="tvm_getcount-message"></a>Mensaje \_ GETCOUNT de TVM

Recupera un recuento de los elementos de un control de vista de árbol. Puede enviar este mensaje explícitamente o mediante la macro [**TreeView \_ GetCount.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getcount)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el recuento de elementos.

## <a name="remarks"></a>Comentarios

El recuento de nodos devuelto por [**TreeView \_ GetCount**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getcount) se limita a valores enteros. Si agrega un nodo más allá de 32767, la macro devuelve un valor negativo. Después de agregar 65536 nodos, el recuento vuelve a cero. Cuando esto sucede, el control de vista de árbol aparece vacío sin barras de desplazamiento.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





