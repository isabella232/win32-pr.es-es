---
title: Mensaje de TVM_GETSCROLLTIME (commctrl. h)
description: Recupera el tiempo de desplazamiento máximo para el control de vista de árbol. Puede enviar este mensaje explícitamente o mediante la \_ macro GetScrollTime de TreeView.
ms.assetid: 992d1906-cda3-4ac7-ba90-c681c551ac2e
keywords:
- TVM_GETSCROLLTIME controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TVM_GETSCROLLTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6f0bacc6c12dd7f54f20d882faf738c11848d59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150058"
---
# <a name="tvm_getscrolltime-message"></a>\_Mensaje de GETSCROLLTIME TVM

Recupera el tiempo de desplazamiento máximo para el control de vista de árbol. Puede enviar este mensaje explícitamente o mediante la macro [**\_ GetScrollTime de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getscrolltime) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el tiempo de desplazamiento máximo, en milisegundos.

## <a name="remarks"></a>Observaciones

El tiempo de desplazamiento máximo es la cantidad más larga de tiempo que puede tardar una operación de desplazamiento. El desplazamiento se ajustará para que el desplazamiento tenga lugar dentro del tiempo de desplazamiento máximo. Una operación de desplazamiento puede tardar menos tiempo que el máximo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TVM \_ SETSCROLLTIME**](tvm-setscrolltime.md)
</dt> </dl>

 

 





