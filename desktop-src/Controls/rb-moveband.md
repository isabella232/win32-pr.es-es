---
title: RB_MOVEBAND mensaje (Commctrl.h)
description: Mueve una banda de un índice a otro.
ms.assetid: bb5b45de-957e-46fb-b59a-18b55b69c395
keywords:
- RB_MOVEBAND controles de Windows mensaje
topic_type:
- apiref
api_name:
- RB_MOVEBAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ab45f63b46b8bb883ef9f1fd8708f915dba2a6860ef2f6fabb09e2b00bd8fe6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119798545"
---
# <a name="rb_moveband-message"></a>Mensaje \_ MOVEBAND de RB

Mueve una banda de un índice a otro.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base cero de la banda que se va a mover.

</dd> <dt>

*lParam* 
</dt> <dd>

Índice de base cero de la nueva posición de banda.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si se realiza correctamente o cero en caso contrario.

## <a name="remarks"></a>Comentarios

Lo más probable es que este mensaje cambie el índice de otras bandas en el control rebar. Si una banda se mueve del índice 6 al índice 0, todas las bandas entre sí tendrán su índice incrementado en uno.

*lParam nunca* debe ser mayor que el número de bandas menos una. El número de bandas se puede obtener con el [**mensaje \_ GETBANDCOUNT de RB.**](rb-getbandcount.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





