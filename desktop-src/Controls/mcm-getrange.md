---
title: Mensaje de MCM_GETRANGE (commctrl. h)
description: Recupera las fechas mínimas y máximas permitidas establecidas para un control de calendario mensual. Puede enviar este mensaje explícitamente o mediante la macro MonthCal \_ GetRange.
ms.assetid: 5000053a-2975-4781-b3c9-83f9763f679a
keywords:
- MCM_GETRANGE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- MCM_GETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c757c046b88479072eb0771ecbf3f7fb79cdb31b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905601"
---
# <a name="mcm_getrange-message"></a>Mensaje de MCM \_ GETRANGE

Recupera las fechas mínimas y máximas permitidas establecidas para un control de calendario mensual. Puede enviar este mensaje explícitamente o mediante la macro [**MonthCal \_ GetRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getrange) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una matriz de dos elementos de estructuras [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) que recibirá la información de límite de fecha. El límite mínimo se establece en *lprgSysTimeArray* \[ 0 \] y *lprgSysTimeArray* \[ 1 \] recibe el límite máximo. Si alguno de los elementos se establece en ceros, no se establece ningún límite correspondiente para el control de calendario mensual. Este parámetro debe ser una dirección válida y no puede ser **null**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor DWORD** que puede ser cero (no se establece ningún límite) o una combinación de los siguientes valores que especifican la información de límite:



| Código devuelto                                                                              | Descripción                                                                                                                        |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GDTR \_ máx.**</dt> </dl> | Se establece un límite máximo para el control; *lprgSysTimeArray* \[ 0 \] es válido y contiene la información de fecha aplicable. <br/> |
| <dl> <dt>**GDTR \_ mín.**</dt> </dl> | Se establece un límite mínimo para el control. *lprgSysTimeArray* \[ 1 \] es válido y contiene la información de fecha aplicable. <br/> |



 

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

 

