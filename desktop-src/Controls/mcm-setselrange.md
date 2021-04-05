---
title: Mensaje de MCM_SETSELRANGE (commctrl. h)
description: Establece la selección de un control de calendario mensual en un intervalo de fechas determinado. Puede enviar este mensaje explícitamente o mediante la macro MonthCal \_ SetSelRange.
ms.assetid: 750b0c83-6baa-4caa-a738-feae8751a70e
keywords:
- MCM_SETSELRANGE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- MCM_SETSELRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad28966ab67a5e7c0d27dd8fc9c367ec30e4cd7b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078933"
---
# <a name="mcm_setselrange-message"></a>Mensaje de MCM \_ SETSELRANGE

Establece la selección de un control de calendario mensual en un intervalo de fechas determinado. Puede enviar este mensaje explícitamente o mediante la macro [**MonthCal \_ SetSelRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setselrange) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una matriz de dos elementos de estructuras [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) que contienen información de fecha que representa los límites de la selección. La primera fecha seleccionada se debe especificar en *lpSysTimeArray* \[ 0 \] y la última fecha seleccionada debe especificarse en *lpSysTimeArray* \[ 1 \] .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si es correcto o cero de lo contrario. Se producirá un error en este mensaje si se aplica a un control de calendario mensual que no use el estilo [**MCS \_ MultiSelect**](month-calendar-control-styles.md) .

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

 

