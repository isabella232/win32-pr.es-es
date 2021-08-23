---
title: MCM_GETCALENDARCOUNT mensaje (Commctrl.h)
description: Obtiene el número de calendarios que se muestran actualmente en el control de calendario. Puede enviar este mensaje explícitamente o mediante la macro MonthCal \_ GetCalendarCount.
ms.assetid: b9463f02-d37b-49b0-8387-0938020c23ee
keywords:
- MCM_GETCALENDARCOUNT controles de Windows mensaje
topic_type:
- apiref
api_name:
- MCM_GETCALENDARCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9379aa8c273451ba53c2a13d6190712212765b46dc1052a08b6d03ae4ae32e61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019053"
---
# <a name="mcm_getcalendarcount-message"></a>Mensaje \_ GETCALENDARCOUNT de MCM

Obtiene el número de calendarios que se muestran actualmente en el control de calendario. Puede enviar este mensaje explícitamente o mediante la macro [**MonthCal \_ GetCalendarCount.**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcalendarcount)

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

Número de calendarios que se muestran actualmente en el control de calendario. El número máximo de calendarios permitidos es 12.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





