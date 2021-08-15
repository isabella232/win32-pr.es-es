---
title: LB_SELITEMRANGE mensaje (Winuser.h)
description: Selecciona o anula la selección de uno o varios elementos consecutivos en un cuadro de lista de selección múltiple.
ms.assetid: 817d62df-98a3-40b3-8d62-86bf07ad797f
keywords:
- LB_SELITEMRANGE controles de Windows mensaje
topic_type:
- apiref
api_name:
- LB_SELITEMRANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87a08019f3d60e6c9bfe841067b48220b8fcfe75891c9bcc8db64bf28d219b15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958604"
---
# <a name="lb_selitemrange-message"></a>Mensaje \_ LB SELITEMRANGE

Selecciona o anula la selección de uno o varios elementos consecutivos en un cuadro de lista de selección múltiple.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

**TRUE** para seleccionar el intervalo de elementos o **FALSE** para anular la selección.

</dd> <dt>

*lParam* 
</dt> <dd>

[**Loword**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica el índice de base cero del primer elemento que se debe seleccionar. HIWORD [**especifica**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) el índice de base cero del último elemento que se debe seleccionar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se produce un error, el valor devuelto es LB \_ ERR.

## <a name="remarks"></a>Comentarios

Use este mensaje solo con cuadros de lista de selección múltiple.

Este mensaje puede seleccionar un intervalo solo dentro de los primeros 65 536 elementos.

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

[**LB \_ SELITEMRANGEEX**](lb-selitemrangeex.md)
</dt> <dt>

[**LB \_ SETSEL**](lb-setsel.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**MAKELPARAM**](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> </dl>

 

