---
title: Mensaje de MCM_SETRANGE (commctrl. h)
description: Establece las fechas mínima y máxima permitida para un control de calendario mensual. Puede enviar este mensaje explícitamente o mediante la macro MonthCal \_ SetRange.
ms.assetid: dab9ebb0-f397-4e71-b060-ef8d7d89a6bc
keywords:
- MCM_SETRANGE controles de mensajes de Windows
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
ms.openlocfilehash: 380e599da8cd4a054c02135bc64f57f29d2c81d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658326"
---
# <a name="mcm_setrange-message"></a>\_Mensaje de SetRange de MCM

Establece las fechas mínima y máxima permitida para un control de calendario mensual. Puede enviar este mensaje explícitamente o mediante la macro [**MonthCal \_ SetRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setrange) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valores de marca que especifican los límites de fecha que se establecen. Este valor debe ser uno de los siguientes:



| Value                                                                                                                                          | Significado                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GDTR_MAX"></span><span id="gdtr_max"></span><dl> <dt>**GDTR \_ máx.**</dt> </dl> | Se está configurando la fecha máxima permitida. La estructura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) en *lpSysTimeArray* \[ 1 \] debe contener información de fecha. <br/> |
| <span id="GDTR_MIN"></span><span id="gdtr_min"></span><dl> <dt>**GDTR \_ mín.**</dt> </dl> | Se está configurando la fecha mínima permitida. La estructura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) en *lpSysTimeArray* \[ 0 \] debe contener información de fecha. <br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una matriz de dos elementos de estructuras [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) que contiene los límites de fecha. El límite máximo debe estar en *lpSysTimeArray* \[ 1 \] si \_ se especifica GDTR Max y *lpSysTimeArray* \[ 0 \] debe contener el límite mínimo si \_ se especifica GDTR min.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si es correcto o cero de lo contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Horas en el control de calendario mensual](month-calendar-controls.md)
</dt> </dl>

 

