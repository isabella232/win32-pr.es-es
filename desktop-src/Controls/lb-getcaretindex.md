---
title: LB_GETCARETINDEX mensaje (Winuser.h)
description: Recupera el índice del elemento que tiene el foco en un cuadro de lista de selección múltiple. El elemento puede estar seleccionado o no.
ms.assetid: vs|controls|~\controls\listboxes\listboxreference\listboxmessages\lb_getcaretindex.htm
keywords:
- LB_GETCARETINDEX controles de Windows mensaje
topic_type:
- apiref
api_name:
- LB_GETCARETINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74732bae571cdcba0cfe8096437bf681e7a339c5c0edb3f18d378ea610bdf8c2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085545"
---
# <a name="lb_getcaretindex-message"></a>Mensaje \_ GETCARETINDEX de LB

Recupera el índice del elemento que tiene el foco en un cuadro de lista de selección múltiple. El elemento puede estar seleccionado o no.

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

El valor devuelto es el índice de base cero del elemento de cuadro de lista centrado, o 0 si ningún elemento tiene el foco.

## <a name="remarks"></a>Comentarios

Este mensaje también se puede usar para obtener el índice del elemento seleccionado actualmente en un cuadro de lista de selección única.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**LB \_ SETCARETINDEX**](lb-setcaretindex.md)
</dt> </dl>

 

 





