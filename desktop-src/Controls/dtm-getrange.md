---
title: DTM_GETRANGE mensaje (Commctrl.h)
description: Obtiene las horas del sistema mínimas y máximas permitidos actuales para un control selector de fecha y hora (DTP). Puede enviar este mensaje explícitamente o usar la macro DateTime \_ GetRange.
ms.assetid: 190cada6-49ee-483f-a464-d3d789127159
keywords:
- DTM_GETRANGE controles de Windows mensaje
topic_type:
- apiref
api_name:
- DTM_GETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d9c0c90780e4bcd35da2d410f7b4743547cbd8d31ac06293c411f2415e4e408
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877955"
---
# <a name="dtm_getrange-message"></a>Mensaje \_ GETRANGE de DTM

Obtiene las horas del sistema mínimas y máximas permitidos actuales para un control selector de fecha y hora (DTP). Puede enviar este mensaje explícitamente o usar la macro [**DateTime \_ GetRange.**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getrange)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una matriz de dos elementos de [**estructuras SYSTEMTIME.**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor DWORD** que es una combinación de GDTR \_ MIN o GDTR \_ MAX. El primer elemento de la [**matriz SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) contiene el tiempo mínimo permitido si se establece GDTR \_ MIN. El segundo elemento de la **matriz SYSTEMTIME** contiene el tiempo máximo permitido si se establece GDTR \_ MAX.

## <a name="remarks"></a>Comentarios

El selector de fecha y hora muestra solo las fechas y horas que se encuentran dentro del intervalo especificado, lo que impide que el usuario seleccione una fecha y hora que se encuentran fuera del intervalo. Si el [**mensaje \_ SETSYSTEMTIME de DTM**](dtm-setsystemtime.md) especifica una fecha y hora que se encuentran fuera del intervalo, se producirá un error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

