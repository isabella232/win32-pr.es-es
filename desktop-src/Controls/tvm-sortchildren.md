---
title: TVM_SORTCHILDREN mensaje (Commctrl.h)
description: Ordena los elementos secundarios del elemento primario especificado en un control de vista de árbol. Puede enviar este mensaje explícitamente o mediante la macro TreeView \_ SortChildren.
ms.assetid: c18bcd5f-c083-46ee-873b-d3100b0d7b04
keywords:
- TVM_SORTCHILDREN controles de Windows mensaje
topic_type:
- apiref
api_name:
- TVM_SORTCHILDREN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f975814fadc5271c562e4e8e420c35dbb3450142bed797af83af73fdf81a55d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913805"
---
# <a name="tvm_sortchildren-message"></a>Mensaje \_ SORTCHILDREN de TVM

Ordena los elementos secundarios del elemento primario especificado en un control de vista de árbol. Puede enviar este mensaje explícitamente o mediante la macro [**TreeView \_ SortChildren.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sortchildren)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor que especifica si la ordenación es recursiva. Establezca *wParam en* **TRUE para** ordenar todos los niveles de elementos secundarios por debajo del elemento primario. De lo contrario, solo se ordenan los elementos secundarios inmediatos del elemento primario.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador del elemento primario cuyos elementos secundarios se van a ordenar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** de lo contrario.

## <a name="remarks"></a>Comentarios

Este mensaje alfabéticamente los elementos de árbol [**mediante lstrcmpi**](/windows/desktop/api/winbase/nf-winbase-lstrcmpia) en el nombre del elemento. Puede usar el mensaje [**\_ TVM SORTCHILDRENCB**](tvm-sortchildrencb.md) para personalizar el comportamiento de la ordenación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

