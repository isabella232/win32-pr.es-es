---
title: TVM_GETSCROLLTIME mensaje (Commctrl.h)
description: Recupera el tiempo de desplazamiento máximo para el control de vista de árbol. Puede enviar este mensaje explícitamente o mediante la macro TreeView \_ GetScrollTime.
ms.assetid: 992d1906-cda3-4ac7-ba90-c681c551ac2e
keywords:
- TVM_GETSCROLLTIME controles de Windows mensaje
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
ms.openlocfilehash: e026a463476d5625f7632d7b6679ce94ca2c8ab6d8c6a050d8938bd46d9858b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118408502"
---
# <a name="tvm_getscrolltime-message"></a>Mensaje \_ DE TVM GETSCROLLTIME

Recupera el tiempo de desplazamiento máximo para el control de vista de árbol. Puede enviar este mensaje explícitamente o mediante la macro [**TreeView \_ GetScrollTime.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getscrolltime)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el tiempo de desplazamiento máximo, en milisegundos.

## <a name="remarks"></a>Comentarios

El tiempo de desplazamiento máximo es la mayor cantidad de tiempo que puede tardar una operación de desplazamiento. El desplazamiento se ajustará para que el desplazamiento se lleve a cabo dentro del tiempo de desplazamiento máximo. Una operación de desplazamiento puede tardar menos tiempo que el máximo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**TVM \_ SETSCROLLTIME**](tvm-setscrolltime.md)
</dt> </dl>

 

 





