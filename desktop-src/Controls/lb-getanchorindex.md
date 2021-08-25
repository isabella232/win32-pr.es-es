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
ms.openlocfilehash: df33244a755ddd99a5af0c849e7753e478a91b94cd5cbd717505ca4ab37b0f9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799585"
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



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**LB \_ SETANCHORINDEX**](lb-setanchorindex.md)
</dt> </dl>

 

 





