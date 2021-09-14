---
title: TVM_SETSCROLLTIME mensaje (Commctrl.h)
description: Establece el tiempo de desplazamiento máximo para el control de vista de árbol. Puede enviar este mensaje explícitamente o mediante la macro \_ SetScrollTime de TreeView.
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
ms.openlocfilehash: b49fab2f662b5ec641d9ffc6cc276f2196d2613e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165618"
---
# <a name="tvm_setscrolltime-message"></a>Mensaje \_ DE TVM SETSCROLLTIME

Establece el tiempo de desplazamiento máximo para el control de vista de árbol. Puede enviar este mensaje explícitamente o mediante la macro [**\_ SetScrollTime de TreeView.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setscrolltime)

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

## <a name="remarks"></a>Observaciones

El tiempo de desplazamiento máximo es la cantidad de tiempo más larga que puede tardar una operación de desplazamiento. El desplazamiento se ajustará para que el desplazamiento se lleve a cabo dentro del tiempo de desplazamiento máximo. Una operación de desplazamiento puede tardar menos tiempo que el máximo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TVM \_ GETSCROLLTIME**](tvm-getscrolltime.md)
</dt> </dl>

 

 





