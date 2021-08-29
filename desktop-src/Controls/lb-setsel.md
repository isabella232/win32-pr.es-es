---
title: LB_SETSEL mensaje (Winuser.h)
description: Selecciona un elemento en un cuadro de lista de selección múltiple y, si es necesario, desplaza el elemento a la vista.
ms.assetid: 643783f2-0e00-4b79-b957-47938bb9f8da
keywords:
- LB_SETSEL controles de Windows mensaje
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
ms.openlocfilehash: 4830dc83a2b62fa87a222be276cdd9db55720014adeaa03362f4965bc0ecf246
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958534"
---
# <a name="lb_setsel-message"></a>Mensaje \_ DE LB SETSEL

Selecciona un elemento en un cuadro de lista de selección múltiple y, si es necesario, desplaza el elemento a la vista.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica cómo establecer la selección. Si este parámetro es **TRUE**, el elemento está seleccionado y resaltado; Si es **FALSE,** se quita el resaltado y el elemento ya no está seleccionado.

</dd> <dt>

*lParam* 
</dt> <dd>

Especifica el índice de base cero del elemento que se debe establecer. Si este parámetro es -1, la selección se agrega o se quita de todos los elementos, en función del valor de *wParam* y no se produce ningún desplazamiento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se produce un error, el valor devuelto es LB \_ ERR.

## <a name="remarks"></a>Comentarios

Use este mensaje solo con cuadros de lista de selección múltiple.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Referencia**
</dt> <dt>

[**LB \_ GETSEL**](lb-getsel.md)
</dt> <dt>

[**LB \_ SELITEMRANGE**](lb-selitemrange.md)
</dt> </dl>

 

 





