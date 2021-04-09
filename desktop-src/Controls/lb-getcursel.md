---
title: Mensaje de LB_GETCURSEL (Winuser. h)
description: Obtiene el índice del elemento seleccionado actualmente, si existe, en un cuadro de lista de selección única.
ms.assetid: 39ab7f77-6c8e-45a4-aad4-47eba0a11a11
keywords:
- LB_GETCURSEL controles de mensajes de Windows
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
ms.openlocfilehash: 4a6209f1f5b67e059f9a2b8a224e6f96ec671e38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079717"
---
# <a name="lb_getcursel-message"></a>\_Mensaje lb GETCURSEL

Obtiene el índice del elemento seleccionado actualmente, si existe, en un cuadro de lista de selección única.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

No se utiliza; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

No se utiliza; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

En un cuadro de lista de selección única, el valor devuelto es el índice de base cero del elemento actualmente seleccionado. Si no hay ninguna selección, el valor devuelto es LB \_ Err.

## <a name="remarks"></a>Observaciones

Para recuperar los índices de los elementos seleccionados en un cuadro de lista de selección múltiple, use el mensaje [**lb \_ GETSELITEMS**](lb-getselitems.md) . Para determinar si el elemento que tiene el rectángulo de foco en un cuadro de lista de selección múltiple está seleccionado, use el mensaje [**lb \_ GETSEL**](lb-getsel.md) .

Si se envía a un cuadro de lista de selección múltiple, **lb \_ GETCURSEL** devuelve el índice del elemento que tiene el rectángulo de foco. Si no se selecciona ningún elemento, devuelve cero.

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

[**LB \_ GETCARETINDEX**](lb-getcaretindex.md)
</dt> <dt>

[**LB \_ GETSEL**](lb-getsel.md)
</dt> <dt>

[**LB \_ GETSELITEMS**](lb-getselitems.md)
</dt> <dt>

[**LB \_ SETCURSEL**](lb-setcursel.md)
</dt> </dl>

 

 





