---
title: LB_SELITEMRANGEEX mensaje (Winuser.h)
description: Selecciona uno o varios elementos consecutivos en un cuadro de lista de selección múltiple.
ms.assetid: aac85d72-43e2-4ab0-b9ee-c7a87e21d7a1
keywords:
- LB_SELITEMRANGEEX controles de Windows mensaje
topic_type:
- apiref
api_name:
- LB_SELITEMRANGEEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16e3112e36a7b212c1d0968ca738472000fabbf3d26d4d94e36ea9f21d80fe57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799445"
---
# <a name="lb_selitemrangeex-message"></a>Mensaje \_ LB SELITEMRANGEEX

Selecciona uno o varios elementos consecutivos en un cuadro de lista de selección múltiple.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica el índice de base cero del primer elemento que se debe seleccionar.

Windows 95/Windows 98/Windows Edition (Windows Me): el parámetro *wParam* está limitado a valores de 16 bits. Esto significa que los cuadros de lista no pueden contener más de 32 767 elementos. Aunque el número de elementos está restringido, el tamaño total en bytes de los elementos de un cuadro de lista solo está limitado por la memoria disponible.

</dd> <dt>

*lParam* 
</dt> <dd>

Especifica el índice de base cero del último elemento que se debe seleccionar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se produce un error, el valor devuelto es LB \_ ERR.

## <a name="remarks"></a>Comentarios

Si el *parámetro wParam* es menor que el parámetro *lParam,* se selecciona el intervalo de elementos especificado. Si *wParam es* mayor o igual que *lParam*, el intervalo se quita del intervalo de elementos especificado. Para seleccionar solo un elemento, seleccione dos elementos y anule la selección del elemento no deseado.

Use este mensaje solo con cuadros de lista de selección múltiple.

Este mensaje puede seleccionar un intervalo solo dentro de los primeros 65 536 elementos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**LB \_ SELITEMRANGE**](lb-selitemrange.md)
</dt> <dt>

[**LB \_ SETSEL**](lb-setsel.md)
</dt> </dl>

 

 





