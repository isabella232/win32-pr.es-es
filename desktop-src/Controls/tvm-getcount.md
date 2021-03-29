---
title: Mensaje de TVM_GETCOUNT (commctrl. h)
description: Recupera un recuento de los elementos de un control de vista de árbol. Puede enviar este mensaje explícitamente o mediante la \_ macro getCount de TreeView.
ms.assetid: cb8477be-51c9-4e96-8fa6-f978e0c1595f
keywords:
- TVM_GETCOUNT controles de mensajes de Windows
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
ms.openlocfilehash: 870ca0d1e4bf04d054d29d78ab60371863648a8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492371"
---
# <a name="tvm_getcount-message"></a>Mensaje de la GETCOUNT de TVM \_

Recupera un recuento de los elementos de un control de vista de árbol. Puede enviar este mensaje explícitamente o mediante la macro [**\_ getCount de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getcount) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el recuento de elementos.

## <a name="remarks"></a>Observaciones

El número de nodos devueltos por la función [**\_ getCount de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getcount) se limita a los valores enteros. Si agrega un nodo más allá de 32767, la macro devuelve un valor negativo. Después de agregar 65536 nodos, el recuento vuelve a cero. Cuando esto ocurre, el control de vista de árbol aparece vacío sin barras de desplazamiento.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





