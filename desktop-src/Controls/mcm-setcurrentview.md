---
title: Mensaje de MCM_SETCURRENTVIEW (commctrl. h)
description: Establece la vista actual del calendario. Puede enviar este mensaje explícitamente o mediante la macro MonthCal \_ SetCurrentView.
ms.assetid: 26ccbb80-0dba-4241-a2eb-b79000fc3618
keywords:
- MCM_SETCURRENTVIEW controles de mensajes de Windows
topic_type:
- apiref
api_name:
- MCM_SETCURRENTVIEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d383c984932c19805f452cb39841c2edf36809b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997028"
---
# <a name="mcm_setcurrentview-message"></a>Mensaje de MCM \_ SETCURRENTVIEW

Establece la vista actual del calendario. Puede enviar este mensaje explícitamente o mediante la macro [**MonthCal \_ SetCurrentView**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcurrentview) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Nueva vista. Una de las constantes siguientes.



| Value                                                                                                                                                      | Significado                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="MCMV_MONTH"></span><span id="mcmv_month"></span><dl> <dt>**MCMV \_ mes**</dt> </dl>       | Vista mensual.<br/> |
| <span id="MCMV_YEAR"></span><span id="mcmv_year"></span><dl> <dt>**MCMV \_ año**</dt> </dl>          | Vista anual.<br/>  |
| <span id="MCMV_DECADE"></span><span id="mcmv_decade"></span><dl> <dt>**década de MCMV \_**</dt> </dl>    | Vista de década.<br/>  |
| <span id="MCMV_CENTURY"></span><span id="mcmv_century"></span><dl> <dt>**\_siglo MCMV**</dt> </dl> | Vista de siglo.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si es correcto o cero de lo contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





