---
title: DTM_SETRANGE mensaje (Commctrl.h)
description: Establece las horas del sistema mínimas y máximas permitidos para un control selector de fecha y hora (DTP). Puede enviar este mensaje explícitamente o usar la macro DateTime \_ SetRange.
ms.assetid: ef0f48f2-906e-4ae0-839d-177e0fb7f14e
keywords:
- DTM_SETRANGE controles de Windows mensaje
topic_type:
- apiref
api_name:
- DTM_SETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 380bd35bd590facd1368507f2bf5900c05c4f68557cf1e4201058dfbacdb282d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877735"
---
# <a name="dtm_setrange-message"></a>Mensaje \_ SETRANGE de DTM

Establece las horas del sistema mínimas y máximas permitidos para un control selector de fecha y hora (DTP). Puede enviar este mensaje explícitamente o usar la macro [**DateTime \_ SetRange.**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setrange)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor que especifica qué valores de intervalo son válidos. Este parámetro puede ser una combinación de los valores siguientes:



| Value                                                                                                                                          | Significado                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GDTR_MIN"></span><span id="gdtr_min"></span><dl> <dt>**GDTR \_ MIN**</dt> </dl> | El primer elemento de la matriz [**de estructura SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) es válido y se usará para establecer el tiempo mínimo permitido del sistema.<br/>  |
| <span id="GDTR_MAX"></span><span id="gdtr_max"></span><dl> <dt>**GDTR \_ MAX**</dt> </dl> | El segundo elemento de la matriz [**de estructura SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) es válido y se usará para establecer el tiempo máximo permitido del sistema.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una matriz de dos elementos de [**estructuras SYSTEMTIME.**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) El primer elemento de la **matriz SYSTEMTIME** contiene el tiempo mínimo permitido. El segundo elemento de la **matriz SYSTEMTIME** contiene el tiempo máximo permitido. No es necesario rellenar un elemento de matriz que no se especifica en el *parámetro wParam.*

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si se realiza correctamente o cero en caso contrario.

## <a name="remarks"></a>Comentarios

El selector de fecha y hora muestra solo las fechas y horas que se encuentran dentro del intervalo especificado, lo que impide que el usuario seleccione una fecha y hora que se encuentran fuera del intervalo. Si el [**mensaje \_ DTM SETSYSTEMTIME**](dtm-setsystemtime.md) especifica una fecha y hora que se encuentran fuera del intervalo, se producirá un error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

