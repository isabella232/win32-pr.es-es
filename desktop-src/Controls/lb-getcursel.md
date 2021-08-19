---
title: LB_GETCURSEL mensaje (Winuser.h)
description: Obtiene el índice del elemento seleccionado actualmente, si existe, en un cuadro de lista de selección única.
ms.assetid: 39ab7f77-6c8e-45a4-aad4-47eba0a11a11
keywords:
- LB_GETCURSEL controles de Windows mensaje
topic_type:
- apiref
api_name:
- LB_GETCURSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d67a060669d48a9ab020540c78ece395504c9f0b7e36807e3ac59daf216ea395
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085525"
---
# <a name="lb_getcursel-message"></a>Mensaje \_ GETCURSEL de LB

Obtiene el índice del elemento seleccionado actualmente, si existe, en un cuadro de lista de selección única.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

No se usa; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

No se usa; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

En un cuadro de lista de selección única, el valor devuelto es el índice de base cero del elemento seleccionado actualmente. Si no hay ninguna selección, el valor devuelto es LB \_ ERR.

## <a name="remarks"></a>Comentarios

Para recuperar los índices de los elementos seleccionados en un cuadro de lista de selección múltiple, use el [**mensaje \_ LB GETSELITEMS.**](lb-getselitems.md) Para determinar si el elemento que tiene el rectángulo de foco en un cuadro de lista de selección múltiple está seleccionado, use el [**mensaje \_ LB GETSEL.**](lb-getsel.md)

Si se envía a un cuadro de lista de selección múltiple, **LB \_ GETCURSEL** devuelve el índice del elemento que tiene el rectángulo de foco. Si no se selecciona ningún elemento, devuelve cero.

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

[**LB \_ GETCARETINDEX**](lb-getcaretindex.md)
</dt> <dt>

[**LB \_ GETSEL**](lb-getsel.md)
</dt> <dt>

[**LB \_ GETSELITEMS**](lb-getselitems.md)
</dt> <dt>

[**LB \_ SETCURSEL**](lb-setcursel.md)
</dt> </dl>

 

 





