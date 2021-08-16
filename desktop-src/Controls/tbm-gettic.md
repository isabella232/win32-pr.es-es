---
title: TBM_GETTIC mensaje (Commctrl.h)
description: Recupera la posición lógica de una marca de graduación en una barra de seguimiento. La posición lógica puede ser cualquiera de los valores enteros del intervalo de posiciones del control deslizante mínimo al máximo de la barra de seguimiento.
ms.assetid: 9d70c860-de97-4579-bb10-e9e9db7f1784
keywords:
- TBM_GETTIC controles de Windows mensaje
topic_type:
- apiref
api_name:
- TBM_GETTIC
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b7cdd2c28f9add787c41da3cde3fabc3a5dff33812b3dd9c07a26a603d3a79e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829609"
---
# <a name="tbm_gettic-message"></a>Mensaje \_ GETTIC de TBM

Recupera la posición lógica de una marca de graduación en una barra de seguimiento. La posición lógica puede ser cualquiera de los valores enteros del intervalo de posiciones del control deslizante mínimo al máximo de la barra de seguimiento.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base cero que identifica una marca de graduación. Los índices válidos están en el intervalo de cero a dos menos que el número de tics devuelto por el [**mensaje \_ GETNUMTICS de TBM.**](tbm-getnumtics.md)

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve la posición lógica de la marca de graduación especificada o -1 si *wParam* no especifica un índice válido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





