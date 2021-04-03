---
title: Mensaje de TVM_GETITEMHEIGHT (commctrl. h)
description: Recupera el alto actual de cada elemento de vista de árbol. Puede enviar este mensaje explícitamente o mediante la \_ macro GetItemHeight de TreeView.
ms.assetid: 017476a3-1929-4a31-97a7-0f66175d47ea
keywords:
- TVM_GETITEMHEIGHT controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905675"
---
# <a name="tvm_getitemheight-message"></a>\_Mensaje de GETITEMHEIGHT TVM

Recupera el alto actual de cada elemento de vista de árbol. Puede enviar este mensaje explícitamente o mediante la macro [**\_ GetItemHeight de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitemheight) .

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
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TVM \_ SETITEMHEIGHT**](tvm-setitemheight.md)
</dt> </dl>

 

 





