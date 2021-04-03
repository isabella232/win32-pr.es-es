---
title: Mensaje de TVM_SORTCHILDREN (commctrl. h)
description: Ordena los elementos secundarios del elemento primario especificado en un control de vista de árbol. Puede enviar este mensaje explícitamente o mediante la \_ macro SortChildren de TreeView.
ms.assetid: c18bcd5f-c083-46ee-873b-d3100b0d7b04
keywords:
- TVM_SORTCHILDREN controles de mensajes de Windows
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
ms.openlocfilehash: 341591c31accb4aab0b49f611359a93ec99c0cab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079705"
---
# <a name="tvm_sortchildren-message"></a>\_Mensaje de SORTCHILDREN TVM

Ordena los elementos secundarios del elemento primario especificado en un control de vista de árbol. Puede enviar este mensaje explícitamente o mediante la macro [**\_ SortChildren de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sortchildren) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor que especifica si la ordenación es recursiva. Establezca *wParam* en **true** para ordenar todos los niveles de los elementos secundarios por debajo del elemento primario. De lo contrario, solo se ordenan los elementos secundarios inmediatos del elemento primario.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador del elemento primario cuyos elementos secundarios se van a ordenar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto, o **false** en caso contrario.

## <a name="remarks"></a>Observaciones

Este mensaje alphabetizes los elementos de árbol mediante [**lstrcmpi**](/windows/desktop/api/winbase/nf-winbase-lstrcmpia) en el nombre del elemento. Puede usar el mensaje [**TVM \_ SORTCHILDRENCB**](tvm-sortchildrencb.md) para personalizar el comportamiento de ordenación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

