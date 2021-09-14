---
title: TVM_GETITEMHEIGHT mensaje (Commctrl.h)
description: Recupera el alto actual de cada elemento de vista de árbol. Puede enviar este mensaje explícitamente o mediante la macro TreeView \_ GetItemHeight.
ms.assetid: 017476a3-1929-4a31-97a7-0f66175d47ea
keywords:
- TVM_GETITEMHEIGHT controles de Windows mensaje
topic_type:
- apiref
api_name:
- TVM_GETITEMHEIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 789347b7a50f9bb42a7aebb6fecddf24c42c559c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165733"
---
# <a name="tvm_getitemheight-message"></a>Mensaje \_ GETITEMHEIGHT de TVM

Recupera el alto actual de cada elemento de vista de árbol. Puede enviar este mensaje explícitamente o mediante la macro [**TreeView \_ GetItemHeight.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitemheight)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el alto de cada elemento, en píxeles.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TVM \_ SETITEMHEIGHT**](tvm-setitemheight.md)
</dt> </dl>

 

 





