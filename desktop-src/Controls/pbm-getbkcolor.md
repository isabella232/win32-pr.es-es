---
title: PBM_GETBKCOLOR mensaje (Commctrl.h)
description: Obtiene el color de fondo de la barra de progreso.
ms.assetid: 9526ed78-08d9-468f-831b-72bb7c8c92d1
keywords:
- PBM_GETBKCOLOR controles de Windows mensaje
topic_type:
- apiref
api_name:
- PBM_GETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1462d864df0440cd0567e6d6b1d04261818bb98ab4a6b5a803272e63abcb8d5d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919525"
---
# <a name="pbm_getbkcolor-message"></a>Mensaje \_ GETBKCOLOR de PBM

Obtiene el color de fondo de la barra de progreso.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el color de fondo de la barra de progreso.

## <a name="remarks"></a>Comentarios

Este es el color establecido por el [**mensaje \_ SETBKCOLOR de PBM.**](pbm-setbkcolor.md) El valor predeterminado es CLR \_ DEFAULT, que se define en commctrl.h.

Esta función solo afecta al modo clásico, no a ningún estilo visual.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





