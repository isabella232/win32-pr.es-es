---
title: MCM_GETRANGE mensaje (Commctrl.h)
description: Recupera las fechas mínimas y máximas permitidos establecidas para un control de calendario mensual. Puede enviar este mensaje explícitamente o mediante la macro MonthCal \_ GetRange.
ms.assetid: 5000053a-2975-4781-b3c9-83f9763f679a
keywords:
- MCM_GETRANGE controles de Windows mensaje
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
ms.openlocfilehash: 26f8b9d5a485b12caf720afe518a2fc5499e55eba07c90c2fde1bb34eea2404b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117830399"
---
# <a name="mcm_getrange-message"></a>Mensaje \_ GETRANGE de MCM

Recupera las fechas mínimas y máximas permitidos establecidas para un control de calendario mensual. Puede enviar este mensaje explícitamente o mediante la macro [**MonthCal \_ GetRange.**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getrange)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una matriz de dos elementos de [**estructuras SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) que recibirá la información del límite de fecha. El límite mínimo se establece en *lprgSysTimeArray* \[ 0 \] y *lprgSysTimeArray* \[ 1 recibe el límite \] máximo. Si cualquiera de los elementos se establece en todos los ceros, no se establece ningún límite correspondiente para el control de calendario mensual. Este parámetro debe ser una dirección válida y no puede ser **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **DWORD** que puede ser cero (no se establecen límites) o una combinación de los siguientes valores que especifican información de límite:



| Código devuelto                                                                              | Descripción                                                                                                                        |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GDTR \_ MAX**</dt> </dl> | Se establece un límite máximo para el control; *lprgSysTimeArray* \[ 0 \] es válido y contiene la información de fecha aplicable. <br/> |
| <dl> <dt>**GDTR \_ MIN**</dt> </dl> | Se establece un límite mínimo para el control; *lprgSysTimeArray* \[ 1 \] es válido y contiene la información de fecha aplicable. <br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Horas del control Calendario mensual](month-calendar-controls.md)
</dt> </dl>

 

