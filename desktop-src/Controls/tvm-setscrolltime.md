---
title: TVM_SETSCROLLTIME mensaje (Commctrl.h)
description: Establece el tiempo de desplazamiento máximo para el control de vista de árbol. Puede enviar este mensaje explícitamente o mediante la macro TreeView \_ SetScrollTime.
ms.assetid: b0ad81ba-0621-42b7-8fe1-f3bd5bc16d6a
keywords:
- TVM_SETSCROLLTIME controles de Windows mensaje
topic_type:
- apiref
api_name:
- TVM_SETSCROLLTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c9ca3392de81a712aa6be7dc2addb87eedf65af4aa77958e5b7f5fbb2eafc87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118408492"
---
# <a name="tvm_setscrolltime-message"></a>Mensaje \_ SETCROLLTIME de TVM

Establece el tiempo de desplazamiento máximo para el control de vista de árbol. Puede enviar este mensaje explícitamente o mediante la macro [**TreeView \_ SetScrollTime.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setscrolltime)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Nuevo tiempo máximo de desplazamiento, en milisegundos.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el tiempo de desplazamiento máximo anterior, en milisegundos.

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

[**TVM \_ GETSCROLLTIME**](tvm-getscrolltime.md)
</dt> </dl>

 

 





