---
title: MCM_SETRANGE mensaje (Commctrl.h)
description: Establece las fechas mínimas y máximas permitidos para un control de calendario mensual. Puede enviar este mensaje explícitamente o mediante la macro MonthCal \_ SetRange.
ms.assetid: dab9ebb0-f397-4e71-b060-ef8d7d89a6bc
keywords:
- MCM_SETRANGE controles de Windows mensaje
topic_type:
- apiref
api_name:
- MCM_SETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c66e9cca17aabd93bfba896d361da6b90eab0c5c21fc4d50ec3c81a9eba5ccd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119319255"
---
# <a name="mcm_setrange-message"></a>Mensaje \_ SETRANGE de MCM

Establece las fechas mínimas y máximas permitidos para un control de calendario mensual. Puede enviar este mensaje explícitamente o mediante la macro [**MonthCal \_ SetRange.**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setrange)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Marca los valores que especifican qué límites de fecha se establecen. Este valor debe ser uno o ambos de los siguientes:



| Value                                                                                                                                          | Significado                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GDTR_MAX"></span><span id="gdtr_max"></span><dl> <dt>**GDTR \_ MAX**</dt> </dl> | Se establece la fecha máxima permitido. La [**estructura SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) en *lpSysTimeArray* \[ 1 debe contener información de \] fecha. <br/> |
| <span id="GDTR_MIN"></span><span id="gdtr_min"></span><dl> <dt>**GDTR \_ MIN**</dt> </dl> | Se establece la fecha mínima permitido. La [**estructura SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) en *lpSysTimeArray* \[ 0 debe contener información de \] fecha. <br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una matriz de dos elementos de [**estructuras SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) que contienen los límites de fecha. El límite máximo debe estar en *lpSysTimeArray* 1 si se especifica \[ \] GDTR \_ MAX y *lpSysTimeArray* 0 debe contener el límite mínimo si se especifica \[ \] GDTR \_ MIN.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si se realiza correctamente o cero en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Horas del control Calendario mensual](month-calendar-controls.md)
</dt> </dl>

 

