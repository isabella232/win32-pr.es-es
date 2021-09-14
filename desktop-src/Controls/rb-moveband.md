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
ms.openlocfilehash: 146103c4c3d70fc0514729a00eac152c4847b85c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167302"
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

## <a name="remarks"></a>Observaciones

Lo más probable es que este mensaje cambie el índice de otras bandas en el control rebar. Si una banda se mueve del índice 6 al índice 0, todas las bandas entre sí tendrán su índice incrementado en uno.

*lParam nunca* debe ser mayor que el número de bandas menos una. El número de bandas se puede obtener con el [**mensaje \_ GETBANDCOUNT de RB.**](rb-getbandcount.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





