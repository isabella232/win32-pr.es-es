---
title: MCM_SETCALID mensaje (Commctrl.h)
description: Establece el identificador de calendario para el control de calendario especificado. Puede enviar este mensaje explícitamente o mediante la macro MonthCal \_ SetPROCD.
ms.assetid: 4b9d06f5-0784-4a17-b401-982206d4be67
keywords:
- MCM_SETCALID controles de Windows mensaje
topic_type:
- apiref
api_name:
- MCM_SETCALID
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b40e7f4577382aa0e003165e38e4557b8dc234592f747a579e5a071ce2440a37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119575585"
---
# <a name="mcm_setcalid-message"></a>Mensaje \_ SET UNAD DE MCM

Establece el identificador de calendario para el control de calendario especificado. Puede enviar este mensaje explícitamente o mediante la macro [**MonthCal \_ SetPROCD.**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcalid)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador del calendario. Una de las [constantes de identificadores de](/windows/desktop/Intl/calendar-identifiers) calendario.

</dd> <dt>

*lParam* 
</dt> <dd>

Debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Sin usar.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

