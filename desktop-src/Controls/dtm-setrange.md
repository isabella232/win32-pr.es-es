---
title: Mensaje de DTM_SETRANGE (commctrl. h)
description: Establece las horas de sistema mínimas y máximas permitidas para un control de selector de fecha y hora (DTP). Puede enviar este mensaje explícitamente o usar la \_ macro DateTime SetRange.
ms.assetid: ef0f48f2-906e-4ae0-839d-177e0fb7f14e
keywords:
- DTM_SETRANGE controles de mensajes de Windows
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
ms.openlocfilehash: 70578e7d468c6a0e54d1373af2d46e680afbbe5b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803068"
---
# <a name="dtm_setrange-message"></a>\_Mensaje de SetRange DTM

Establece las horas de sistema mínimas y máximas permitidas para un control de selector de fecha y hora (DTP). Puede enviar este mensaje explícitamente o usar la macro [**DateTime \_ SetRange**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setrange) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor que especifica los valores de intervalo válidos. Este parámetro puede ser una combinación de los siguientes valores:



| Value                                                                                                                                          | Significado                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GDTR_MIN"></span><span id="gdtr_min"></span><dl> <dt>**GDTR \_ mín.**</dt> </dl> | El primer elemento de la matriz de estructuras [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) es válido y se utilizará para establecer la hora mínima permitida del sistema.<br/>  |
| <span id="GDTR_MAX"></span><span id="gdtr_max"></span><dl> <dt>**GDTR \_ máx.**</dt> </dl> | El segundo elemento de la matriz de estructuras [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) es válido y se utilizará para establecer la hora máxima permitida del sistema.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una matriz de dos elementos de estructuras [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) . El primer elemento de la matriz **SYSTEMTIME** contiene el tiempo mínimo permitido. El segundo elemento de la matriz **SYSTEMTIME** contiene el tiempo máximo permitido. No es necesario rellenar un elemento de matriz que no se especifica en el parámetro *wParam* .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si es correcto o cero de lo contrario.

## <a name="remarks"></a>Observaciones

En el selector de fecha y hora solo se muestran las fechas y horas que se encuentran dentro del intervalo especificado, lo que impide que el usuario seleccione una fecha y hora fuera del intervalo. Si el [**mensaje \_ SETSYSTEMTIME de DTM**](dtm-setsystemtime.md) especifica una fecha y una hora que están fuera del intervalo, se producirá un error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

