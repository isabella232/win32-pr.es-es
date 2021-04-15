---
title: Mensaje de DTM_GETRANGE (commctrl. h)
description: Obtiene las horas de sistema mínimas y máximas permitidas para un control de selector de fecha y hora (DTP). Puede enviar este mensaje explícitamente o utilizar la macro GetRange de fecha y hora \_ .
ms.assetid: 190cada6-49ee-483f-a464-d3d789127159
keywords:
- DTM_GETRANGE controles de mensajes de Windows
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
ms.openlocfilehash: a50a2ae9fe4ca77198f9e63548f709e0f571fdb0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491825"
---
# <a name="dtm_getrange-message"></a>DTM \_ GETRANGE

Obtiene las horas de sistema mínimas y máximas permitidas para un control de selector de fecha y hora (DTP). Puede enviar este mensaje explícitamente o utilizar la [**macro \_ GetRange de fecha y hora**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getrange) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una matriz de dos elementos de estructuras [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **DWORD** que es una combinación de GDTR \_ min o GDTR \_ Max. El primer elemento de la matriz [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) contiene el tiempo mínimo permitido si \_ se establece GDTR min. El segundo elemento de la matriz **SYSTEMTIME** contiene el tiempo máximo permitido si \_ se establece GDTR Max.

## <a name="remarks"></a>Observaciones

En el selector de fecha y hora solo se muestran las fechas y horas que se encuentran dentro del intervalo especificado, lo que impide que el usuario seleccione una fecha y hora fuera del intervalo. Si el [**mensaje \_ SETSYSTEMTIME de DTM**](dtm-setsystemtime.md) especifica una fecha y una hora que están fuera del intervalo, se producirá un error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

