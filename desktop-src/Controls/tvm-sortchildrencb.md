---
title: TVM_SORTCHILDRENCB mensaje (Commctrl.h)
description: Ordena los elementos de vista de árbol mediante una función de devolución de llamada definida por la aplicación que compara los elementos. Puede enviar este mensaje explícitamente o mediante la macro TreeView \_ SortChildrenCB.
ms.assetid: 1669e576-5e57-49f6-8097-7d6547306014
keywords:
- TVM_SORTCHILDRENCB controles de Windows mensaje
topic_type:
- apiref
api_name:
- TVM_SORTCHILDRENCB
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45f0ec311cc5ce0f972f3363ea97cd42874ca85807bf852296de0283fccc95c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118669481"
---
# <a name="tvm_sortchildrencb-message"></a>Mensaje \_ SORTCHILDRENCB de TVM

Ordena los elementos de vista de árbol mediante una función de devolución de llamada definida por la aplicación que compara los elementos. Puede enviar este mensaje explícitamente o mediante la macro [**TreeView \_ SortChildrenCB.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sortchildrencb)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Reservado. Debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura TVSORTCB.**](/windows/win32/api/commctrl/ns-commctrl-tvsortcb) El **miembro lpfnCompare** es la dirección de la función de devolución de llamada definida por la aplicación, a la que se llama durante la operación de ordenación cada vez que es necesario comparar el orden relativo de dos elementos de lista. Para obtener más información sobre la función de devolución de llamada, vea la descripción de **TVSORTCB.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





