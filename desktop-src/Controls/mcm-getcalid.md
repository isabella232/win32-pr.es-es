---
title: MCM_GETCALID mensaje (Commctrl.h)
description: Obtiene el identificador de calendario para el control de calendario especificado. Puede enviar este mensaje explícitamente o mediante la \_ macro MonthCal GetPROCD.
ms.assetid: ecfab4f3-a5af-445d-8b90-243b646524a6
keywords:
- MCM_GETCALID controles de Windows mensaje
topic_type:
- apiref
api_name:
- MCM_GETCALID
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 148db880fe941c3b7df045c0ecdd4fbc9303203eace2b3be3ab38831aa4e3644
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118170192"
---
# <a name="mcm_getcalid-message"></a>Mensaje \_ GET HAND de MCM

Obtiene el identificador de calendario para el control de calendario especificado. Puede enviar este mensaje explícitamente o mediante la macro [**\_ MonthCal GetPROCD.**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcalid)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Identificador del calendario actual. Una de las [constantes de identificadores de](/windows/desktop/Intl/calendar-identifiers) calendario.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

