---
title: Mensaje de LB_SETSEL (Winuser. h)
description: Selecciona un elemento en un cuadro de lista de selección múltiple y, si es necesario, desplaza el elemento a la vista.
ms.assetid: 643783f2-0e00-4b79-b957-47938bb9f8da
keywords:
- LB_SETSEL controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LB_SETSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd50f12c4190ba9ecafad11b167c1ac60adf691d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492430"
---
# <a name="lb_setsel-message"></a>\_Mensaje lb SETSEL

Selecciona un elemento en un cuadro de lista de selección múltiple y, si es necesario, desplaza el elemento a la vista.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica cómo establecer la selección. Si este parámetro es **true**, el elemento se selecciona y se resalta; Si es **false**, se quita el resaltado y ya no se selecciona el elemento.

</dd> <dt>

*lParam* 
</dt> <dd>

Especifica el índice de base cero del elemento que se va a establecer. Si este parámetro es-1, la selección se agrega o se quita de todos los elementos, dependiendo del valor de *wParam*, y no se produce ningún desplazamiento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se produce un error, el valor devuelto es LB \_ Err.

## <a name="remarks"></a>Observaciones

Use este mensaje solo con cuadros de lista de selección múltiple.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**LB \_ GETSEL**](lb-getsel.md)
</dt> <dt>

[**LB \_ SELITEMRANGE**](lb-selitemrange.md)
</dt> </dl>

 

 





