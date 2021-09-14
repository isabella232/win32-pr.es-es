---
title: LB_GETANCHORINDEX mensaje (Winuser.h)
description: Obtiene el índice del elemento delimitador \ 8212; es decir, el elemento desde el que se inicia una selección múltiple. Una selección múltiple abarca todos los elementos desde el elemento delimitador hasta el elemento de careta.
ms.assetid: vs|controls|~\controls\listboxes\listboxreference\listboxmessages\lb_getanchorindex.htm
keywords:
- LB_GETANCHORINDEX controles de Windows mensaje
topic_type:
- apiref
api_name:
- LB_GETANCHORINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5502a234424b818bb46e9c4326839b5aff2f83d0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061894"
---
# <a name="lb_getanchorindex-message"></a>Mensaje \_ LB GETANCHORINDEX

Obtiene el índice del elemento delimitador, es decir, el elemento desde el que se inicia una selección múltiple. Una selección múltiple abarca todos los elementos desde el elemento delimitador hasta el elemento de careta.

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

El valor devuelto es el índice del elemento delimitador.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**LB \_ SETANCHORINDEX**](lb-setanchorindex.md)
</dt> </dl>

 

 





